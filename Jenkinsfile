pipeline{
    agent any
    stages{
        stage("GetProject"){
            steps {
                git branch:'main', url:'https://github.com/Chadlikouider/CT5171_testmaven.git'
            }
        }
        stage('build'){
            steps{
                sh 'mvn clean:clean'
                sh 'mvn dependency:copy-dependencies'
                sh 'mvn compiler:compile'
            }
        }
        
        stage('Exec'){
            steps{
                sh 'mvn exec:java'
            }
        }
    }
}
