pipeline {
    agent {
        label 'jenkins-slave'
    }
    stages {
        stage('build') {
            steps{
                echo "building new code"
            }
        }
        stage('scanning') {
            steps{
                echo "scanning the code"
            }
        }
        stage("deployToprod") {
            options {
                timeout (time: 300, units: 'SECONDS')
            }
            input {
                message 'are you directly deploying into production'
                ok 'yes'
                submitter 'sai,venkat,nagasai'
            }
            steps {
                echo "deploying the code into production"
            }
        }
    }
}
