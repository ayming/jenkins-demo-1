pipeline {
    agent {
        docker { image 'node:14.17-alpine' }
    }

    stages {
        stage('Enviroment') {
            steps {
                sh 'pwd'
                sh 'ls -al'
                sh 'cat /etc/os-release'
                sh 'node -v'
                sh 'npm -v'
                sh 'yarn -v'
            }
        }
        stage('Build') {
            steps {
                sh 'yarn'
                sh 'yarn build'
            }
        }
        stage('Test') {
            steps {
                sh 'yarn lint'
                sh 'yarn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
