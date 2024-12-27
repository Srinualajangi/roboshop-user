@Library('Jenkins-shared-library') _

// create variable of map type and set the values
def configMap = [
    component: "user",
    project: "roboshop"
]

echo "test:"

// Manually set the branch name for testing
env.BRANCH_NAME = env.BRANCH_NAME ?: env.GIT_BRANCH ?: 'feature-branch' // Replace with the actual branch name you are testing with

echo "Branch name: ${env.BRANCH_NAME}"

if (env.BRANCH_NAME != null) {
    if (!env.BRANCH_NAME.equalsIgnoreCase('main')) {
        echo "Calling nodeJSEKSPipeline"
        nodeJSEKSPipeline(configMap)
    } else {
        echo "Proceed with CR or NON-PROD pipeline"
    }
} else {
    echo "BRANCH_NAME is null"
}
