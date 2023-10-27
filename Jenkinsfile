import groovy.json.JsonSlurperClassic
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Read and Print JSON') {
            steps {
                script {
                    
                    def jsonData = readFile(file: 'data.json')
                    def jsonSlurper = new JsonSlurperClassic()
                    def parsedData = jsonSlurper.parseText(jsonData)
                    echo "JSON Data:"
                    echo "Name: ${parsedData.name}"
                    echo "Email: ${parsedData.email}"
                    echo "Age: ${parsedData.age}"
                    echo "City: ${parsedData.city}"
                }
            }
        }
    }
}
