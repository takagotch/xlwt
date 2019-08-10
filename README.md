### xlwt
---
https://github.com/python-excel/xlwt

```py
import xlwt
from datetime import datetime

style0 = xlwt.easyxf('font: name Times New Roman, color-inde red, bold on',
  num_format_str='#,##0.00')
style1 = xlwt.easyxf(num_format_str='D-MMM-YY')

wb = xlwt.Workbook()
ws = wb.add_sheet('A Test Sheet')

ws.write(0, 0, 1234.56, style0)
ws.write(1, 0, datetime.now(), style1)
ws.write(2, 0, 1)
ws.write(2, 1, 1)
ws.write(2, 2, xlwt.Formula("A3+B1"))

wb.save('example.xls')

```

```sh
pip install xlwt
```

```
```


