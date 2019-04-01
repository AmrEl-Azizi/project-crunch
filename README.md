# Project Crunch

---

## Introduction

Home of the resulting GUI for ece senior design.

---

## How to download the app and install it

### Downloading


### Installation


### Troubleshooting

#### FAQ

> When I configure ssh keys, there is an error that says I only have one ssh key and I must manually reconfigure it. How do I do this?

* You typically generate an ssh key pair, which includes a private key and a public key. The installer was only able to find one of the keys. If you do not have any need for your current key setup or it is a mistake, you can simply delete the extra key and re-run the configuration. If your key was moved by mistake, you can move it back and re-run the configuration. The program looks for keys in the default location, which is `~/.ssh/id_rsa` and `~/.ssh/id_rsa.pub`. If the program finds a key pair, it will just use the existing keys.

#### In Depth Troubleshooting

We recommend cloning the repository and running the project from the command line to debug more in depth errors. You may also reference the code documentation at #TODO. #TODO add more here as we come across it. Also include instructions for gathering stdout and stderr from the project. 

---

## How to use the app

---

## How to modify and maintain this project

---

### Navigating the Repository

The installer lives under `installer/` and the main app lives under `app/`.

There is a minimal example with a working call to a bash script in `examples/src/`. Run it with `fbs run`.

---

### Setting up a virtual environment

<p>
It is recommended to set up a virtual environment to contain the required python dependencies. (There are several ways to do this, the author's favorite is below)
Further reading on virtual environments in python can be found <a href="https://docs.python-guide.org/dev/virtualenvs/">here</a>, <a href="">here</a>, <a href="https://python-guide-cn.readthedocs.io/en/latest/dev/virtualenvs.html">here</a> and <a href="https://docs.python.org/3/tutorial/venv.html">here</a>.
</p>

From the top level of the repository (but inside of it), run:

```bash
virtualenv -p python3 .env
```

This sets up an entire python installation as an environment under the name `.env` which is not descriptive, but keeps you from having to remember how to activate all my different environments.

<p>
Next activate the environment, and install all the python dependencies via the requirements file. When the environment is active it will display to the left of the prompt, as shown below (where the $ symbol indicates your prompt.)
</p>

```bash
$ source .env/bin/activate
(.env) $ pip install -r requirements
```

<p>
When finished with the repository or environment, you can deactivate it with the simple command deactivate.
</p>

```bash
(.env) $ deactivate
$ 
```
---

### Creating a new release

#### Introduction

There is a provided build script for generating a new release called `release.sh`. Before running it make sure:

* Be sure your repository is on master by typing `git status`. 
* Be sure your [virtual environment](#Setting up a virtual environment) is activated.
* You have the Ubuntu `zip` utility installed. (`sudo apt-get install zip`)

The script will compile the projects and generate a zip and a tar file. All artifacts of the process are left in a `build/` directory. Running the script again automatically deletes the `build/` directory. You must follow the GitHub instructions to post the release to the repository. Be prepared to provide a short description of the changes and have a new version number ready. For more information on software versioning, please see [https://en.wikipedia.org/wiki/Software_versioning](https://en.wikipedia.org/wiki/Software_versioning).

#### Usage

The script must be run with the version number as an argument. For example:

```bash
#TODO
```

#TODO follow instructions to set new release https://help.github.com/en/articles/creating-releases

or future #TODO automate it https://developer.github.com/v3/guides/getting-started/
https://developer.github.com/v3/repos/releases/#create-a-release
