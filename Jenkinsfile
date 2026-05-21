pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/starhacker577/WattWheels.git'
            }
        }

        stage('Build Backend Docker Image') {
            steps {
                bat 'docker build -t wattwheels-backend ./backend'
            }
        }

        stage('Build Frontend Docker Image') {
            steps {
                bat 'docker build -t wattwheels-frontend ./frontend/app'
            }
        }

        stage('Run Docker Compose') {
            steps {
                bat 'docker compose up -d'
            }
        }
    }
}