# Linters Config

## How to use this repo? 🤔

Each directory listed below contains config files specific to one programming language and README file with detailed instructions:

- [html&css + javascript](./html-css-js) (for projects that require you to use both JavaScript and HTML & CSS)
- [react&redux](./react-redux)
- [Laravel](./laravel)(coming soon)

Follow those instructions in order to set up linters or validators in your repo.

## GitHub Actions

[Github Actions](https://help.github.com/en/actions) is a [CI/CD](https://codilime.com/what-is-ci-cd-all-you-need-to-know/) service offered by GitHub. It allows you to automate your workflow by letting GitHub take care of a number of tasks which can be triggered by [different of events](https://help.github.com/en/actions/reference/events-that-trigger-workflows) on the platform.

🐛 **What to do if GitHub Actions does not work?** Check [Troubleshooting](#troubleshooting) below.

You can automate tasks by creating **workflows** in your GitHub repository. GitHub will look for [YAML](https://en.wikipedia.org/wiki/YAML) files inside the `.github/workflows` directory.

## Troubleshooting

Depending on the configuration of your GitHub credentials, you may have an error like this when trying to create a new GitHub Actions workflow:

```
! [remote rejected] master -> master (refusing to allow an OAuth App to create or update workflow `.github/workflows/file.yml` without `workflow` scope)

```

The problem is that you may be using a credentials app like [Credential Manager in Windows](https://github.com/gitextensions/gitextensions/issues/4916#issuecomment-557509451) or OSX Keychain. In that case, you should [setup a personal access token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line) and configure it in your credentials app. Make sure to check the `workflow` permissions when you setup your personal access token.


## Validation

Do not make any changes in config files - they represent style guidelines that you share with your team.

TSEs will validate that you are using the same configuration files provided here. You can check if your linter configuration is correct using the [`check-linters-config`](scripts) script.

## Stickler

Stickler is an app, that can be integrated into any Github repo. It uses multiple linters that can be configured according to the programmer’s needs.

With Stickler enabled you can see:

- Linting result in your PR
  <img width="788" alt="result" src="https://user-images.githubusercontent.com/120318564/222523826-2a0435e6-c833-47e8-a0fb-a7b204043134.png">

- `Checks` tab in your PR
  <img width="1403" alt="checks" src="https://user-images.githubusercontent.com/120318564/222523952-61a1b00b-0935-43c8-86b4-0ab958a63332.png">

- Comments under any problematic line of code
  <img width="975" alt="comment" src="https://user-images.githubusercontent.com/120318564/222524108-23f0d23f-cd61-40fe-a1b2-6e677a53b4b7.png">


See more: https://stickler-ci.com/


## Contributing

Everybody is welcome to suggest changes in linters config files.

In order to do it, fork this repository, create a new branch and open a Pull Request from your branch. A detailed description of this process.
