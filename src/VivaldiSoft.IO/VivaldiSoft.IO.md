<a name='assembly'></a>
# VivaldiSoft.IO

## Contents

- [DirectoryHelper](#T-VivaldiSoft-IO-DirectoryHelper 'VivaldiSoft.IO.DirectoryHelper')
  - [CopyDirectory(source,destination,overwrite)](#M-VivaldiSoft-IO-DirectoryHelper-CopyDirectory-System-String,System-String,System-Boolean- 'VivaldiSoft.IO.DirectoryHelper.CopyDirectory(System.String,System.String,System.Boolean)')
- [FileHelper](#T-VivaldiSoft-IO-FileHelper 'VivaldiSoft.IO.FileHelper')
  - [IsFileOpen(file,fileAccess)](#M-VivaldiSoft-IO-FileHelper-IsFileOpen-System-String,System-IO-FileAccess- 'VivaldiSoft.IO.FileHelper.IsFileOpen(System.String,System.IO.FileAccess)')

<a name='T-VivaldiSoft-IO-DirectoryHelper'></a>
## DirectoryHelper `type`

##### Namespace

VivaldiSoft.IO

##### Summary

A static class of extension methods for [Directory](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.IO.Directory 'System.IO.Directory').

<a name='M-VivaldiSoft-IO-DirectoryHelper-CopyDirectory-System-String,System-String,System-Boolean-'></a>
### CopyDirectory(source,destination,overwrite) `method`

##### Summary

Copy files from the source folder to destination folder overwriting the content.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| source | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | Source folder. |
| destination | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | Destination folder. |
| overwrite | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Overwrite destination file. |

##### Example

```csharp
var source = "sourceDir";
var destination = "destDir";
var overwrite = true;
DirectoryHelper.CopyDirectory(source, destination, overwrite); 
```

##### Remarks

This method check if is posible to override a file and retry it.

<a name='T-VivaldiSoft-IO-FileHelper'></a>
## FileHelper `type`

##### Namespace

VivaldiSoft.IO

##### Summary

A static class of extension methods for [File](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.IO.File 'System.IO.File').

<a name='M-VivaldiSoft-IO-FileHelper-IsFileOpen-System-String,System-IO-FileAccess-'></a>
### IsFileOpen(file,fileAccess) `method`

##### Summary

Check if a file is open.

##### Returns

True if file is open, false otherwise.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| file | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | File name. |
| fileAccess | [System.IO.FileAccess](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.IO.FileAccess 'System.IO.FileAccess') | File access. |

##### Example

```csharp
var file= "foo";
var fileAccess = FileAccess.ReadWrite;
var fileIsOpen = FileHelper.IsFileOpen(file, fileAccess)
/*
fileIsOpen is true if file is open, false otherwise.
*/ 
```
