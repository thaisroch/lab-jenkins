pipeline {
    agent any

    stages {
	stage ('Build Image'){
            steps {
		script {
                    dockerapp = docker.build("rochathais/api-produto", '-f ./src/Dockerfile ./src')
		}
            }
	}       
    }
}
