pipeline { 
    agent any

    stages {
        stage('Build & Tag Docker Image') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'dockercreds', toolName: 'docker') {
                        sh "docker build -t devopsvishal077758/shippingservice:latest ."
                    }
                }
            }
        }
        
        stage('Push Docker Image') {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'dockercreds', toolName: 'docker') {
                        sh "docker push devopsvishal077758/shippingservice:latest "
                    }
                }
            }
        }
    }
}
