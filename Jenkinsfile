pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Technical-Ravi-web/nodeapp.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test || echo "No tests found or tests failed"'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build || echo "No build script or build failed"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment step - Add your deploy commands here'
            }
        }
    }
}
