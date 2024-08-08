pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/malmayahi/dynamic-website.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                // Add build steps here if needed
            }
        }
        stage('Deploy') {
            steps {
                sh 'scp -i /var/lib/jenkins/.ssh/testkey.pem -o StrictHostKeyChecking=no -r * ubuntu@your-web-server-ec2-public-ip:/var/www/html'
            }
        }
    }
}

