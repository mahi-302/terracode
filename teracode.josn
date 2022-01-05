node('main'){
    stage('pulling'){
       git branch: 'main', url: 'https://github.com/mahi-302/module1.git'
        sh "ls"
    }
    stage('lb'){
         sh "terraform init"
        sh "terraform plan"
        sh "terraform apply -auto-approve"
    }
    stage('pushing data'){
        sh "git add terraform.tfstate"
        sh "git commit -m 'terraform'"
        sh "git remote set-url origin https://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@github.com/mahi-302/module1.git"
        sh "git push --set-upstream origin main"
       }
    }
