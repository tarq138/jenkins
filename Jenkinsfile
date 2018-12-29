pipeline {
    agent { docker { image 'python:3.5.1' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('print') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
#        stage('Deploy'){
#            steps {
#                retry(3){
#                    sh '/home/ukniazeu/flakey-deploy.sh'
#                }
#
#                timeout(time:3, unit: 'MINUTES'){
#                    sh './health-check.sh'
#                }
#            }
#        }
    }
}