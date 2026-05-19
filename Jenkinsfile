pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t preet1018/learning-docker-react -f Dockerfile.dev .'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'docker run -e CI=true preet1018/learning-docker-react npm test'
            }
        }
    }
}