pipeline{
    agent any
    
    stages{
        stage('Parallel Stage')
        {
            parallel
            {
                
                stage('Build')
                {
                    steps
                    {
                        echo 'Learning to build from SCM'
               
                    }
            
                } 
                stage('Test')
                {
                    steps
                    {
                        echo 'Learning to test in a multistAge pipeline'
                
                    }
            
                }
            } 
        }
        
       
        stage('Deploy'){
            steps{
                echo 'Learning to DEPLOY from MULTI STAGE PIPELINE'
              
            }
            
        }
    }
    post{
        always{
            echo 'This will always execute after the stages are done'
        }
        success{
            echo 'This will execute only if the pipeline is successful'
        }
        failure{
            echo 'This will execute only if the pipeline fails'
        }
    }
}
