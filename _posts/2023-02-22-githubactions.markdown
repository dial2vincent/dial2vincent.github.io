---
layout: post
title:  "What is GitHub Actions?"
date:   2022-02-22 
categories: jekyll update
---
# What is GitHub Actions?
- 5 major steps:  Events, Workflows, Jobs, Actions, Runners
## Events
When:
- Merge to main branch
- Commit and Push
- Someone create issue
## Workflows
When the event happens then do the workflow
## Jobs
- Job will be in the workflows
  - Example 
    Job: run unit tests
    Step 1. action check out
    Step 2. npm test
- Single job or multiple jobs
- Job can be action
## Actions
- You can reuse the action liberary that already has been written
- action check out
- action setup node
## Runner
- It will be a VM or container that Job can run in here

# How to create workflows
- The yaml format file should be in the .github/workflows/workflow.yml
- Sample code:
```
name: learn-github-actions
on: [push]
jobs:
  check-bat-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: '14'
      - run: npm install -g bats
      - run: bats -v
```
# Demo
- You need get a sample demo code.

