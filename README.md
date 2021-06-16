# gitops_operator_deployment
Tech Preview of the gitops operator doe not include native Oauth from openshift. Edit the sub for the appropriate Dex changes and run the batch job included. 

to note, RBAC changes need to take place at the Gitops level and if access to additional namespaces is needed, the service account will need additional privileges. 

subscription object mod:
spec:
  config:
    env:
    - name: DISABLE_DEX
      Value: "false"

