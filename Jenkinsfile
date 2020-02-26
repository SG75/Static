pipeline {
    agent any
    stages {
        stage('Upload to AWS'){
            steps {
                withAWS(credentials: 'aws-static', region: 'ap-southeast-1') {
                    sh 'echo "Uploading from github with AWS credentials"'
                        s3Upload(bucket: 'guru-c3-jenkins', file: 'index.html')                                                 
                               
                       
                    }  
                     
              
           }
       }
    }
}