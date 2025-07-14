
pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo "building the code"
            }
        }
        stage('codequality') {
            steps {
                 echo "checking the code quality"
            }
        }
        stage('Dockerbuildnpush') {
            steps {
                echo "building the docker"    
            }
        }
        stage('k8s') {
            steps {
                echo "deploying the image into k8s"
            }
        }
        stage("deploytoproduction") {
            options {
                timeout(time: 300, unit: 'SECONDS')
            }
            input {
                message  "doing deploying in production??????"
                ok 'yes'
                submitter 'Nagasaivardhan,devsai'
            }
            steps {
                echo "deploy the production"
            }
           
        }
        
    }
}
