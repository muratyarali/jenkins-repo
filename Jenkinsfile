pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'Clarusway_Way to Reinvent Yourself'
                sh 'echo Integrating Jenkins Pipeline with GitHub Webhook using Jenkinsfile'
            }
        }

        stage('run') {
            steps {
                echo 'Clarusway_Way to Reinvent Yourself'
                sh '''
                python --version
                python pipeline.py
                '''
            }
        }

        stage('test') {
            steps {
                echo 'Clarusway_Way to Reinvent Yourself'
            }
        }
    }
}