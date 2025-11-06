pipeline {

  agent any 

  tools {
  nodejs 'NodeJS_Home'
}


  stages {
    stage('Building Stage'){
      steps {
         echo "building "
        dir('app'){
        bat 'npm install'
        }
      echo "build successfullly "
      }
    }
  }
  
}
