def teamName = 'cloudbeers'
def repoName = 'jenkins-35475'

stage 'Checkout'
node {
    checkout([
        $class: 'GitSCM',
        branches: [[name: env.BRANCH_NAME]],
        browser: [
            $class: 'GithubWeb',
            repoUrl: "https://github.com/${teamName}/${repoName}.git"
        ],
        doGenerateSubmoduleConfigurations: false,
        extensions: [[$class: 'CleanBeforeCheckout']],
        submoduleCfg: [],
        userRemoteConfigs: [[
            name: 'origin',
            url: "https://github.com/${teamName}/${repoName}.git"
        ]]
    ])
}