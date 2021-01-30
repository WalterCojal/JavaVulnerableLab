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
        sh 'cp target/*.war /Users/user00381/Desktop/JavaVulnerableLab'
      }
    }

  }
  tools {
    maven 'maven3.6.3'
  }
}