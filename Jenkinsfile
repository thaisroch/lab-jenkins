pipeline {
    agent any

    stages {
	stage ('Biuld Image'){
            steps {
		script{
                  dockerapp = docker.biuld("rochathais/api-produto", '-f ./src/Dockerfile ./src')
		}
            }
	}       
    }
}
