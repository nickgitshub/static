pipeline {
  agent any
  stages {
    stage(‘UploadtoAWS’) {
        steps {
          withAWS(region:’us-west-1’,credentials:’aws-static’) {
            sh 'echo "Uploading content with AWS creds"'
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’udacity-p3-bucket’)
          }
        }
      }
    }
  }
