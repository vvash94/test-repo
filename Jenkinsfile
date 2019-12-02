pipeline {
  agent any
  environment {
    RELEASE_VERSION="5.0.0"
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
