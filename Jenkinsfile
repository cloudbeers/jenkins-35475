def teamName = 'cloudbeers'
def repoName = 'jenkins-35475'

stage 'Checkout'
node {
    checkout scm;
}
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
            name: 'upstream',
            url: "https://github.com/${teamName}/${repoName}.git"
        ]]
    ])
}
node {
    checkout([
        $class: 'GitSCM',
        branches: [[name: env.BRANCH_NAME]],
        browser: [
            $class: 'GithubWeb',
            repoUrl: "https://github.com/${teamName}/jenkins-37028.git"
        ],
        doGenerateSubmoduleConfigurations: false,
        extensions: [[$class: 'CleanBeforeCheckout']],
        submoduleCfg: [],
        userRemoteConfigs: [[
            name: 'upstream',
            url: "https://github.com/${teamName}/jenkins-37028.git"
        ]]
    ])
}