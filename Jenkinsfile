pipeline {
    agent any
    tools {
        terraform 'terraform'
    }
    
     environment {
        TF_HOME = tool('terraform')
        TF_INPUT = "0"
        TF_IN_AUTOMATION = "TRUE"
        TF_LOG = "WARN"
        PATH = "$TF_HOME:$PATH"
    }
    
    stages{
        stage('Terraform Init'){
            steps{
                 sh 'terraform --version'
                 sh 'pwd'
                 sh label: '', script: 'terraform init'
                
                    
                }
            }
        }
    }