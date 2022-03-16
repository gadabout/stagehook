# stagehook
Like [skyhook](github.com/gadabout/skyhook) ... but for stage


## The Setup

1. Dev ArgoCD [Argocd](https://argocd.dev.peek.com)
2. Codefresh [Codefresh](https://g.codefresh.io/login)

## How to update image tags for stage

1. Clone this repo somewhere
2. Edit build variables json file for stage: (e.g.`stage/build-variables.json`)
3. Update CF_COMMIT_MESSAGE is the same file with commit message. This commit message is for bodhi repo.
4. git add : (`git add . --all`)
5. Updating stage. (e.g.`git commit -m"updating tags on stage [update stage]"`)
   git commit needs a string in this format `[update stage]` to trigger corresponding peekstack pipeline.
6. git push to master. (e.g.`git push`)
