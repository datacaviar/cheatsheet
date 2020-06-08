# Resources

> This is a list of   `resources` that I personally use.



## Virtual Environments

> Virtualenvs

1. **Check if python3 is installed**

```bash
	$ python3
```

2. **Instal Virtual Envs**

```bash
	$ pip install virtualenv
```

If you don't have permissions to install it.

```bash
	$ sudo pip install virtualenv
```

3. **Create a directory to store your virtual envs**

```bash
	$ cd ~
	$ mkdir virtualenvs
```

4. **Install the `vitualenvwrapper` package**

```bash
	$ pip install virtualenvwrapper
```

5. **Edit your `.bashrc` file**

```bash
	$ cd ~
	$ nano .bashrc
```

6. **Add the following lines. Make sure you insert the right path for your system**

```.bashrc
	export WORKON_HOME=~/virtualenvsexport 

	VIRTUALENVWRAPPER_PYTHON=/usr/local/bin/python3

	source /usr/local/bin/virtualenvwrapper.sh
```

Sometimes `.bashrc` will not load if that happens run this command
```bash
	$ source ~/.bashrc
```

7. **Create a new virtualenv with Jupyter**

```bash
	$ cd ~
	$ cd virtualenvs
	$ mkvirtualenv --python=/usr/local/bin/python3 name_of_virtual_env
```

You will know when you are in your env when you see the name in parentesis `(name_of_virtual_env) ~ $`

8. **Install the software needed for the virtual env**

```bash
	(name_of_virtual_env) ~ $ pip install --upgrade pip
	(name_of_virtual_env) ~ $ pip install numpy pandas matplotlib
	(name_of_virtual_env) ~ $ pip install jupyter jupyterlab
``` 

9. **Create a directory for the notebook**

```bash
	(name_of_virtual_env) ~ $ cd ~
	(name_of_virtual_env) ~ $ mkdir project_name
	(name_of_virtual_env) ~ $ cd project_name
```

10. **Fireup jupyter lab**

```bash
	(name_of_virtual_env) ~ $ jupyter lab
```

11. **Activating and deactivating virtual envs using virtualenvwrapper**

```bash
	$ workon

		project_1
		project_2
		project_3

	$ workon project_2

	(project_2) ~ $

```

12. **Deactivating**

```bash
	(project_2) ~ $ deactivate

	$ 
```