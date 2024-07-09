 
----My Notes

1) You created a repo called CodeSpace-HithubActionsin from git hub and you have cloned 

2) with in C:\Sudhakar\Learn\0001-AWS\05-GithubAction\CodeSpace-HithubActions\.github\workflows> you are creating your workflows(github actions) 

3) you have also done noode JS setup 

4) Git Command 
git init
git add .
git commit - 'initial commit'
git remote add origin  (you might use)
git push 

Behind the secnes
when you do git push  the workflow triggeres a job in git hub action, you need to go to git hub action section and see the job running status 
For example 
I ran below commands 
git add .\01-buildingblocks.yaml
git commit -m "-buildingblock specific"
git push

This wf got triggered in github actions, this because of the event called on: push
you various event for example 

on: [push, fork]
on:
  label:
    types:
      - created
on:
  issues:
    types:
      - opened
      - labeled
on:
  push:
    branches:
      - main
      - 'releases/**'
on:
  label:
    types:
      - created
  push:
    branches:
      - main
  page_build:
on:
  label:
    types: [created, edited]  etc 


    