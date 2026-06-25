pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Sudhevan01/jenkins_demo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t web-image .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8090:80 web-image'
            }
        }
    }
}