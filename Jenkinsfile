pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/YOUR_USERNAME/simple-website.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("simple-website")
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    docker.image("simple-website").run("-d -p 8081:80")
                }
            }
        }
    }
}
