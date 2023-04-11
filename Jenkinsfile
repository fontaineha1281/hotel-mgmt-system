pipeline {
    agent any
    tools {
        nodejs "NodeJS"
    }
    stages {
        stage('Checkout') {
            steps {
                // Clone your React project from your repository
                git branch: 'master', url: 'https://github.com/fontaineha1281/hotel-mgmt-system.git'
            }
        }       
        stage('Build') {
            steps {
                // Build your React project
                sh 'npm i'
            }
        }
        stage('Serve') {
            steps {
                sh 'serve -s build'
            }
        }
    }
}
