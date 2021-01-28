pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello World'
        sh 'pwd'
        sh 'mvn -Dmaven.test.failure.ignore=true clean package'
      }
    }

    stage('Deliver') {
      steps {
        sh 'pwd'
        sh 'cp target/*.war /var/lib/tomcat9/webapps'
      }
    }

  }
}
