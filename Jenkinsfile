pipeline {
    agent {
        docker {
            image 'node:0.10.35'
            args '-p 3000:3000'
            args '-u root:root'
        }
    }
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                sh 'npm test' 
            }
        }
    }
}