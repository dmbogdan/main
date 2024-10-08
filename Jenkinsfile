pipeline {
	agent any

	stages {
		stage('Build') {
			steps {
				// comenzile pentru constructie
				sh 'echo Building the app myappJ'
				sh 'make build'
			}
		}
		stage('Test') {
			steps {
				//Comenzile pentru testare
				sh 'echo Running test for myappJ'
				sh 'make test'
			}
		}
		stage('Deploy') {
			steps {
				//Comenzi pentru livrare
				sh 'echo Deploying the application myappJ'
				sh 'make deploy'
			}
		}
	}	
}
