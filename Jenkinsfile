pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', credentialsId: 'git_credentials', url: 'https://github.com/Bishwajeetdalai/jenkins-ansible.git'
       }
 }
 stage('Execute Ansible'){
  steps{
     ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, inventory: 'dhost.inv', playbook: 'apache.yml'  
      }
    }
}
}
