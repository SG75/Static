pipeline {
    agent any
    stages {
        stage('Upload to AWS'){
            steps {
                    withAWS(credentials: 'aws-static', region: 'ap-southeast-1') {
                        s3Upload bucket: 'arn:aws:s3:::guru-c3-jenkins', file: 'index.html'                                                 
                                steps {  
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