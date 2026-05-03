pipeline {
    agent any

    environment {
        DEPLOY_DIR = "/var/www/html"
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/DishaRaskar15/Jenkins.git'
            }
        }

        stage('Build') {
            steps {
                echo "No build step (static project assumed)"
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                mkdir -p /var/www/html
                rm -rf /var/www/html/*
                cp -r * /var/www/html/
                '''
            }
        }
    }
}
