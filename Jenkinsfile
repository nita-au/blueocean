pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '${mvn}/bin/mvn clean package'
        archiveArtifacts 'target/blueocean*.jar'
      }
    }
    stage('Test') {
      steps {
        sh 'echo "test"'
        junit 'target/surefire-reports/*.xml'
      }
    }
  }
  environment {
    mvn = '/opt/apache-maven-3.5.0'
  }
}