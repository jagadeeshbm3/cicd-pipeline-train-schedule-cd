#!/usr/bin/groovy

@Library('https://github.com/lachie83/jenkins-pipeline@master')

def pipeline = new io.estrado.Pipeline()
def cloud = pipeline.getCloud(env.BRANCH_NAME)
def label = pipeline.getPodLabel(cloud)

// deploy only the staging branch
if (env.BRANCH_NAME == 'staging') {
    stage ('deploy to k8s staging') {
      //Deploy to staging
    }
}
// deploy only the master branch
if (env.BRANCH_NAME == 'master') {
    stage ('deploy to k8s production') {
      //Deploy to production
    }
}
