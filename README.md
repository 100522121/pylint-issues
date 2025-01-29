# pylint-issues
Quick guide on solving pylint issues. 

## Check if Pylint is installed
Try writing the following command in the Terminal. If it states Pylint is not installed, try it again by referring to this [steps](#Pylint-installed-but-unable-to-find-syntax-mistakes).
```
pip list | grep pylint
```
Alternatively, try to find Pylint's installation path using the command `where pylint`, or install the Pylint package (apart from the plugin) if it was not automatically installed when installing the plugin.

## Pylint installed but unable to find syntax mistakes
If Pylint is already installed and its overlay can be accessed, but does not find any error in a errory-python code, then uninstall it from `File > Settings > Plugins > Pylint > Uninstall`. Then, reinstall it but specifically with the command:
```
python pip install pylint
```

## Instalation issues
If pip or any other Python commands are not being recognised, it could be due to these reasons:

### General info:
- Verify *pip* is installed in your device.
- Try updating your *pip* to the latest version available.
- After every solution applied, **restart** Pycharm.

#### System Environment variables
The existence of *python.exe* is not recognised, for which you have to find and copy its installation path. Usually you can find it in the Windows taskbar search bar (or by only pressing the Windows key) and right clicking to `open file location`. It is vital to mention that this can direct you to the Shortcut rather than the actual installation path:
![image](https://github.com/user-attachments/assets/bfe7cdaa-2a99-410a-b51f-baa89a91135a)
Right clicking the shortcut this time should direct you the desired path:
![image](https://github.com/user-attachments/assets/44a2ec08-a0b3-44d5-b28c-b84cb896ccee)

#### Manage App Execution Aliases
If `python` commands do not work or you receive Microsoft Store messages/redirects, Python and its Apps Installer are conflicting. The simplest way to overcome this problem is to write `py` or `python3` instead of `python`.

For a permanent solution, go to `Settings > Apps > Advanced Settings > **App Execution Aliases**` and disable all Python App Installers that appear.
![image](https://github.com/user-attachments/assets/1e86140a-3720-4994-916f-93503ec6e6ee)

## Farewell
For more information, refer to some StackOverflow queries:
[1] [Which files get installed when 'pip' installing 'pylint'?](https://stackoverflow.com/questions/51358987/which-files-get-installed-when-pip-installing-pylint)
[2] [Python was not found; run without arguments to install from the Microsoft Store](https://stackoverflow.com/questions/65348890/python-was-not-found-run-without-arguments-to-install-from-the-microsoft-store) 
[3] [Pip installed (and updated), but can't be found](https://stackoverflow.com/questions/71110397/pip-installed-and-updated-but-cant-be-found?)
