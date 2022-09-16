pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Placeholder'
        bat(script: 'mvn -B -DskipTests clean package', returnStdout: true)
      }
    }

    stage('test') {
      steps {
        bat 'mvn test'
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