pipeline {
    agent any

    stages {
        stage('Compile Stage') {
            steps {
                echo 'Comple Stage starts...'
				withMaven(maven : 'maven_3_5_2'){
				 bat 'mvn clean compile'
				echo 'Comple Stage ends...'
				}
            }
        }
        stage('Testing Stage') {
            steps {
                echo 'Testing Stage starts...'
				withMaven(maven : 'maven_3_5_2'){
				 bat 'mvn test'
				echo 'Testing Stage ends...'
				}
            }
        }
        stage('Install Stage') {
            steps {
                echo 'Install Stage starts...'
				withMaven(maven : 'maven_3_5_2'){
				 bat 'mvn install'
				echo 'Install Stage ends...'
				}
            }
        }
	 stage('Deploy Stage') {
            steps {
                echo 'Install Stage starts...'
				withMaven(maven : 'maven_3_5_2'){
				 bat 'mvn deploy'
				echo 'Deploy Stage ends...'
				}
            }
        }   
        stage('SonarQube Scanner Stage') {
            steps {
                echo 'Deploymnet Stage starts...'
				 bat 'mvn sonar:sonar'
				echo 'Deploymnet Stage ends...'
            }
        }
    
    }
	
}	
}	
