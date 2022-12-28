pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                sh 'java --version'
            }
        }
        stage('Push image') {
            steps {
                script {
                    def customImage = docker.build("my-image:${env.BUILD_ID}")
                    customImage.push()
                }
            }
        }
    }
}
