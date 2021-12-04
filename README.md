## What is Cookiecutter?
Cookiecutter creates projects from project templates. In ohter words it will help you initialize your projects easily.


## What is this repo?
This will create your project structure for Django DRF by using cookiecutter utility. It will create your Dockerfile, docker-compoe.yml, .gitignore, nginx.conf and other commonly needed configurations. It will create requirement.in that you can put your limits on package versions.


## Why you should use this?
Imagine you have bunch of projects. Each one has different structures. It will be annoying for you to think about different configurations in different projects. By using something like this you have same structure for your projcts.
Other point is that this will craft your new project easily and in a fast way.


## Usage:
1. First, You need cookiecutter utility. Just install cookiecutter by pip in your terminal
 ```
 pip install cookiecutter
 ```
2. Run cookiecutter command to this dir
```
cookiecutter paht-to-this-dir
```
3. Terminal will ask you question about parameters values. You can use default values by just press Enter.
4. That's it. Your new project structure is ready.

## How I can change it?
It includes two steps;
1. First, put your configuration files in {{cookiecutter.project_name}} directory. For example if you want have settings for SSL here, put it fiels in that directory. Notice that even for directory names you can use parameters. For example directory {{cookiecutter.project_name}} will use project_name value. So if you set Miner for project_name, you will have Miner directory.
2. Second, define your parameters in the cookiecutter.json file.
That's it. Cookiecutter will create files and in them will use your paramters.


## Licenses
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)


