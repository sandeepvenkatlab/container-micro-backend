pipeline {
    agent any
    stages {
        stage("build") {
            steps {
                script {
                    sh """
                        aws ecr get-login-password --region eu-north-1 | sudo docker login --username AWS --password-stdin 703858353487.dkr.ecr.us-east-2.amazonaws.com
                        sudo docker build -t 703858353487.dkr.ecr.us-east-2.amazonaws.com/backend:latest .
                        sudo docker push 703858353487.dkr.ecr.us-east-2.amazonaws.com/backend:latest
                    """
                    }
            }
        }
    }
}