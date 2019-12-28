pipeline {
  agent any
  stages {
    stage(‘Upload to AWS’) {
        steps {
          withAWS(region:’us-west-1’,credentials:’aws-static’) {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’udacity-p3-bucket’)
          }
        }
      }
    }
  }
