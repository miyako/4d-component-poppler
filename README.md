# 4d-component-poppler
Cross-platform tools to extract text from PDF, etc.

Example
---

Extract

```
$pdfPath:=Get 4D folder(Current Resources folder)+"sample.pdf"

$FLAG_RAW:=1
$FLAG_LAYOUT:=2
$FLAG_NO_PAGE_BREAK:=4

$text:=pdftotext ($pdfPath;$FLAG_LAYOUT|$FLAG_NO_PAGE_BREAK)
```

Split

```
$srcPath:=$pdfPath
$dstPath:=System folder(Desktop)+"split.pdf"
$pageNum:=2

pdfseparate ($srcPath;$dstPath;$pageNum)
```

Merge

```
ARRAY TEXT($paths;0)
APPEND TO ARRAY($paths;$pdfPath)
APPEND TO ARRAY($paths;$pdfPath)
$dstPath:=System folder(Desktop)+"merge.pdf"

pdfunite (->$paths;$dstPath)
```
