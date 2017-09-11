#!/usr/bin/groovy
@Library('github.com/fabric8io/fabric8-pipeline-library@master')
def dummy
clientsNode {
  ws {
    checkout scm
    if (utils.isCI()){
      echo 'no CI enabled'
    } else if (utils.isCD()){
      npmUpdateOrganisationDependencies{
        organisation = 'fabric8-ui'
      }
    }
  }
}
