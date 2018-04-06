pipeline {
    agent any
    tools{
    	maven 'maven-3.3.9'
    	jdk 'jdk1.8.0_152'
    }
    stages {
    	stage('check out') {            
            steps {                
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'a923605e-c0ed-435f-af9c-0d56281e3b4e', url: 'https://github.com/githubshenyuan/devops-demo.git']]])
            }        
        }
        stage('Build') {            
            steps {    
                sh 'mvn clean package -Dmaven.test.skip=true'
            }        
        }        
        stage('Test') {            
            steps {                
                echo 'hhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhhnnhhhhh'            
            }        
        }  
    }
 
  
}

