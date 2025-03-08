pipeline{
    agent any
    stages{

        stage("Delete old container and image"){
            steps{
                 echo "=========Check old container & image========"
                 sh ''' 
                     if docker ps -a | grep "my_site"

                     then
                         echo "=======Removed old versions========"
                         docker stop my_site
                         docker rm my_site
                         docker rmi site_on_docker:gitlab
                     else
                         echo "=======Old versions not found======="

                     fi
                 '''
                 }
        }

        stage("Make Docker Image"){
            steps{
                echo "========Build========"
                sh 'echo "Build by Jenkins Build# $BUILD_ID" >> index.html'
                sh 'docker build -t site_on_docker:gitlab .'
                 }
         }
        stage("Run Docker Image"){
            steps{
                echo "========Run Image Run========"
                sh 'docker run -d -p 7777:80 --name my_site --restart=always  site_on_docker:gitlab'
            }
        
        }
    }
}
