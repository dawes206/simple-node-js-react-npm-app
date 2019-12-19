pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
		sh 'echo "$HTTP_PROXY"'
		sh 'echo "hello world"'
		sh 'npm config set proxy http://one.proxy.att.com:8080'
                sh 'npm install'
            }
        }
    }
}
