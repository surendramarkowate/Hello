pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository from GitHub
                git 'https://github.com/surendramarkowate/Hello-World'
            }
        }
        
        stage('Install Dependencies') {
            steps {
                // Install npm dependencies
                sh 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                // Build your project (if needed)
                // For a static website, this might not be necessary
                sh 'npm run build'  // Adjust this command based on your project setup
            }
        }
        
        stage('Test') {
            steps {
                // Run tests (if applicable)
                sh 'npm test'  // Adjust this command based on your project setup
            }
        }
        
        stage('Deploy') {
            steps {
                // Deployment steps (if applicable)
                // Example: Deploy to Nginx or any other server
                sh 'sudo systemctl restart nginx'  // Restart Nginx as an example
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline succeeded! Your application is deployed.'
        }
        failure {
            echo 'Pipeline failed! There may be issues with your build or tests.'
        }
    }
}
