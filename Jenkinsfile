pipeline
{
  agent any
  stages
  {
    stage('Git checkout')
    {
      steps
      {
        echo "Checking out from Git Repo";
      }
    }
    
    stage('Run test')
    {
      steps
      {
        echo "Running the tests";
        javac TestClass.java
      }
    }
    
    stage('Success stage')
    {
      steps
      {
        echo "Test finished successfully";
      }
    }
  }
  
  post
	{
		always
		{
			echo 'This will always run'
		}
		success 
		{
			echo 'THis will run only if successfull'
		}
		failure
		{
			echo 'This will run only if failed'
		}
		unstable
		{
			echo 'Only if the run was marked as unstable'
		}
		changed
		{
			echo 'This will run only if the state of the Pipeline has changed'
			echo 'FOr example, if the Pipeline was previously failing but is now successfull'
		}
	}
}
