pipeline{
  agent any
  environment {
  PATH = "${PATH}:${getTerraformPath()}"
}
  stages{
    stage('Git Checkout'){
      steps{
        git credentialsId: 'd5075fae-5d58-43db-bf5f-3bdb617dd015', url: 'https://github.com/Krishnadev3699/hello-world'
      }
    }
    stage('terraform init'){
      steps{
        sh 'terraform init'
      }
    }
    stage('terraform apply'){
      steps{
        sh 'install_jenkins'
      }
    }
  }
  }
def getTerraformPath(){
  def tfHome = tool name: 'Terraform-12', type: 'terraform'
  return tfHome
}
