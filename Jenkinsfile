pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn -f javademos/source/java/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war', fingerprint: true)
        sh '''mkdir /home/azureuser/buildoutput/${BUILD_NUMBER}
cp **/target/*.war /home/azureuser/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}