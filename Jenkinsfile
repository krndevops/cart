@Library('central-library') _

node('workstation') {
    if (env.BRANCH_NAME == 'main') {
        echo 'Nothing to Do'

    }
    else if (env.TAG_NAME =~ '.*') {
        sast()
        sca()
        secretDetection()
        artifactProduce()
    }
    else if (env.BRANCH_NAME =~ '.*') {
        unitTests()
        integrationTests()
        codeQuality()
    }
}
