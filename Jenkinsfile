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

    stage ('Deploying to Docker '){
      steps {
        echo "Opening Docker"

        withCredentials([string(credentialsId: 'docker-pwd', variable: 'Dine')]) {
          bat 'docker login -u dhineshdine -p $(Dine)'

          bat 'docker-compose -f mongo.yaml up -d '
          
}
        
      }
    }
  }
  
}
