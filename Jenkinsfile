pipeline{
    agent any
    
    tools{
        maven 'Maven 3.9.11'
    }
    
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
                        sh 'mvn -v'
               
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
            when{
                branch 'main'
             }
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
