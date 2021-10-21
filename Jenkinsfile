pipeline
{
	agent any
	stages
	{
		stage('Checkout')
		{
			steps
			{
				git 'https://github.com/rams446/demo-java.git'
			}
		}
		
		stage('Compile')
		{
			steps
			{
				sh 'mvn compile'
			}
		}
		
		
		stage('Test')
		{
			steps
			{
				sh 'mvn test'
			}
		}
		
		

		stage('Build')
		{
			steps
			{
				sh 'mvn build'
			}
		}
	}
}
		
