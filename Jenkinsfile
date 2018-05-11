//pipeline {
//    agent any
//    tools {maven 'maven-curso'}
//    stages{
//        stage ('Build'){
//            steps {bat 'mvn clean package'}
//            post {
//                success {
//                    echo 'Guardando...'
//                    archiveArtifacts artifacts: '**/target/*.war'
//                }
//            }
//        }
//    }
//}

pipeline {
    agent any
    tools {maven 'maven-curso'}
    stages{
        stage ('Build'){
            steps {bat 'mvn clean package'}
            post {
                success {
                    echo 'Guardando...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
        stage ('Paso a pre'){
            steps {
                build job: 'proyecto-deploy'
            }
        }
    }
}
