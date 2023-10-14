pipeline {
  agent { label 'workstation' }

   options {
     ansiColor('xterm')
   }

  stages {

    stage('Download Dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Code Quality') {
      steps {
        sh 'sonar-scanner -Dsonar.host.url=http://172.31.41.26:9000 -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=backend -Dsonar.qualitygate.wait=true'
      }
    }

    stage('Unit Test') {
      steps {
        echo 'CI'
      }
    }

    stage('Release') {
      steps {
        echo 'CI'
      }
    }

  }
}

/////