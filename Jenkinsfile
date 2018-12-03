pipeline {
	agent {
		docker {
			image "python:3.7.1"
		}
	}
	stages {
		stage("Test") {
			steps {
				sh "python -c 'import os; print(os.urandom(20))'"
				sh 'echo "Hello, World!"'
			}
		}
	}
	post {
		always {
			echo "This will always run"
		}
		success {
			echo "Successful"
		}
		failure {
			echo "Failured"
		}
		changed {
			echo "Pipeline state change"
		}
	}
}
