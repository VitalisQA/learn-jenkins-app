pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    npm ci
                    npm run build
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
                    echo "Test stage"
                    // test -f build/index.html
                    // npm test
                '''
            }
        }
    }
}