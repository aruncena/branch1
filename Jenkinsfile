pipeline {
    agent any 
    stages {
        stage ('Choose env') {
            steps {
            echo 'welcome to 1st pipleline'
              }
        }
        stage ( 'SCM checkout' ){
        steps {
            git 'https://github.com/aruncena/branch1.git'
            sh 'scp * root@172.31.34.47:/var/www/html/. '
        }    
        }
        stage ('connect to remote server') {
        steps {
          sh "ssh -tt {$DEV} systemctl restart httpd"
            }     
        }
        
   }
}
