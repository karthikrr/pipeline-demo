pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Placeholder'
        sh 'mvn -B -DskipTests clean package'
      }
    }

    stage('test') {
      steps {
        sh '''echo test starting
echo test completed'''
        sh 'mvn test'
        junit 'target/surefire-reports/*.xml'
      }
    }

    stage('deploy') {
      steps {
        sh 'echo deployed successfully'
      }
    }

  }
}