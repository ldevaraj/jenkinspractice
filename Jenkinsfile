pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '2771a3c9-f3ee-456e-b182-f5751417a047', url: 'https://github.com/ldevaraj/jenkinspractice.git']])
            }
        }
         stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }
         stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
