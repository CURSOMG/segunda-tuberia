pipeline {    
    agent any     
    tools {    maven 'maven-curso'  }    
    stages{        
        stage ('Build'){            
            steps {        bat 'mvn clean package'      }          
            post {               
                success {                   
                    echo 'Guardando...'                   
                    archiveArtifacts artifacts: '**/target/*.war'              
                }          
            }      
        }  
    }
}
