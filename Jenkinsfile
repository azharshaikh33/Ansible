pipeline {
    agent { label 'ws' }
    environment {
        SSH_CRED = credentials ('SSH_CRED')
    }
    stages ('Performing the Ansible dryrun') {
        steps {
            sh "env"
            sh "ansible-playbook robot-dryrun.yaml -e COMPONENT=mongodb -e ansible_user=${SSH_CREDENTIALS_usr} -e ansible_password=${SSH_CREDENTIALS_}"
        }
    }
}