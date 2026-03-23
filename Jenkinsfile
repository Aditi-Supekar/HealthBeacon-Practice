pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello from Jenkins!'
                sh 'echo "Running on: $(hostname)"'
                sh 'date'
            }
        }
        stage('Show System Info') {
            steps {
                sh 'whoami'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        stage('Done') {
            steps {
                echo 'Pipeline completed successfully!'
            }
        }
    }
    post {
        always {
            echo "Build result: ${currentBuild.result ?: 'SUCCESS'}"
        }
    }
}