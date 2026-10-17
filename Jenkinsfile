
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test Website') {
            steps {
                sh 'test -f index.html'
                echo 'Website file exists and is ready for deployment!'
            }
        }

        stage('Deploy Website') {
            steps {
                sh 'cp index.html /var/www/html/index.html'
                echo 'Website deployed to Nginx successfully!'
            }
        }
    }
}
