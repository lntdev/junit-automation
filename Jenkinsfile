#!groovy


node ('master') {
    timestamps {
        // Create a unique workspace so Jenkins doesn't reuse an existing one
        ws("/mnt/data") {
            stage("Clone Repo") {
                checkout scm
            }
            stage("build dockr images") {
            // sh "sudo docker build -t Myapp1 ."
        } 

    
        }
    } 
}