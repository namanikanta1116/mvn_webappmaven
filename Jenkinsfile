pipeline {
	agent any
	triggers
	       {
            pollSCM('* * * * *')
           }
	stages {
		stage ('Git-Checkout')
		{
			steps
			{
			    echo "Accessing bat files from github repo"
			    git 'https://github.com/namanikanta1116/mvn_webappmaven.git'
			}
		}
		stage ('Unit Test')
		{
		  steps
		  {
		      bat 'mvn validate'
		  }
		}
		stage ('compile')
		{
		  steps
		  {
		      bat 'mvn compile'
		  }
		}
		stage ('Test')
		{
		  steps
		  {
		      bat 'mvn test'
		  }
		}
		stage ('install')
		{
		  steps
		  {
		      bat 'mvn install'
		  }
		}
	}
}
