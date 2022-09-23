pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Placeholder'
        bat(script: 'D:\\maven\\apache-maven-3.6.3-bin\\apache-maven-3.6.3\\bin\\mvn -B -DskipTests clean package', returnStdout: true)
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true)
      }
    }

    stage('test') {
      steps {
        bat 'D:\\maven\\apache-maven-3.6.3-bin\\apache-maven-3.6.3\\bin\\mvn  test'
        junit 'target/surefire-reports/*.xml'
      }
    }

    stage('deploy') {
      steps {
        echo 'deployed successfully'
      }
    }

  }
}