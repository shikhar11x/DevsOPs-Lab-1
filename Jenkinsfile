
pipeline {
    agent any

    options {
        timestamps()
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the web application'

                sh '''
                    test -f index.html
                    test -f style.css
                    echo "Build completed successfully"
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Testing application files'

                sh '''
                    grep -q "My First CI/CD Pipeline" index.html
                    grep -q "body" style.css
                    echo "All tests passed"
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to Nginx'

                sh '''
                    cp index.html style.css /var/www/html/
                    echo "Deployment completed successfully"
                '''
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'CI/CD Pipeline failed. Check the logs.'
        }

        always {
            echo 'Pipeline execution finished.'
        }
    }
}
