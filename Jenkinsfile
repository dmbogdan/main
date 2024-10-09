pipeline {
	agent any


		stages{	
			stage('Install Dependencies'){
				steps {
					sh 'apt-get update && apt-get install -y build-essential'
					sh 'apt-get update && apt-get install -y make'
				}
			}
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
			stage('check tools'){
				steps {
					sh 'which make || echo "make not found" '
					sh 'make --version || echo "Unable to get version" '
					}
				}
		}	
	}
