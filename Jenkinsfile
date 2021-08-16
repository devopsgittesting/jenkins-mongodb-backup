pipeline { 
  
   agent any
stage('Deploy to Production') {
            when {
                expression { 
                   return params.ENVIRONMENT == 'PROD'
                }
            }
            steps {
                    sh """
                    echo "deploy to production"
                    """
                }
            }
}}  
