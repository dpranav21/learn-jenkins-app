pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker{
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh'''
                cat build/index.html
                '''
            }
        }
        stage('Test'){
            steps{
                sh'''
                test -f build/index.html
                '''
            }
        }
    }
}
