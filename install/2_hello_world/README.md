# openpyxl-sample program

Here create a new workbook and get the active sheet. We then enter data onto the worksheet using various methods. Finally, we save the workbook as "sample.xlsx".

## hello world

```python
from openpyxl import Workbook
wb = Workbook()

# grab the active worksheet
ws = wb.active

# Data can be assigned directly to cells
ws['A1'] = 42

# Rows can also be appended
ws.append([1, 2, 3])

# Python types will automatically be converted
import datetime
ws['A2'] = datetime.datetime.now()

# Save the file
wb.save("sample.xlsx")
```

## sample code can be found in app.py