pipeline {
 agent any

 parameters {
   string(name: 'DEPLOY_ENV', defaultValue: 'devlopment', description: 'Select the target environment')
}

stage("checkout"){
  when {
                // Execute this stage if the ENVIRONMENT parameter is 'development'
                expression { 
                     return params.DEPLOY_ENV == 'devlopment' 
                }
          }
}
     steps {
           sh """
           echo "Checkout done - $PWD"
           echo "DEPOLYMENT ENV SELECTED - $DEPLOY_ENV"
           ls -l
           """
      }
   }
   stage("Building the application"){
     steps {
         sh """
           echo "========Building Java Application============"
           mvn clean package
           echo "======Building Java Application completed====="
         """      
      }
   }

       
        
    
          


} // end of stages

} // end of pipeline
