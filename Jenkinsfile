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
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
