node {
   def mvnHome
   def scannerHome
   def dockerHome
   stage('Setup') { 
          
      mvnHome = tool 'maven3.5.2'
      scannerHome = tool 'sonarqube3.0'
      dockerHome = tool 'docker'
      

   }


   stage('Code') {
      git 'https://github.com/HarveyHe/wa_dema_test.git'
   }


   stage('Build') {
      sh "'${mvnHome}/bin/mvn' -f ./demo1/pom.xml -Dmaven.test.failure.ignore clean package"
      sh "'${mvnHome}/bin/mvn' -f ./demo2/pom.xml  -Dmaven.test.failure.ignore clean package"
   }

}