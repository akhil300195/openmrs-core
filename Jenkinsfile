node {

stage('SCM') {
    // git clone 
     git 'https://github.com/openmrs/openmrs-core.git'
     
 }

stage('Build the packages') {
    // mvn package
     sh 'mvn package'
 }

stage ('Archival') {
     // archiving artifacts
      archive 'target/*.jar'
 }

stage('Publish Test Results') {
    // Test results
     junit 'target/surefire-reports/*.xml'
 }

}
