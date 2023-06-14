pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                script {
                    sh """
                        aws ecr get-login-password --region eu-north-1 | sudo docker login --username AWS --password-stdin 087541746984.dkr.ecr.eu-north-1.amazonaws.com
                        sudo docker build -t 087541746984.dkr.ecr.eu-north-1.amazonaws.com/backend:latest .
                        sudo docker push 087541746984.dkr.ecr.eu-north-1.amazonaws.com/backend:latest
                    """
                    }
            }
        }
    }
}