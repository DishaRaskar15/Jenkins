pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'No build needed for HTML project'
            }
        }

        stage('Test') {
            steps {
                echo 'Checking if index.html exists'
                bat 'if exist index.html (echo File exists) else (exit 1)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to XAMPP htdocs'
                bat '''
                if not exist C:\\xampp\\htdocs mkdir C:\\xampp\\htdocs
                xcopy * C:\\xampp\\htdocs\\ /E /H /C /I /Y
                '''
            }
        }
    }
}
