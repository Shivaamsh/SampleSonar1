pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Hello world!' 
            }
        }
		stage('Stage 2') {
            steps {
                echo 'How are you' 
            }
        }
		stage('Stage 3') {
            steps {
                echo 'Hope you all are good' 
            }
        }
    }
}
