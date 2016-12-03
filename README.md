About
=====
This is a modified version of pip that integrates in-toto verification.

pip-in-toto installation
=====================
* First install in-toto as outlined in the  
"Download and setup in-toto on *NIX (Linux, OS X, ..)" section of https://github.com/in-toto/in-toto/tree/develop/demo

```shell
# After installing in-toto, get pip-in-toto
git clone https://github.com/team-ferret/pip-in-toto.git

# Change into project root directory
cd pip-in-toto

# Install with pip in "develop mode"
# (we strongly recommend using Virtual Environments)
# http://docs.python-guide.org/en/latest/dev/virtualenvs/
pip install -e .

```

pip-in-toto commands
====================
* The following options are now valid when using pip install
	* --toto-verify <layout> <layout-keys> 
		EXAMPLE: pip install MyDemoProject3 --toto-verify root.layout alice.pub
	* --toto-default (This command requires no arguments. It assumes a layout of "root.layout" and layout-key of "alice.pub")
		EXAMPLE: pip install MyDemoProject3 --toto-default


