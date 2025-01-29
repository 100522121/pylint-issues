# Pylint Issues
Quick guide on solving [Pylint](https://github.com/pylint-dev/pylint) issues in Pycharm IDE. 

#### General info:
- Verify *pip* is installed in your device.
- Try updating *pip* to the latest version available.
- After every solution applied, **restart** Pycharm.

## Check if Pylint is installed
Try writing the following command in the Terminal. If it states Pylint is not installed, refer to this [steps](#Pylint-installed-but-unable-to-find-syntax-mistakes).
```
pip list | grep pylint
```
Alternatively, try to find Pylint's installation path using the command `where pylint`, or install the Pylint package (apart from the plugin) if it was not automatically installed when installing the plugin.

## Pylint installed but unable to find syntax mistakes
If Pylint is already installed and its overlay can be accessed, but does not find any error in any code, uninstall it from `File > Settings > Plugins > Pylint > Uninstall`. Then, reinstall it specifically with the command:
```
python pip install pylint
```

## Instalation issues
If *pip* or any other Python commands are not being recognised, it could be due to these reasons:

### System Environment variables
The existence of *python.exe* is not recognised, for which you have to find and copy its installation path. Usually you can find it in the Windows taskbar search bar (or by only pressing the Windows key) and right clicking to `open file location`. It is vital to mention that this can direct you to the Shortcut rather than the actual installation path:

![image1](https://github.com/user-attachments/assets/0782bba2-0fd9-4a72-9076-984afc918e16)

Right clicking the shortcut this time should direct you the desired path:

![image2](https://github.com/user-attachments/assets/1c85bce7-fc63-46e2-b5f1-ce3757acb475)

Go `System Properties > System Environment variables` and add two paths independently: the path itself and the path with \Scripts at the end, for instance:
```
C:\Users\yourname\AppData\Local\Programs\Python\Python312
C:\Users\yourname\AppData\Local\Programs\Python\Python312\Scripts
```
![recording](https://github.com/user-attachments/assets/552d37bd-e397-470a-b3ae-21aeadce850a)

### Manage App Execution Aliases
If `python` commands do not work or you receive Microsoft Store messages/redirects, Python and its Apps Installer are conflicting. The simplest way to overcome this problem is to write `py` or `python3` instead of `python`.

For a permanent solution, go search directly for **Manage App Execution Aliases** in the Windows search bar or manually in `Settings > Apps > Advanced Settings > App Execution Aliases` and disable all Python App Installers that appear.
![image3](https://github.com/user-attachments/assets/1e86140a-3720-4994-916f-93503ec6e6ee)

## Farewell
For more information, refer to some StackOverflow queries:
- [Which files get installed when 'pip' installing 'pylint'?](https://stackoverflow.com/questions/51358987/which-files-get-installed-when-pip-installing-pylint)
- [Python was not found; run without arguments to install from the Microsoft Store](https://stackoverflow.com/questions/65348890/python-was-not-found-run-without-arguments-to-install-from-the-microsoft-store)
- [Pip installed (and updated), but can't be found](https://stackoverflow.com/questions/71110397/pip-installed-and-updated-but-cant-be-found?)
