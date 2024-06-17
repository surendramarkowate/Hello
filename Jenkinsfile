pipeline {
    agent any

    environment {
        NODEJS_VERSION = '14'  // Specify the Node.js version
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/surendramarkowate/Hello-World.git'
            }
        }

        stage('Build') {
            steps {
                // Use Node.js 14 for this stage
                withNodejs(nodejsInstallationName: 'Node.js 14') {
                    sh 'npm install'
                }
            }
        }

        // Add more stages as per your build/deployment process
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
