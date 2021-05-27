pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
            }
        }
		stage('SonarQube Analysis') {
        def mvnHome =  tool name: 'maven3', type: 'maven'
        withSonarQubeEnv('sonarqube123') { 
          sh "${mvnHome}/bin/mvn sonar:sonar"
        }
    }
}
