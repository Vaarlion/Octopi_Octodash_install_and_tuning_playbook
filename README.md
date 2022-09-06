# Introduction
This playbook is a quickly put together install script to run over a raspberry with Octopi distro
It achieve the following
 * Install octodash GUI
 * Setup a minimal X11
 * Hide startup with plymouth
 * add a custom CA

Because i don't own the right to the splash logo i used, it isn't provided, please provide you own or remove that part of the playbook the the standard raspberry splash screen

I've also removed the CA, same, provide your own or remove the section

# Setup
```
python -m venv --system-site-packages .venv
source .venv/bin/activate
pip install -r requirements.txt
```
# Run
```
source .venv/bin/activate
ansible-playbook -i inventory.ini --ask-pass -K playbook.yml
```


# TODO
 * make octodash service a notify one to wait for a full start before stopping plymouth
 * add promtail to gather logging data
