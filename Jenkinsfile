pipeline {
    agent any
    stages {
        stage('Upload to AWS.'){
            steps {
                withAWS(region:'ap-southeast-1', credentials:'AKIAR4ZVDGTGZGZOIIBF') {
                  s3Upload(file:'index.html', bucket:'arn:aws:s3:::guru-c3-jenkins'){
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
                       }
              }
           }
       }
    }
}