pipeline {
    agent any
    
    stages{
        stage('Code'){
            steps {
                git url: 'git@github.com:sundayebosele/node-todo-cicd.git', branch: 'working'
            }
        }
        stage('Build and Test'){
            steps {
                sh 'docker build . -t sandima/springnodejs:v5' 
            }
        }
        stage('Login and Push Image'){
            steps {
                echo 'logging in to docker hub and pushing image..'
                    sh "docker push sandima/springnodejs:v5"
                }
            }
        }
    }
