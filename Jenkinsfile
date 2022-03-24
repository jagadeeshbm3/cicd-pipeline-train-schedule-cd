pipeline 
{
        stages 
        {
               stage('staging')
               {
                     steps
                     {
                        echo 'building the codes from the git'
                      }
                }
                stage('developer-branch-stuff')
                {
                   when
                   {
                       branch 'staging'
                   }
                   steps
                   {
                      echo 'run this stage - only if the branch = staging branch'
                   }
                }
        stage('Deliver for development') 
        {
            when 
            {
                branch 'developer'
            }
            steps 
            {
                sh 'your_filename_along_with_your_filepath'
                input message: 'shall we deploy it? (Click "Proceed" to continue)'
            }
        }
        stage('Deploy for production') 
        {
            when
            {
                branch 'developer'
            }
            steps
            {
                sh 'your_filename_along_with_your_filepath'
                input message: 'shall we proceed to production? (Click "Proceed" to continue)'
            }
        }
    }
}
