pipeline {
    agent any

    stages {
        stage('build') {
            agent{
                docker{
                    image 'npm:18-alpine'
                }
            }
            steps {
                sh '''
                node -v
                npm -v
                npm ci
                npm run build
                '''
            }
        }
    }
}
