pipeline { 
  
   agent any
  
   stages {
  
stage('Deploy to Production') {
            when {
                expression { 
                   return params.ENVIRONMENT == 'PROD'
                }
            }
            steps {
                   script {
			echo 'Using remote command over ssh'
			sh 'echo "Today is:" date'
			echo '*** Executing remote commands ***'
	 		sh '''#!/bin/bash
				ssh root@192.168.0.108 >> ENDSSH
			date  
			mongodump --out /root/mongobackup_16082021
'''
                }
            }
}
}
}
