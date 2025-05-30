pipeline {
	agent any {
	tools{
		maven 'maven'
	}
	stages {
		stage ('Checkout') {
			steps {
				git branch: 'master', url: ''
			}
		}
		stage ('Build') {
			steps {
				sh 'mvn clean package'
			}
		}
		stage ('Test') {
			steps {
				sh 'mvn test'
			}
		}
		stage ('Run Application') {
			steps {
				sh 'java -jar target/mavenapp-1.0-SNAPSHOT.jar'
			}
		}
	}
}
}
