pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/<your-username>/<your-repo>.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t hello-supraja .'
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    sh 'docker rm -f hello-supraja || true'
                    sh 'docker run -d -p 8080:80 --name hello-supraja hello-supraja'
                }
            }
        }
    }
}
