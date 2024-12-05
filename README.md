# yaml-files



## 
pipeline{
    agent {
        label 'demo'
    }
    
    stages{
        stage("checkout"){
            steps{
                git branch: "main", url: "https://github.com/veer-H/postgress.git"
            }
        }
        stage(" build"){
            steps{
                sh "docker compose up -d"
            }
        }
    }
        
    
}
