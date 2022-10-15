pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                sh '''
                aws ecr get-login-password --region us-east-2 | docker login --username AWS --password-stdin 286076086092.dkr.ecr.us-east-2.amazonaws.com
                docker build -t 286076086092.dkr.ecr.us-east-2.amazonaws.com/khyathi-sttaiuc .
                docker push 286076086092.dkr.ecr.us-east-2.amazonaws.com/khyathi-sttaiuc:1
                '''
            }
        }
    }
}