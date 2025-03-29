pipeline{
 
  agent any

  tools{
   jdk 'JAVA_HOME'
    maven "maven"
  }

  stages{

    stage('Checkout'){
       steps{
         git branch:'master',
         url: 'https://github.com/Adarsh765-jpg/Devops-test-.git'
       }
    }

     stage('Build'){

       steps{
          bat 'mvn -B -DskipTests clean package'
          }
     }

     stage('Test'){
       steps{
         bat 'mvn test'
       }
     }

     stage('Deliver'){
       steps{
         scripts{
              bat './scripts/deliver.bat'
           }
       }
     }

  }

}





