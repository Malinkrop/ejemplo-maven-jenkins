import groovy.json.JsonSlurperClassic
def jsonParse(def json) {
    new groovy.json.JsonSlurperClassic().parseText(json)
}
pipeline {
    agent any
    stages {
        stage("Paso 1: Saludar"){
            steps {
                script {
                sh "echo 'Hello, World Usach!'"
                }
            }
        }
        stage("Paso 2: Crear Archivo"){
            steps {
                script {
                sh "echo 'Hello, World Usach!!' > hello-devops-usach-.txt"
                }
            }
        }
        stage("Paso 3: Guardar Archivo"){
            steps {
                script {
                sh "echo 'Persisitir Archivo!'"
                }
            }
            post {
                //record the test results and archive the jar file.
                success {
                    archiveArtifacts(artifacts:'**/*.txt', followSymlinks:false)
                }
            }
        }
    }
    post {
        always {
            sh "echo 'fase always executed post'"
        }
        success {
            sh "echo 'fase success'"
        }
        failure {
            sh "echo 'fase failure'"
        }
    }
}
Contraer





Luis Dominguez (ldominguez)
  20:08
https://nksistemas.com/forzar-que-jenkins-siempre-se-vea-en-ingles/#:~:text=Vamos%20a%20Administrar%20Jenk[…]0de%20ingl%C3%A9s%20tipeamos%3A%20en_US
NKSistemasNKSistemas
Forzar que Jenkins siempre se vea en inglés
Por defecto Jenkins toma el idioma de nuestro navegador, algo que suelo cambiar, pero a algunos solo les interesa cambiar el idioma de la herramienta, es bastante simple, usaremos un plugin y verem…
15 jul. (26 kB)
https://nksistemas.com/forzar-que-jenkins-siempre-se-vea-en-ingles/#:~:text=Vamos%20a%20Administrar%20Jenkins%20%3E%20Configuraci%C3%B3n,caso%20de%20ingl%C3%A9s%20tipeamos%3A%20en_US

Nuevo


Roger Reyes Miranda
  20:09
Pipeline del tipo Pipeline
pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Step 1') {
            steps {
                echo 'Step 1'
                sh "uname"
            }
        }
        stage('Step 2') {
            steps {
                echo 'Step 2'
                sh "java --version"
            }
        }
        stage('Step 3') {
            steps {
                echo 'Step 3'
                sh "ps -aux"
            }
        }
        stage('Step 4') {
            steps {
                echo 'Step 4'
                sh "pwd"
            }
        }
        stage('Good Bye') {
            steps {
                echo 'Good Bye Usach Ceres'
            }
        }
    }
}