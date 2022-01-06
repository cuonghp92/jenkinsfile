pipeline{
  agent any
  environment {
  PATH = "{$path}:${getTerraformPath()}"
}

stages{
  stage('terraform init'){
    steps{
      sh returnStatus: true, script: 'terraform workspace new dev test'
      sh 'terraform init'
      sh 'terraform apply -auto-approve'
    }
  }

  }
  }
  def getTerraformPath(){
  tfHome = tool name: 'terraform-0.15.4', type: 'terraform'
  return tfHome
  }
