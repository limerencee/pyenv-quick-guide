# Python Virtual Environments Guide

## Installation

> GitHub repo for installation can be found at: [https://github.com/pyenv/pyenv-installer](https://github.com/pyenv/pyenv-installer).

Install the binaries:

```bash
$ curl https://pyenv.run | bash
# or
$ curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
```

Insert the following lines into your `.bashrc` or any bash profile that you use:

```bash
# pyenv bins
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

Restart your shell to continue (either manually or):

```bash
$ exec "$SHELL"
```

## Usage

> GitHub repo for more information can be found at: [https://github.com/pyenv/pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv).

### Managing Python Versions

**Listing Available Python Versions**

```bash
$ pyenv verions

* system (set by /home/kali/.pyenv/version)
```

**Installing Python Versions**

```bash
$ pyenv install 3.6.0

# Listing
$ pyenv versions

* system (set by /home/kali/.pyenv/version)
  3.6.0
```

**Deleting Python Versions**
```bash
$ pyenv uninstall 3.6.0

# Listing
$ pyenv versions

* system (set by /home/kali/.pyenv/version)
```

### Managing Python Virtual Environments

**Listing Available Python Virtual Environments**

```bash
$ pyenv virtualenvs

```

**Creating Python Virtual Environments**

```bash
$ pyenv virtualenv 3.6.0 venv36

# Listing
$ pyenv virtualenvs
  3.6.0/envs/venv36 (created from /home/kali/.pyenv/versions/3.6.0)
  venv36 (created from /home/kali/.pyenv/versions/3.6.0)
```

**Deleting Python Virtual Environments**

```bash
$ pyenv uninstall venv36
pyenv-virtualenv: remove /home/kali/.pyenv/versions/3.6.0/envs/venv36? (y/N) y

# Listing
$ pyenv virtualenvs

```

**Starting Python Virtual Environments**

```bash
$ source activate venv36
pyenv-virtualenv: activate venv36
pyenv-virtualenv: prompt changing will be removed from future release. configure `export PYENV_VIRTUALENV_DISABLE_PROMPT=1' to simulate the behavior.

(venv36) ┌──(venv36)(kali@Kali)-[~]
```

**Stopping Python Virtual Environments**

```bash
$ source deactivate
pyenv-virtualenv: deactivate 3.6.0/envs/venv36
```
