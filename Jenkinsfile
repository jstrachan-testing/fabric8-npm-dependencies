#!/usr/bin/groovy
@Library('github.com/fabric8io/fabric8-pipeline-library@master')
def dummy
clientsNode {
  ws {
    checkout scm
      npmUpdateOrganisationDependencies{
        organisation = 'fabric8io'
        repos = 'fabric8-ui,fabric8-planner'
      }
      npmUpdateOrganisationDependencies{
        organisation = 'fabric8-ui'
      }
  }
}
