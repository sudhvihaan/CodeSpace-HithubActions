Documentations 


name: 04 - using Actions

on: workflow_dispatch 
https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows

on:
  pull_request:
    branches:
      - 'releases/**'
      - '!releases/**-alpha'
      
https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#onpushpull_requestpull_request_targetpathspaths-ignore


jobs:
    build:
        runs-on: ubuntu-latest
        steps:
            - name: Checkout Code to github Actions
              uses: actions/checkout@v4


            - name: Set up Node
              uses: actions/setup-node@v3
              with:
                node-version: '20.x'


            - name: Install Dependencies
              run: npm ci
              working-directory: 04-workflow-actions/react-app

            - name: Run unit Tests
              run: npm run test
              working-directory: 04-workflow-actions/react-app

        # 1. Install dependencies of our react application
        # 2. Execute automated tests

