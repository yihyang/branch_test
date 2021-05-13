# Branch Test

Sometimes when we work in a big team, we will have features compromised separate set of changes pointing to a same development environment.

Usually the changes that we make will need to be deployed separately into production / QA environment. However if we all merge it back to same environment branch, it will be quite challenging if we need to launch the features separately.

Therefore the proposed idea will be create a different set of epic branches which will act as anchor for the changes.
The new changes will be pushed to the epic branches and once the epic branches are completed it can be launched into the production / QA environment separately.


The ![Workflow file](.github/workflows/merge_epic_branch.yml) aims to help this process by automating the pushed changes to the epic branch to the environment.

In this example, `staging_a` is a separate development environment.
`epic/staging_a/some_feature` is the epic branch.

The workflow will automatically identify the target environment and push the latest changes to the environment automatically.
