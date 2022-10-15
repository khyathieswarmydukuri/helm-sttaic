pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                sh '''
                aws ecr get-login-password --region us-east-2 | sudo docker login --username AWS --password-stdin 286076086092.dkr.ecr.us-east-2.amazonaws.com
                 sudo docker build -t 286076086092.dkr.ecr.us-east-2.amazonaws.com/khyathi-sttaiuc .
                sudo docker push 286076086092.dkr.ecr.us-east-2.amazonaws.com/khyathi-sttaiuc:1
                '''
            }
        }
    }
}