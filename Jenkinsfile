pipeline {
    agent any

    stages {
        stage('Checkout Source Code') {
            steps {
                echo 'Pulling code from Git repository...'
                checkout scm
            }
        }

        stage('Build & Execute Script') {
            steps {
                echo 'Running test.py...'
                bat '"C:\\Users\\STUDENT\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" test.py'
            }
        }

        stage('Code Stability Check') {
            steps {
                echo 'Verifying pipeline execution...'
                bat 'echo "Python script executed successfully!"'
            }
        }
    }

    post {
        success {
            echo 'SUCCESS: CI Pipeline completed successfully!'
        }
        failure {
            echo 'FAILURE: Pipeline failed. Check build logs.'
        }
    }
}
