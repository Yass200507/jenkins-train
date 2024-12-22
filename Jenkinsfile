pipeline{
    agent any
    stages{
        stage("build jar file"){
            steps{
                script{
                        docker.image('maven').inside('-v $HOME/.m2:/root/.m2') {
                            sh 'mvn package'
                        }
                }
            }   
        }
        stage("build docker image"){
            steps{
                script{
                    sh "docker build -t firsttrial:0.0 ."
                }
            }
        }
    }
}