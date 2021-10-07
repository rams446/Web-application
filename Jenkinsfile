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

		stage('Build')
		{
			steps
			{
				sh 'mvn package -Dmaven.test.skip'
			}
		}
		
		/*stage('Build Docker Image')
		{
			steps
			{
				sh 'mkdir -p /code/$PROJECT_NAME/$BUILD_NUMBER'
				sh 'sudo cp /var/lib/jenkins/workspace/$PROJECT_NAME/target/addressbook.war /code/$PROJECT_NAME/$BUILD_NUMBER/'
				sh 'sudo cp /var/lib/jenkins/workspace/$PROJECT_NAME/Dockerfile /code/$PROJECT_NAME/$BUILD_NUMBER/'
				sudo docker build -f /code/$PROJECT_NAME/$BUILD_NUMBER/Dockerfile -t iamdevopstrainer/ab-30Sep2021:$BUILD_NUMBER /code/$PROJECT_NAME/$BUILD_NUMBER
			}
		}

		stage('Push Docker Image')
		{
			steps
			{
				sh 'sudo docker push iamdevopstrainer/ab-30Sep2021:$BUILD_NUMBER'
			}
		}

		stage('Update Application')
		{
			steps
			{
				sh 'sudo docker run -itd -P iamdevopstrainer/ab-30Sep2021:$BUILD_NUMBER'
			}
		}*/
		
	}
		
}
