pipeline {
    agent any

    stages {

        stage('Build Backend Image') {
            steps {
                echo 'Starting backend build stage'
                sh '''
                echo "Workspace contents:"
                ls
                echo "Backend build simulated successfully"
                '''
            }
        }

        stage('Deploy Backend Containers') {
            steps {
                sh '''
                BACKEND_COUNT=1
                if [ "$BACKEND_COUNT" = "1" ]; then
                    echo "Simulating deployment of 1 backend container"
                else
                    echo "Simulating deployment of 2 backend containers"
                fi
                '''
            }
        }

        stage('Deploy NGINX Load Balancer') {
            steps {
                echo 'Simulating NGINX load balancer deployment'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Check console logs for errors.'
        }
        success {
            echo 'Pipeline executed successfully.'
        }
    }
}

