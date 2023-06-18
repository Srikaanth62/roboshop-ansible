pipeline {
 agent {
  node {
   label 'workstation'
  }
 }
 parameters {
         string(name: 'component', defaultValue: '', description: 'component name')
         choice(name: 'env', choices: ['dev', 'prod'], description: 'Pick environment')
     }
 stages {
  stage ('ansible') {
   steps {
    sh 'ansible-playbook -i ${component}-${env}.srikaanth62.online, roboshop.yml -e ansible_user=root -e ansible_password=DevOps321 -e env=${env} -e role_name=${component}'
   }
  }
 }
 post {
  always {
   clearWs()
  }
 }
}