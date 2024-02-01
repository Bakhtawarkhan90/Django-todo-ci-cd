pipeline{
    agent any
    stages{
        stage ("clone"){
            steps{
                echo "cloning the code"
                git url: "https://github.com/Bakhtawarkhan90/django-todo-cicd.git", branch: "develop"
                      }

        }
        stage ("Build"){
            steps{
                echo "Building image"
                sh "docker build . -t note-app"
            }
            
         }
         stage ("contanarization"){
            steps{
                echo "running the container"
                sh "docker run -d -p 8000:8000 note-app"
            }
            
         }
     
    }   
}
