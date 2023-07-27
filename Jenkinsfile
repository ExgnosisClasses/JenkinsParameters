pipeline {
    agent any
  
    parameters {
        booleanParam(name: "PRODUCTION", defaultValue: false, description: "For triggering Packahe")
        string(name: "AUTHOR", defaultValue: "Rod", trim: true, description: "Code Author")
        choice(name: "TARGET", choices: ["production", "development", "testing"], description: "Build Target")
    }
    stages {
        stage("Build") {
            steps {
                echo "Build stage."
                echo "This is ${params.TARGET} build authored by ${params.AUTHOR}"
            }
        }
        stage("Test") {
            steps {
                echo "Test stage."
            }
        }
        stage("Release") {
            steps {
                echo "Release stage."
                echo "We have a ${params.TARGET} target"
            }
        }
    }
}
    
