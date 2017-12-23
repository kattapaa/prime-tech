node {
   stage('Code Checkout') { 
     git credentialsId: 'github-credential', url: 'https://github.com/manee2k6/DKPractises.git' 
   }
   stage('Build') {
     withMaven(jdk: 'JDK-1.8.0.151', maven: 'Maven-3.5.2') {
      sh 'mvn clean compile'
      }
     
   }
   stage('Sonar Code Coverage') {
           
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
