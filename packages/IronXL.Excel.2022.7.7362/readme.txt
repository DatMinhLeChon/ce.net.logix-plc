﻿IronXL  - The Excel Library for .Net 
=============================================================
Quickstart:  https://ironsoftware.com/csharp/excel/
	

Compatibility
=============================================================
Supports applications and websites developed in 
- .Net FrameWork 4.5 (and above) for Windows and Azure
- .Net Core 2, 3 (and above) for Windows, Linux, MacOs and Azure
- .Net 5 for Windows, Linux, MacOs and Azure
- .Net 6 for Windows, Linux, MacOs and Azure

C# Code Example
=============================================================
```
using IronXL;


//Create new Excel WorkBook document. 
//The default file format is XLSX, but we can override that for legacy support
WorkBook xlsWorkbook = WorkBook.Create(ExcelFileFormat.XLS);
xlsWorkbook.Metadata.Author = "IronXL";

//Add a blank WorkSheet
WorkSheet xlsSheet = xlsWorkbook.CreateWorkSheet("new_sheet");
//Add data and styles to the new worksheet

xlsSheet["A1"].Value = "Hello World";
xlsSheet["A2"].Style.BottomBorder.SetColor("#ff6600");
xlsSheet["A2"].Style.BottomBorder.Type = IronXL.Styles.BorderType.Double;

//Save the excel file
xlsWorkbook.SaveAs("NewExcelFile.xls");
```

Documentation
=============================================================

- Code Samples				:	https://ironsoftware.com/csharp/excel/examples/read-excel/
- MSDN Class Reference		:	https://ironsoftware.com/csharp/excel/object-reference/
- Tutorials					:	https://ironsoftware.com/csharp/excel/tutorials/how-to-read-excel-file-csharp/
- Support					:	developers@ironsoftware.com
