Python Utilities to make working with Open Bank Project api easier

- uses python3

## Install

```
pip install --user obp-python # Requires at least python 3
```

> Warning: If your operating system defaults to python 2, your pip command might be:
``
pip3 install --user obp-python
#or 
pip3.6 install --user obp-python
```


## Usage
```
Usage: obp [OPTIONS] COMMAND [ARGS]...

Options:
  --help  Show this message and exit.

Commands:
  addaccount       📁 Add a bank account
  addrole          🚧 Add a role for current user
  adduser          📝 Add a user
  deletebranches   ⚠️ 🏦 Delete all branches
  getaccountsheld  📁 Get list of accounts held
  getauth          🔑 Get your DirectLogin token
  getbanks         🏦 Get list of banks
  getuser          😃 Get your user info
  getuserid        📋 Get your user id
  importbranches   🚜 Import branches from spreadsheet template
  init             💡 Initalize connection to your Open Bank Project instance
  sandboximport    🚜 Bulk import sandbox data from json input
```

## Examples

You must initalize the obp cli once, by doing:
```
obp init
```

### Generate Direct Login Token
```
obp init 
Please enter your API_HOST: api.example.com
Please enter your username:
Please enter your password: : 
Repeat for confirmation: 
... generating direct login token
Please enter your OBP_CONSUMER_KEY: # Go to api.example.com, then "Get API Key" to generate consumer key.
obp getauth # Displays your DirectLogin token
```


#### Contributing

> **Note** You can ignore this is your just using the utlity. This is 
just for developing the utlity.

To work on this utility as a developer:
##### Building 

```
# Setup python3 environment
virtualenv -p python3 venv
. venv/bin/activate
git clone <this-repo>
# Building wheels etc
python setup.py sdist bdist_wheel
# Installing your edits locally:
pip install -e <path-to-this-repo> # -e means Install  a  project  in editable mode (i.e.  setuptools "developmode")
# Work on utility..submit pull request 

```
###### Update history

- 0.19 Added sandboximport utility `obp sandboximport --example`
- 0.0.9
Switch to use `OBP_API_HOST` instead of `OBP_ENDPOINT`
