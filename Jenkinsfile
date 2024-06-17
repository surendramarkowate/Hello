pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/surendramarkowate/Hello-World.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'npm install'  // Example build step for Node.js project
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
