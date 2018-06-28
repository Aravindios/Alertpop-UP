env.PATH = '/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Applications/Server.app/Contents/ServerRoot/usr/bin:/Applications/Server.app/Contents/ServerRoot/usr/sbin'
env.HOME = '/Users/iosbuilds'
env.USER = 'iosbuilds'
// backwards compat with old branch variable
env.GIT_BRANCH = env.BRANCH_NAME

node {
    stage('Checkout/Build/Test') {
        // Checkout files.
        checkout([
            $class: 'GitSCM',
            branches: [[name: 'master']],
            doGenerateSubmoduleConfigurations: false,
            extensions: [], submoduleCfg: [],
            userRemoteConfigs: [[
                name: 'hannatest',
                url: 'https://github.com/Aravindios/Alertpop-UP'
            ]]
        ])
 //   sh "brew cask install fastlane"
 //    sh "export LC_ALL=en_US.UTF-8"
 //    sh "export LANG=en_US.UTF-8"   
//     sh "bundle exec fastlane beta" 
   //  sh "fastlane init"   
   //  sh "fastlane beta"
        
 //   sh 'sonar-scanner -Dsonar.projectKey=Alertpop-UP -Dsonar.sources=. -Dsonar.host.url=http://localhost:6363 -Dsonar.login=02933fa7063af5473698c298c014cc3b4b50f9f4'
        
         sh 'sonar-scanner'

    }
}
