pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install') {
          steps {
            sh 'npm install'
          }
        }
        stage('Generate') {
            steps {
                sh 'npm start'
            }
        }
        stage('Move') {
            steps {
                sh 'cp web/index.html /var/www/bridzius.lt/html/index.html'
            }
        }
    }
}