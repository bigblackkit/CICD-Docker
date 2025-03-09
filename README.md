![CI_CD_Docker](https://github.com/user-attachments/assets/a76e3c82-f178-4788-bb4b-3ca85438a2f8)

############################################################################

1. После того как в Main ветку репозитория СI/CD-Docker внесли изменения,
отправляется Webhook в Jenkins.
2. Jenkins в свою очередь использует файл с инструкциями с репозитория
В дженкинс файле:
 - Delete old container and image
 - Build new docker image
 - Run new Docker Image

Что касается стенда на котором всё это выполнялось: OS ubuntu-22.04.5-live-server-amd64 , в качестве средства виртуализации использовал Oracle VirtualBox Данный проект выполнялся для самообучения, хотелось всё развернуть своими руками используя документацию и сторонние гайды конечно, куда без них ))

############################################################################

1. After changes have been made to the Main branch of the CI/CD-Docker repository,
a Webhook is sent to Jenkins.
2. Jenkins in turn uses a file with instructions from the repository
In the Jenkins file:
- Delete old container and image
- Build new docker image
- Run new Docker Image

As for the stand on which all this was performed: OS ubuntu-22.04.5-live-server-amd64, Oracle VirtualBox was used as a virtualization tool This project was carried out for self-study, I wanted to deploy everything myself using documentation and third-party guides, of course, where without them))
