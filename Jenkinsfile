pipeline {
    agent {
	label 'node-1'
	}
    tools {
        maven 'maven3.9.3'
    }
    stages {      
        stage('maven build') {
            steps {
                sh 'mvn clean compile'
            }
        }
	stage('maven test') {
            steps {
                sh 'mvn test'
            }
        }
	stage('maven package') {
            steps {
                sh 'mvn package'
            }
        }
	stage('store artifile') {
	   steps{
		archiveArtifacts artifacts: '/home/**/*.jar'
		}
	}
}
}

