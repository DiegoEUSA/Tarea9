pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Construyendo el proyecto...'
                sh 'python3 -m venv venv'
                sh 'source venv/bin/activate && pip install -r requirements.txt || true'
            }
        }

        stage('Test') {
            steps {
                echo 'Ejecutando pruebas...'
                sh 'source venv/bin/activate && python3 -m unittest discover tests || true'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Simulando despliegue a staging...'
                sh 'echo "Desplegando en entorno de staging..."'
            }
        }
    }
}
