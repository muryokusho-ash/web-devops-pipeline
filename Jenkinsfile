pipeline{
    agent any

    stages {
        stage("Build Docker Image") {
            step {
                bat 'docker build -t web-dev-img ./'
            }
        }
        
        stage("Build Docker Image") {
            step {
                bat 'docker run -d -p 3000:80 --name web-dev-container web-dev-img'
            }
        }
    }
}