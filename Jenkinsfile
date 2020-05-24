pipeline {
	agent any
	stages {

		stage('Lint HTML') {
			steps {
				sh 'tidy -q -e *.html'
			}
		}
		
		stage('Build Docker Image') {
			steps {
				withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'dockerhub', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD']]){
					sh '''
						
						docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD
						docker build -t rashmijoyappa/capstone .
					'''
				}
			}
		}

		stage('Push Image To Dockerhub') {
			steps {
				withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'dockerhub', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD']]){
					sh '''
						docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD
						docker push rashmijoyappa/capstone
					'''
				}
			}
		}

		stage('Set current kubectl context') {
			steps {
				withAWS(region:'us-east-2', credentials:'capstone') {
					sh '''
						kubectl config get-contexts
					'''
				}
			}
		}

		
		
		

	}
}
