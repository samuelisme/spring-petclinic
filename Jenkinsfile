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
                withDockerRegistry([ credentialsId: "DockerHub", url: "" ]) {
                    dockerImage.push()
                }
            }
        }
    }    
}
