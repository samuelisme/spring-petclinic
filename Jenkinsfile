pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                sh 'java --version'
            }
        }
        stage('Push image') {
        withDockerRegistry([ credentialsId: "DockerHub", url: "" ]) {
        dockerImage.push()
        }
    }    
    }
}
