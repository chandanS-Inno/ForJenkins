pipeline{
    agent any
    stages {
        stage("Compile") {
            steps {
                //pip install requirements.txt
                echo "Python compile done"
            }
        }
        stage("Unit test") {
            steps {
                sh "python test_calc.py"
            }
        }
        stage("Schedule build"){
            triggers{
                cron(30 8 10 11 *)
            }
        }
    }
}
