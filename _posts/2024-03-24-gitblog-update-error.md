---
title: Gitblog update error
date: 2024-03-24  #YYYY-MM-DD HH:MM:SS +/-TTTT
last_modified_at : 2024-03-24
categories: [TIL, Git] #[TOP_CATEGORIE, SUB_CATEGORIE]
tags: [gitblog]     # TAG names should always be lowercase
#math: true

toc : true
toc_sticky : true

runs:
  using: 'node20'
  main: 'main.js'
---


## Issue 
I commit & pushed the post to github, but the post did not get updated on the gitblog

## What I've tried 
I thought I made error in commit & push, but I couldn't find any error on github.
The log showed it the posts have been deployed.


## Solution
Delete web cache
https://sukyungdev.github.io/posts/Post-03/


## Lesson Learned
The gitblog may not be updated because there are web cache stored on my computer and it won't change just by re-opening the page


## Maybe tomorrow
Learn how the web cache works
