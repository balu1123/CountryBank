pipeline{
   agent any
   tools{
    maven 'maven'
   } 

   stages{
    stage("Git Checkout"){
      steps{
        script{
          git changelog: false, poll: false, url: 'https://github.com/balu1123/CountryBank.git'  
        }
      }  
    }

    stage("Unit testing"){
      steps{
        sh 'mvn test'
      }  
    }
   }
}