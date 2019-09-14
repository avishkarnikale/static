pipeline {
  agent any 
  stages {
    stage('Upload index file to AWS bucket') {
                steps {
                    withAWS(region:'ap-south-1',credentials:'aws-static') {
                        s3Upload(file:'index.html', bucket:'udacity-cdend-avishkar-project3', path:'index.html')
                    }
                    sh 'curl -fsS https://udacity-cdend-avishkar-project3.s3.ap-south-1.amazonaws.com/index.html > /dev/null'
                  }

            }
  }
}
