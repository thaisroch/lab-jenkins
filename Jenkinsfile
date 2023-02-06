pipeline {
    agent any

    stages {
	stage ('Build Image'){
            steps {
		script {
                    dockerapp = docker.build("rochathais/api-produto:${env.BUILD_ID}", '-f ./src/Dockerfile ./src')
		}
            }
	}
	stage ('Push Image'){
	    steps {
		script{
		    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub')
			dockerapp.push('latest')
			dockerapp.push('${end.BUIlD_ID}')
			
		}
	    }	
	}       
    }
}
