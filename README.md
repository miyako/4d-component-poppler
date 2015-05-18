# 4d-component-poppler
Cross-platform tools to extract text from PDF, etc.

Example
---

```
$pdfPath:=Get 4D folder(Current Resources folder)+"sample.pdf"

$FLAG_RAW:=1
$FLAG_LAYOUT:=2
$FLAG_NO_PAGE_BREAK:=4

$text:=pdftotext ($pdfPath;$FLAG_LAYOUT|$FLAG_NO_PAGE_BREAK)
```
