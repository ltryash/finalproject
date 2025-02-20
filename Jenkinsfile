pipeline{
  agent any

  stages {
    stage('Code Checkout'){
        steps{
            git 'https://github.com/ltryash/finalproject'
        }
    }

    stage('Deploy'){
        steps{
         script{
          sh'''
           sudo rm -rf /var/www/html/*
           sudo cp -r* /var/www/html/
           sudo chown -R WWW-data:www-data /var/www/html/
           sudo chmod -R 755 /var/www/html
           sudo systemctl restart apache2'''
           
         }
        }
    }
  }
}
   
   



    
