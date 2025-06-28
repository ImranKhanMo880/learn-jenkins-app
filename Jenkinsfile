pipeline {
    agent any

    stages {
        stage('Build') {

            agent{
                image 'node:18-alphine'
                reuseNode true
            }
            steps {
                sh '''
                la -la
                node --version
                npm --version
                npm ci
                npm run build
                la -la
                '''
            }
        }
    }
}
