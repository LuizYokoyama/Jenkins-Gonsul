node {

    stage('Clone') {
        git credentialsId: 'ssh-git', url: 'git@github.com:LuizYokoyama/prv-test.git'
    }

    stage('Run Gonsul') {
    sh 'tree '
        sh './config/gonsul --consul-url=http://0.0.0.0:8500 --repo-root=./ --strategy=ONCE --log-level=DEBUG --input-ext=json,txt,ini,yaml,yml,properties --allow-deletes=true --repo-base-path=/config/'
    }

}