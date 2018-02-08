pipeline {
	
	agent any
	
	stages {
		         stage ('clean stage') {
			steps {
				bat 'mvn clean'
			   }
		        }
		  
		stage ('compile stage') {
			steps {
			bat 'mvn compile'
			}
		}
		
		stage ('Installing') {
			steps {
				bat 'mvn install'
		}
	}
	
}
}
