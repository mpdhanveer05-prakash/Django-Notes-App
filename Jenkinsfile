@Library('shared') _
pipeline{
    agent { label "alpha" }
    stages{
        stage("Code"){
            steps{
                script{
                code("https://github.com/mpdhanveer05-prakash/Django-notesapp.git","main")
                }
            }
        }
        stage("Build"){
            steps{
                script{
                build("notes-app", "latest", "mpdhanveer05")
                }
            }
        }
        stage("Push"){
            steps{
               script{
                push("notes-app", "latest", "mpdhanveer05")   
               }
            }
        }
        stage("Deploy"){
            steps{
                echo "This is Deploying the code"
                compose()
        
        }
    }
    }
}
