---
linkTitle: Github
title: Github
type: book
date: 2024-10-27
summary: This provides some tips when using Github for ecological code hosting and data analyses.
---

## Managing github credentals in R-studio.
Github no longer supports using a password to interact with repositories. You will get the error code below if you use a password to connect to Github.

```console
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
fatal: Authentication failed for 'https://github.com/OWNER/REPO.git/'
```

Thus, you will need to use the Windows credential manager or you will need to follow the steps below to add an access token in Linux or MAC OS. The tutorial below can also be used in the Windows OS.
### Prerequisites
- R installed
- R-studio installed
- Git installed

### Steps to add an access token
The instructions below were summarized from the following web page: https://happygitwithr.com/https-pat
1. Run `usethis::create_github_token()` in the R console to generate your access token.
2. Leave the web page open that opens up. You will need to copy the access token later.
3. Next run `gitcreds::gitcreds_set()` in the R console.
4. Now copy and paste your accesss token from the webpage that opened up when running the first command.
