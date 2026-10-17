
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
                grep -q "Hello, I'm Megha" index.html
                echo 'Website files verified successfully!'
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

