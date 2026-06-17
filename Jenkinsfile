pipeline {
	agent any
	
	tools {
		gradle 'gradle'
		jdk 'jdk'
	}
	
	stages {
		stage('Checkout') {
			steps {
				git branch:'main',
				url:'https://github.com/1bi23cs254/Gradle-AppPract1.git'
			}
		}
		
		stage('Build') {
			steps {
				sh 'gradle build'
			}
		}
		
		stage('Test') {
			steps {
				sh 'gradle test'
			}
		}
		
		stage('Run') {
			steps {
				sh 'gradle run'
			}
		}
	}
	
	post {
		success{
			echo 'Build and deployed successfully'
		}
		
		failure{
			echo 'build failed'
		}
	}
}
