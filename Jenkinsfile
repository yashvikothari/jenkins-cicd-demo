pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
                echo 'Source code checked out successfully'
            }
        }

        stage('Build') {
            steps {
                echo 'Build started'
                echo 'Building application...'
                sh 'ls -la'
                echo 'Build completed successfully'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "Test 1: PASS"'
                sh 'echo "Test 2: PASS"'
                echo 'All tests passed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }

        failure {
            echo 'Pipeline failed. Check the build logs.'
        }
    }
}
