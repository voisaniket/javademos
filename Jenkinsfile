pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn -f javademos/source/java/ssgsems/ -B -DskipTests clean package'
      }
    }

    stage('') {
      steps {
        archiveArtifacts(fingerprint: true, artifacts: '**/target/*.war')
      }
    }

  }
}