pipeline {
    agent any
    stages {
        stage('docker build') {
            steps {
                script {
                    sh "docker build -f 02-primer-pipeline/Dockerfile -t paulocgc/devops-crash-course:1.0.0-${BUILD_ID} 02-primer-pipeline"
                }
            }
        }
        stage('docker push') {
            steps {
                script {
                    sh "docker push paulocgc/devops-crash-course:1.0.0-${BUILD_ID}"
                }
            }
        }
    }
}
