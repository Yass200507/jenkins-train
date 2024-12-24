pipeline{
    agent any
    stages{
        stage("build jar file"){
            steps{
                script{
                        sh 'mvn clean install'
                        echo "building jar file"
                }
            }   
        }
        stage("build docker image"){
            steps{
                script{
                    sh "sudo docker build -t firsttrial:0.0 ."
                    echo "building docker image,"
                }
            }
        }
    }
}