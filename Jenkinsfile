pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello World'
        sh '''pwd
mvn -Dmaven.test.failure.ignore=true clean package'''
      }
    }

    stage('Deliver') {
      steps {
        sh '''pwd
cp target/*.war /var/lib/tomcat9/webapps'''
      }
    }

  }
}