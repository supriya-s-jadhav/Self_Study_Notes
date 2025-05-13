### What is Virtual environment
This is simply a self-contained location that enables us to maintain separate and isolated environment for our python projects. It lets us manage:
- Dependencies
- Versions
- Packages
Without conflicts across different projects

### Commands
These commands are for mac os:
Create virtual env
```
python3 -m venv env
```
Activate virtual env
```
source env/bin/activate
```

Deactivate virtual env
```
deactivate
```

### Shared Projects
Every time we download a new project, there should be a requirements.txt file. First, create a new virtual environment for that project, activate it and then install all the packages using requirements.txt file. Command for doing this is:
1. Use pip to install packages
Pip: Preferred Installer Program
```
pip install requests
```
2. List of installed packages:
```
pip list 
```
3. Install project dependencies 
```
pip install -r requirements.txt 
```
4. Save dependencies
```
pip freeze > requirements.txt 
```