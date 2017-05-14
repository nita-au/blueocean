pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '${mvn}/bin/mvn clean package'
      }
    }
    stage('Test') {
      steps {
        sh 'echo "test"'
      }
    }
  }
  environment {
    mvn = '/opt/apache-maven-3.5.0'
  }
}