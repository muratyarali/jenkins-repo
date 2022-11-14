pipeline {
    agent any
    stages {
        stage('run') {
            steps {
                echo 'Clarusway_Way to Reinvent Yourself'
                sh '''
                python --version
                python pipeline.py
                '''
            }
        }
    }
}