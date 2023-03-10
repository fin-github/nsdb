# NSDB (Not Secure Data Base)
So easy you dont even have to learn it....

## Functions

- SaveData *datakey, datadescription, file="db.txt", write=False*
- LoadData *datakey, only_description=False, file="db.txt"*
- DeleteData *datakey, file="db.txt"*
- datacontains *datakey, file="db.txt"*
- replacedata *datakey, replacmentkey, replacmentdescription, file="db.txt"*
- getdata *leavekey=None, leavedescription=None, file="db.txt"*

## Examples
### Basics
##### GetData/SaveData
**DEMO.PY** = 
```python
from nsdb import getdata, SaveData

SaveData("key", "desc", file="testdb.txt")
print(getdata(file="testdb.txt"))
```
**testdb.txt** =
```txt
key:desc
```
**OUTPUT** = 
```python
{"key": "desc"}
```
If you dont get it getdata will get ***EVERY*** key and description from the file. But if you want to get a specific data you can use LoadData
##### LoadData/DeleteData
Lets say you want to load whatever the user says... Example:
**DEMO.PY** = 
```python
from nsdb import DeleteData, LoadData

query = input("What data do you want to load?\n")

output = LoadData(datakey=query, file="testdb.txt")

print(output)
```
**INPUT** = 
```python
key
```
**OUTPUT** = 
```python
description
```
