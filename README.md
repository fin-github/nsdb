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
