pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Lab 2: Jenkins pipeline started'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the demo application...'
                sh 'echo "Build successful"'
            }
        }

        stage('Test') {
            steps {
                echo 'Running demo tests...'
                sh 'test -f Jenkinsfile'
                echo 'Tests passed'
            }
        }

        stage('Finish') {
            steps {
                echo 'Lab 2 completed successfully'
            }
        }
    }

    post {
        success {
            echo 'SUCCESS: Lab 2 pipeline passed'
        }
        failure {
            echo 'FAILURE: Check the console output'
        }
    }
}
