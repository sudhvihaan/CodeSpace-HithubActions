name: Event and Activity

on:
  pull_request:
    types:
      - opened
      - synchronize
    branches:
      - main # this is triggered only when branching out from main 

jobs:
  echo:
    runs-on: ubuntu-latest
    steps:
      - run: echo "Running whenever a PR is opened or synchronized and base branch is main"
