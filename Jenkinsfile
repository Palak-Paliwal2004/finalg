pipeline {
	agent any
	tools{
		gradle 'gradle'
		jdk 'JDK'
	}
	stages{
		stage('Checkout')
		{
			steps{
				git branch: 'master' , url: 'https://github.com/Palak-Paliwal2004/finalg.git'
			}
		}
		stage('Build')
		{
			steps{
				sh 'gradle build'
			}
		}
		stage('Test')
		{
			steps{
				sh 'gradle Test'
			}
		}
		stage('Running application')
		{
			steps{
				sh 'gradle run'
			}
		}
	}
	post{
	success{
		echo 'Build successfull!'
	}
	failure{
		echo 'Build failed'
	}
	}
}
