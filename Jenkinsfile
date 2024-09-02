pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Bxnnybi/spring-petclinic.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('spring-petclinic:latest')
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('spring-petclinic:latest').run('-d -p 8080:8080')
                }
            }
        }

        stage('Post-Build Actions') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }
}
