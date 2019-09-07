pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-u root -p 3000:3000 -v $NPM_CONFIG_PREFIX=/home/node/.npm-global -v PATH=$PATH:/home/node/.npm-global/bin'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'whoami && npm install'
            }
        }
    }
}
