pipeline{
    agent any

    stages {
        stage("Build Docker Image") {
            steps {
                bat 'docker build -t web-dev-img ./'
            }
        }
        
        stage("Run Docker container") {
            steps {
                bat 'docker run -d -p 3000:80 --name web-dev-container web-dev-img'
            }
        }
    }
}