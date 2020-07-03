pipeline {
    agent any
    tools { 
        maven 'Maven 3.6.3' 
        jdk 'Java jdk 11.0.7' 
    }
	
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Maven 3.6.3') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Maven 3.6.3') {
                    bat 'mvn test'
                }
            }
        }


        stage ('package Stage') {
            steps {
                withMaven(maven : 'Maven 3.6.3') {
                    bat 'mvn package'
                }
            }
        }
    }
}