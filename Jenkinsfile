node {
   stage('Checking out code') { 
     git credentialsId: 'github-credential', url: 'https://github.com/manee2k6/DKPractises.git' 
   }
   stage('Maven Build') {
     withMaven(jdk: 'OpenJDK1.8', maven: 'maven3.5.2') {
      sh 'mvn clean compile'
      }
     
   }
      
   stage('Test') {
       withMaven(jdk: 'JDK-1.8.0.151', maven: 'Maven-3.5.2') {
      sh 'mvn test'
      }
   }
   stage('Results') {
       echo 'Results are generated'
     
   }
   stage('Archive') {
       echo 'Archived Test Reports'
   
   }
   stage('Deploy') {
       echo 'Deployed the artifacts'
     
   }
}
