pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/basyalsunil/sampleweb.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the website...'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                cp -r * /var/www/html/sampleweb/
                '''
            }
        }
    }

    post {
        success {
            echo 'Deployment succeeded!'
        }
        failure {
            echo 'Deployment failed.'
        }
    }
}

