pipeline {
    agent any

    environment {
        // Define environment variables if needed
    }

    stages {

        stage('Install Dependencies') {
            steps {
                script {
                    // Install frontend dependencies
                    dir('frontend') {
                        sh 'npm install'
                    }
                    // Install backend dependencies
                    dir('backend') {
                        sh 'npm install'
                    }
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    dir('frontend') {
                        sh 'npm run build'
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    dir('frontend') {
                        sh 'echo npm-test'
                    }
                }
            }
        }

        stage('Dockerize and Deploy') {
            steps {
                script {
                    sh 'echo docker-build--t-react-app .'
                }
            }
        }
    }
}
