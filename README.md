[![CodeFactor](https://www.codefactor.io/repository/github/tomcdj71/gcrh/badge)](https://www.codefactor.io/repository/github/tomcdj71/gcrh)
[![Forks](https://img.shields.io/github/forks/tomcdj71/gcrh?style=for-the-badge)](https://github.com/tomcdj71/gcrh/network/members)
[![Stars](https://img.shields.io/github/stars/tomcdj71/gcrh?style=for-the-badge)](https://github.com/tomcdj71/gcrh/stargazers)
[![Repo Size](https://img.shields.io/github/repo-size/tomcdj71/gcrh?style=for-the-badge)](https://github.com/tomcdj71/gcrh)
[![License](https://img.shields.io/github/license/tomcdj71/gcrh?style=for-the-badge)](https://github.com/tomcdj71/gcrh/blob/master/LICENSE)
[![Top Language](https://img.shields.io/github/languages/top/tomcdj71/gcrh?style=for-the-badge)](https://github.com/tomcdj71/gcrh)
[![Last Commit](https://img.shields.io/github/last-commit/tomcdj71/gcrh?style=for-the-badge)](https://github.com/tomcdj71/gcrh/graphs/commit-activity)
[![Release Version](https://img.shields.io/github/v/release/tomcdj71/gcrh?style=for-the-badge)](https://github.com/tomcdj71/gcrh/releases)
<p align="center">
An helper tool for cloning repositories
    <br />
    <a href="https://github.com/tomcdj71/gcrh/issues">Report Bug</a>
    ·
    <a href="https://github.com/tomcdj71/gcrh/issues">Request Feature</a>
    <br />
    <br />    
  </p>
</div>


## 🧐 About gcrh
___
GCRH (Github Clone Repo Helper) is an helper tool for cloning user repositories with ease !
It's build for personnal repos, so you'll need a [personnal access token](https://github.com/settings/tokens) in order to make it work.
   

## 🚀 Getting Started 
___
### Prerequisites
Please note that this script needs some dependencies to work.   
You'll need to install `git`, `jq`, `gh` and `mflibs` 
 - git
 - [jq](https://github.com/stedolan/jq)
 - [gh](https://github.com/cli/cli)
 - [mschf-dev/mflibs](https://github.com/mschf-dev/mflibs)

### [jq](https://github.com/stedolan/jq) and git installation
You can install those two packages with  
`apt install -y jq git`  

### [gh](https://github.com/cli/cli) (cli/cli) installation
> `gh` is GitHub on the command line. It brings pull requests, issues, and other GitHub concepts to the terminal next to where you are already working with `git` and your code.    

```bash
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
```
### [mschf-dev/mflibs](https://github.com/mschf-dev/mflibs) installation 

>A collection of various functions and scripts for BASH 4.0 or greater:
>
>reduce duplicated code
>
>add your own libraries with ease  

To install it, you need to clone this repo to `/usr/lib/mflibs` (**important !**)

`git clone https://github.com/mschf-dev/mflibs /usr/lib/mflibs`

## 🎈 How to use GCRH ?
Now that you have installed all the required packages, you can clone this repo wherever you want.

```git clone https://github.com/tomcdj71/gcrh.git
ln -s /path/to/gcrh/src/gcrh /usr/lib/gcrh
```

### Clone repo(s)
`gcrh clone -u [username] -t [token] -v [public/private (default:public)] -a [true/false (default:false)]`  
Example:  
`gcrh clone -u tomcdj71 -t ghp_MYSUPERTOKEN -v public -a false` will retrieve all my public and non-archived repos and then ask what repos you want clone to `/opt/gcrh/tomcdj71`

### Update repos
`gcrh update -u [username] -t [token]`  
Example:   
`gcrh update -u tomcdj -t ghp_MYSUPERTOKEN` will find all cloned repos and then updates them to the latest commit. All other flags are not taken into consideration.

## 🤝 Contributing
___

Contributions are what make the world go around. We would love to be able to accept any new contributions, but I have not written the contribution guidelines yet.
## 📃 License
___

Distributed under the BSD-3-Clause License. See license for more information.
## ✍️ Authors
___

@tomcdj71 - Idea & Initial work

See the list of contributors who participated in this project.
