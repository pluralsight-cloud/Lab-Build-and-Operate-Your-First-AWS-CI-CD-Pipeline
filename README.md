# Status Board

A small internal status page for the product team, deployed to Amazon EC2 through an AWS CodePipeline you build in the lab.

## Contents

- `index.html` and `styles.css`: the status board site.
- `buildspec.yml`: the AWS CodeBuild specification that validates and packages the site.
- `appspec.yml`: the AWS CodeDeploy specification that places the site on the web server and restarts it.
- `scripts/`: deployment lifecycle scripts run by the CodeDeploy agent.

## How it deploys

Every commit to the default branch triggers the pipeline. CodeBuild validates and packages the site, and CodeDeploy releases the package to the web server. Open the instance address from the lab page to see the deployed release.
