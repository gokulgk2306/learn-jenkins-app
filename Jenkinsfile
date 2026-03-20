pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                ls -la
                node --version
                npm --version
                npm ci
                npm run build
                ls -la
            '''    
            }
        }
        stage('Test'){
            steps {
            sh '''
            echo "Test Stage"
            if [ -f "/workspaces/learn-jenkins-app/public/index/html" ]; then
                echo "File exists"
            else
                echo "File not found"
            fi
            npm test
            '''
        }
        }
    }
}
