# Devops template

This is a set of script for deploying an app with `web` and `api` component, to heroku, with aws support (for s3 for now).

## Setup

### Macos

You'll need `heroku` and `aws` cli, installed via [Homebrew](https://brew.sh/) for example, as well as `jq` :

```
brew install awscli heroku jq
```

We recommend using `autoenv` ( `brew install autoenv` ) and have a `.env` file at the root of your project, with at least the following variables :

```
PROJECT=my-project
AWS_PROFILE=my-project-aws-profile
```

## Usage

We use the `ENV` env var to create and destroy environment. You can therefore use it like this :

```
ENV=some-feature ./setup
```

And when you're done :

```
ENV=some-feature ./destroy
```

you'll then have a production environment available at [https://my-project-some-feature-web.herokuapp.com]()
