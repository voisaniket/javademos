pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn -f javademos/source/java/ssgsems/ -B -DskipTests clean package'
      }
    }

  }
}