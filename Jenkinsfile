pipeline{
  agent { label "${LABEL_NAME}"}

  environment { 
    IMAGE_NAME = netweb
    IMAGE_TAG = "${BUILD_NUMBER}"
    CONTAINER_NAME = net1
  }

  stages {
    stage('CHECKOUT'){
      steps{
      git url: '', branch:"main"
    }    
   }
    stage('BUILD') {
      steps{
        sh "docker build -t $IMAGE_NAME:$IMAGE_TAG  . "
      }  
    }
    stage('DEPLOY') {
      steps{
        sh "docker build -t $IMAGE_NAME:$IMAGE_TAG  . "
      }  
    }


}
