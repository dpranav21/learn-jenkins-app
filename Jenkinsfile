pipeline {
    agent any

    stages {
        stage('Test'){
            steps{
                sh'''
                test -f build/index.html
                '''
            }
        }
    }
}
