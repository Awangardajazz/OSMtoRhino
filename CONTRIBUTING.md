<p align="center">
	<h1 align="center">Contributing</h1>
</p>

## Issues
[Issues](https://docs.github.com/en/github/managing-your-work-on-github/about-issues) are used to track tasks that contributors can help with. If you spot something wrong, have a request, or an enhancement, search the open issues on the repo to see if someone else has reported the same thing. If it's something new, open an issue. We'll use this to track what needs to be fixed or improved.


## Commiting

### Branches
A branch is a parallel version of a repository, which does not affect the main branch. This allows you to work freely without disrupting the *live* version.

### Fork
Forking is mostly used when a contributor doesn't have private access to the main/sub branch of development. Forking a repository allows you to copy a repo to your own account and freely experiment without affecting the original project. By default our private repo's have forking disabled.

### Pull Request
When you've made the changes you want to make on a branch or fork, you can merge your code back into the main branch through a pull request. You can submit a [pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests). These changes are then reviewed, and merged with the main repo branch.


## Cloning

### Clone the repo

1. Initialise Git LFS global git hooks on your system by running the following at a command prompt.  You only need to run this once per machine.
   ```bash
   git lfs install
   ```
2. Clone the repository through SSH, replacing $repo with the relevant URL.
   ```bash
   git clone git@github.com:pilbrowandpartners/$repo.git` the repository.
   ```


### Create a branch.

Checkout the new branch.
```bash
git checkout -b new-feature-name
```

### Track large files through Git LFS
We have various default extensions saved in [.gitattributes](.gitattributes), but if you're adding a file that isn't present, run the following command at the repo root.

```bash
git lfs track "*.3dm"
```

### Clone the repo (excluding Git LFS objects)
1. You may want to clone the repo without any large binary files, follow these steps:

   Linux/MacOS:
	```bash
	GIT_LFS_SKIP_SMUDGE=1 git clone git@github.com:pilbrowandpartners/$repo.git
	```
	Windows:
	```bash
	$env:GIT_LFS_SKIP_SMUDGE="1"; git clone git@github.com:pilbrowandpartners/$repo.git
	```

2. You can now selectively checkout binary files to work with, for example:
   * `git lfs pull -I "img/`" to only download images in *img*
   * `git lfs pull -I "img,docs"` to download all images in *img* and *docs*


## Versioning

When creating a version number system, follow protocols outlined in
[Semantic Versioning](https://semver.org/), which briefly reads as following
the MAJOR.MINOR.PATCH principle.
