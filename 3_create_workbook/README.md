# Create a workbook

Here create a new workbook and get the active sheet. We then enter data onto the worksheet using various methods. Finally, we save the workbook as "sample.xlsx".

## Create a workbook

```python
from openpyxl import Workbook
wb = Workbook()
```
## Get active worksheet

```python
ws = wb.active

# or
# In case you have multiple sheets, you have to mention the name of the worksheet, as given below. 
ws2 = wb["Sheet2"]
```

## create new worksheet
 (wb.active set to 0 by default)

You can create new worksheets using the Workbook.create_sheet() method:

```python
ws1 = wb.create_sheet("Mysheet") # insert at the end (default)
#or
ws2 = wb.create_sheet("Mysheet", 0) # insert at first position
#or
ws3 = wb.create_sheet("Mysheet", -1) # insert at the penultimate position
```

## sample code can be found in app.py