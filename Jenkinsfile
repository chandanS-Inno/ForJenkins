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
                cron(35 09 27 10 11 *)
            }
        }
    }
}
