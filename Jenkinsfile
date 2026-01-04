pipeline {
 agent any

 parameters {
   string(name: 'DEPLOY_ENV', defaultValue: 'devlopment', description: 'Select the target environment')
}

stages{
    stage("checkout"){
     steps {
           sh """
           echo "Checkout done - $PWD"
           echo " Deployment env selected is: $DEPLOY_ENV"
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
