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
                sh 'composer install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cd /var/lib/jenkins/workspace/Hotel/'
                sh 'sudo cp -r * /var/www/hotel/'
                sh 'sudo systemctl reload nginx'
            }
        }
    }
}
