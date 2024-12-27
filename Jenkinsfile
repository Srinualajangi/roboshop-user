@Library('Jenkins-shared-library') _

// create variable of map type and set the values
def configMap = [
    component: "user",
    project: "roboshop"
]

echo "test:"

if (env.BRANCH_NAME != null && !env.BRANCH_NAME.equalsIgnoreCase('main')) {
    nodeJSEKSPipeline(configMap)
} else {
    echo "Proceed with CR or NON-PROD pipeline"
}

