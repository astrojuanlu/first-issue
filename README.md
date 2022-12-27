<p align="center">
  <img src="public/firstissue.png" width="355" height="51"/>
</p>

---

Welcome! 👋🏼

**First Issue** is an initiative to curate a list of accessible issues from popular projects, so developers looking for a new (or first) project to contribute to can get started quickly.

Open-source maintainers are always looking to get more people involved, but it can be challenging to become a contributor. We believe First Issue lowers the barrier for future contributions - and this is why it exists.

## Adding a new project

You're welcome to add a new project in First Issue, and we encourage all projects &mdash; old and new, big and small.

Follow these simple steps:

- To maintain the quality of projects in First Issue, please make sure the GitHub repository you want to add meets the following criteria:

  - It has at least three issues with the `good first issue` label or other labels defined in `firstissue.json` (see `labels` and the end).

  - It has at least 10 contributors.

  - It has at least 1000 stars.

  - It contains a README.md with detailed setup instructions for the project, and a CONTRIBUTING.md with guidelines for new contributors.

  - It is actively maintained (last update less than 1 month ago).

- Add your repository's path (in the format `owner/name` and lexicographic order) to [firstissue.json](firstissue.json).

- Create a new pull-request. Please add the link to the issues page of the repository in the PR description. Once the pull request is merged, the changes will be live on [firstissue.dev](https://firstissue.dev/).

## How does it work?

First Issue is a static website that uses Next.js, React and Typescript. The data shown on the website is loaded from the [generated.json](generated.json) file, which is generated by [generate.ts](generate.ts) by querying the GitHub API to fetch issues from the repositories listed in [firstissue.json](firstissue.json). The labels defined in [firstissue.json](firstissue.json) are used to filter issues for the repositories.

To contribute new features and changes to the website, you would want to run the app locally. Please follow these steps:

1. Clone the project locally. Make sure you have a recent version of Node.js installed on your computer.

2. You can use the included [generated.json](generated.json) as dummy data or you can run `npm run prebuild` to fetch the latest data from GitHub yourself: for this, you will need to set the `GITHUB_TOKEN` environment variable to a valid GitHub access token. Notice: repositories not maching the criteria listed above (see rules in [generated.json](generated.json)) are automatically removed from [firstissue.json](firstissue.json) when the [generated.json](generated.json) script runs.

3. Start the development server and open the app in your browser.

```bash
# install the dependencies
$ npm install
# start the development server
$ npm run dev
```

Good to know when you commit: the project contains a `pre-commit` hook that runs linters automatically to ensure code quality!

#### Credits

This project is based on [good-first-issue](https://github.com/deepsourcelabs/good-first-issue). The app and generation scripts have been rewritten using Next.js, React and Typescript, new features have been added and the UI is being updated too. The deployment process has been streamlined, complexity has been reduced and further improvements are planned.
