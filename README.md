<div align="center">

## A FileExists Function


</div>

### Description

Checks to see if a file exists.
 
### More Info
 
full file path(FullFileName as String)

True or False


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Blake Royer](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/blake-royer.md)
**Level**          |Beginner
**User Rating**    |3.3 (62 globes from 19 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/blake-royer-a-fileexists-function__1-10824/archive/master.zip)





### Source Code

```
Private Function FileExists(FullFileName As String) As Boolean
On Error GoTo MakeF
	'If file does not exist, there will be an error
	Open FullFileName For Input As #1
	Close #1
	'no error, file exists
	FileExists = True
Exit Function
MakeF:
	'error, file does not exist
	FileExists = False
Exit Function
End Function
```

