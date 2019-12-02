pipeline {
  agent any
  environment {
    RELEASE_VERSION="${G_GAS_RELEASE_VERSION}"
    COMMSERVER_MINOR_VERSION="${BUILD_NUMBER}"
    COMMSERVER_BUILD_VERSION="${RELEASE_VERSION}.${COMMSERVER_MINOR_VERSION}"
  }
  stages {
    stage('Build') {
      steps {
        withMaven(maven: 'Default') { 
          sh "echo $COMMSERVER_BUILD_VERSION"
        }
      }  
    }    
  }
}
