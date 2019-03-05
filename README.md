[![Netlify Status](https://api.netlify.com/api/v1/badges/d3d2d1ad-4f4f-4da6-846c-83dfd54e369f/deploy-status)](https://app.netlify.com/sites/cnigenie/deploys)  

# CNI-Genie Website
Welcome to the repository of the public website for CNI-Genie.

We use [Hugo](https://gohugo.io/) to format and generate our website, and
[Netlify](https://www.netlify.com/) to manage the deployment of the site. Hugo
is an open-source static site generator that provides us with templates, content
organisation in a standard directory structure, and a website generation engine.
You write the pages in Markdown, and Hugo wraps them up into a website.

## Quickstart

Here's a quick guide to updating the docs. It assumes you're familiar with the
GitHub workflow and you're happy to use the automated preview of your doc
updates:

1. Fork the [cni-genie/website][cnigenie-website-repo] on GitHub.
2. Make your changes and send a pull request (PR).
3. If you're not yet ready for a review, add a comment to the PR saying it's a
  work in progress or add `[WIP]` in your PRs title. (**Don't** add the Hugo declarative "draft = true" to the
  page front matter, because that will prevent the auto-deployment of the
  content preview described in the next point.)
4. Wait for the automated PR workflow to do some checks. When it's ready,
  you should see a comment like this: **deploy/netlify — Deploy preview ready!**
5. Click **Details** to the right of "Deploy preview ready" to see a preview
  of your updates.
6. Continue updating your doc until you're happy with it.
7. When you're ready for a review, add a comment to the PR and assign a
  reviewer/approver. 
  
## Previewing your changes on a local website server

If you'd like to preview your doc updates as you work, you can install Hugo
and run a local server. This section shows you how.

### Install Hugo

See the [Hugo installation guide][hugo-install]. Here are some examples:

#### Mac OS X:

```
brew install hugo
```

#### Debian:

1. Download the latest Debian package from the [Hugo website][hugo-install].
  For example, `hugo_0.46_Linux-64bit.deb`.
1. Install the package using `dpkg`:

    ```
    sudo dpkg -i hugo_0.46_Linux-64bit.deb
    ```

1. Verify your installation:

    ```
    hugo version
    ```

### Run a local website server

Follow the usual GitHub workflow to fork the repo on GitHub and clone it to your
local machine, then use your local repo as input to your Hugo web server:

1. Ensure you are in your target branch:

    ```
    git branch
    ```

1. Start your website server. Make sure you run this command from the
   `/website/` directory, so that Hugo can find the config files it needs:

    ```
    hugo server -D
    ```

1. Your website is at [http://localhost:1313/](http://localhost:1313/).

1. Continue with the usual GitHub workflow to edit files, commit them, push the
  changes up to your fork, and create a pull request. (See the GitHub workflow

1. While making the changes, you can preview them on your local version of the
  website at [http://localhost:1313/](http://localhost:1313/). Note that if you
  have more than one local git branch, when you switch between git branches the
  local website reflects the files in the current branch.

Useful Hugo docs:
- [Hugo installation guide][hugo-install]
- [Hugo basic usage](https://gohugo.io/getting-started/usage/)
- [Hugo site directory structure](https://gohugo.io/getting-started/directory-structure/)
- [hugo server reference](https://gohugo.io/commands/hugo_server/)
- [hugo new reference](https://gohugo.io/commands/hugo_new/)

## Versioning

For each stable release, we should create a new branch for the relevant documentation. 
Each branch has a corresponding netlify website that automatically syncs each merged PR.

Going forward, the versioned sites should follow this convention:
* `https://cnigenie.netlify.com/` always points to the current *master branch*
* `https://master.cnigenie.netlify.com/` always points to Github head
* `https://vXXX-YYY.cnigenie.netlify.com/` points to the release at vXXX.YYY-branch

[hugo-install]: https://gohugo.io/getting-started/installing/
[hugo-shortcode-templates]: https://gohugo.io/templates/shortcode-templates/
[hugo-shortcodes]: https://gohugo.io/content-management/shortcodes/

[kubeedge-contributor-guide]: CONTRIBUTING.md
[kubeEdge-website-repo]: https://github.com/cni-genie/website
