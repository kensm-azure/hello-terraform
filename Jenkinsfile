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
                 sh label: '', script: 'terraform init'
                 }
            }
        stage('Terraform Validate'){
            steps{
                sh 'terraform validate'
                 }
           }
        stage('Terraform Plan'){
            steps{
                sh 'terraform plan'
                 }
           }
        stage('Terraform Apply'){
            steps{
                sh 'terraform Apply'
                 }
           }
        stage('Terraform Show'){
            steps{
                sh 'terraform Show'
                 }
           }
        }
    }
