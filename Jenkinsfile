pipeline{
  agent any
  environment {
  PATH = "{$path}:${getTerraformPath()}"
}

stages{
  stage('terraform init'){
    steps{
      sh 'terraform init'
      sh 'terraform apply -auto-approve'
    }
  }

  }
  }
  def getTerraformPath(){
  tfHome = tool name: 'terraform-0.15', type: 'terraform'
  return tfHome
  }
