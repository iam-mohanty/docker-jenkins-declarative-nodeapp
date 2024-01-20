pipeline {
    agent any

    stages {
        stage('code clone') {
            steps {
                echo "code cloning..."
                git url: "https://github.com/iam-mohanty/docker-jenkins-declarative-nodeapp.git"
            }
        }
        stage('code build') {
            steps {
                echo "code building..."
                sh "docker build . -t nodeappimg:latest"
            }
        }
        stage('code test') {
            steps {
                echo "code testing..."
            }
        }
        stage('code deploy') {
            steps {
                echo "deploying..."
                sh "docker run -itd -p 8000:8000 nodeappimg:latest"
            }
        }
    }
}
