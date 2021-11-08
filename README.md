# General guidelines
## Git
### Commits
1. When creating git commits create a commit with a title and a body (see [this commit](https://github.com/smarterpsoft/sapxt-server/commit/dca7e31c508f89fa015c41cef75972c54ac5b9f6) for reference). The way you do this is when running the git commit command do not supply a -m flag, instead in the editor write the title followed by an empty line and then the body. Like so:

```
Git title

Git body
```

2. Keep the title short but somewhat specific
3. Give as much specific detail in the body as possible. Make sure that when someone who looks at the commit and is familiar with the codebase can tell what happened without looking at the code (obviously not more than 3 lines but enough to get a gist of what happened)
4. When convenient try to make commits smaller, more atomic. But this is not a requirement
5. When convenient also try to make commits stable (the whole thing works more or less, commits never completely break the program). Also not a requirement

### Branches
1. Always keep the main branch stable with high quality code, if you are implementing a new feature / fixing things do one of the following:
2. **Encouraged** Create a separate temporary branch for the issue / feature (e.g. `segfault-fix` for fixing a segfault, `new-xyz-api` for new xyz api, etc), test and complete it there, then merge to main and **delete the branch**. If the feature is big and will take a while to implement, please **push the branch to the server** otherwise feel free to leave it as a local branch
3. **Discouraged** You may also keep a dev branch for all dev tasks but I strongly discourage this. It has several disadvantages. You can't cleanly implement several different features at the same time, different people can't implement different features at the same time and you have to keep syncing it with the main branch
4. If you want you may also keep a "bleeding edge" branch (like `latest`) where you merge changes from latest features (which must still be on separate branches). `latest` can then merge to main every now and then. But never write to `main` or `latest` branches directly

## Javascript
Please make sure to use the eslint linked in this repository. Your editor should be able to seamlessly plug into it (see the [.eslintrc.js](.eslintrc.js) file).
