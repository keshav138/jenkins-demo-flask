pipeline{
    agent any

    stages{
        stage('Build docker image'){
            steps{
                sh 'docker build -t flask-demo-app .'
            }
        }

        stage('Start Docker container'){
            steps{
                sh 'docker rm -f flask-container || true'
                sh 'docker run -d -p 5000:5000 --name flask-container flask-demo-app'
            }
        }
    }
}