pipeline{
    agent any
    environment{
        ENV_VAR1= 'env var-1 Value '
        ENV_VAR2= 'env var-2 Value '
        ENV_VAR3= 'env var-3 Value '
    }
    stages{
        stage('Build'){
            steps{
                echo 'Learning to build from SCM'
                echo "Value of ENV_VAR1 is: ${ENV_VAR1}"
            }
            
        }
        stage('Test'){
            steps{
                echo 'Learning to test in a multistAge pipeline'
                echo "Value of ENV_VAR2 is: ${ENV_VAR2}"
            }
            
        }
        stage('Deploy'){
            steps{
                echo 'Learning to DEPLOY from MULTI STAGE PIPELINE'
                echo "Value of ENV_VAR3 is: ${ENV_VAR3}"
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
