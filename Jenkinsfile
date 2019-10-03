pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        sh './gradlew build --no-daemon'    # background process to speed up builds and works beautifully in a local devel environment but not a pipeline
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
    stage ('Test') {}
  }
}
