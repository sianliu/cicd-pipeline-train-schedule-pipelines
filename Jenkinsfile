pipeline {
	agent any
	stages {
		stage ('Build') {
			steps {
				echo 'Running build automation'
				sh './gradlew build --no-daemon'	# background process to speed up build 
				archiveArtifact artifacts: 'dist/trainSchedule.zip'
			}
		}
	}
}