# pySAPScript
SAP Script to Python Translator

This is a very basic approach for converting vba code generated with
SAP Scripting module of SAP GUI. There are three requiremants for the script to run:
 1) code has to be executed from the machine running SAP
    - citrix will not work
    - local instance of SAP with work just fine
 2) Windows machine
 3) win32com python library (pip install pywin32)
    - note that python and pywin32 can be installed on corporate machines
      without administrative rights, check anaconda project for details

Note that the script is very basic, but seems to work just fine with all of
our the processes in the company. Feedback is always welcome.

```python
sc = SAPSciprt(sapConnectionName)   # sapConnectionName is a string with a connection name
sc.loads('sapscript.vba')
exec(str(sc))
```
