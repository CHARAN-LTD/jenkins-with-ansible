pipeline {
  agent { 
  label 'ansible'
  }
  
  environment {
   AWS_EC2_PRIVATE_KEY=credentials('ec2-private-key') 
  }
  
  stages {
    
    //Get the Code from GitHub Repo
    stage('CheckOutCode'){
      steps{
        git credentialsId: 'e287043b-d1b4-4c15-a128-99c791c6f7f6', url: 'https://github.com/CHARAN-LTD/jenkins-with-ansible.git'
      }
    }
     
    //Run the playbook
    /*stage('RunPlaybook') {
      steps {
        sh "ansible-playbook -i inventory/walmart.hosts --private-key=$AWS_EC2_PRIVATE_KEY playbooks/installTomcat.yml"
      }
    }*/
  
  }//stages closing
}//pipeline closing
