pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'a9ebcdd8-c5d0-41a5-93ea-f77fb0e9d121', url:'https://git.epam.com/logesh_devaraj/webapp.git']])
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
