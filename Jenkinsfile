pipeline 
{
    agent any

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                bat 'mvn clean'
            }
        }

        stage('Test') 
        {
            steps 
            {
                bat 'mvm test'
            }
        }

      
    }

    post
    {

    	always
    	{
    		 archiveArtifacts artifacts:'**/*.jsp,**/*.war,**/*.xml',followSymlinks:false
    	}

    }
}
