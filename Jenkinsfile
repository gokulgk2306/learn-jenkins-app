pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh 'echo "Hello from Jenkins"'
                sh "whoami"
                sh "pwd"
                sh 'echo "Done from Git"'
            }
        }
    }
}
