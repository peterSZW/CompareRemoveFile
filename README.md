
# CompareRemoveFile v1.0
```
Compare and Remove Duplication File Tool, based on file size and partial MD5. Wechat:Peter_szw

Usage:
  CompareRemoveFile [command]

Available Commands:
  BuildDB-Path   Build a zipped database from path
  CheckDB-DB     Check whether the files in the database exist in another database
  CleanDB        Clean up files in database, move duplicate files to 'X:\DupFiles' path in same hard disk
  CleanPath      Clean up files in path, move duplicate files to 'X:\DupFiles' path in same hard disk
  CleanPath-DB   Clean up the files in the path, the files that already exist in the database
  CleanPath-Path Clean up the files in the path, the files that already exist in other path
  completion     Generate the autocompletion script for the specified shell
  help           Help about any command

Flags:
  -h, --help   help for CompareRemoveFile

Use "CompareRemoveFile [command] --help" for more information about a command.
```

# Example

```bash
# move duplicate photo to 'D:\DupFiles' path 
CompareRemoveFile.exe CleanPath -p D:\Photo -y
```

```bash
# move duplicate photo (already in E:\OtherPhoto) to 'D:\DupFiles' path 
CompareRemoveFile.exe CleanPath-Path -p D:\Photo -o E:\OtherPhoto -y
```

# Advanced Example

```bash

# build a database
CompareRemoveFile.exe BuildDB-Path -p Z:\AllPhoto -d AllPhotoDB

# move duplicate photo (already in Z:\AllPhoto) to 'D:\DupFiles' path 

CompareRemoveFile.exe CleanPath-DB -p D:\PhotoA -d AllPhotoDB -y
CompareRemoveFile.exe CleanPath-DB -p D:\PhotoB -d AllPhotoDB -y 
CompareRemoveFile.exe CleanPath-DB -p D:\PhotoC -d AllPhotoDB -y
```

# Chinese

```
CompareRemoveFile v1.0

根据文件大小和部分MD5,比较和删除重复文件工具。微信:Peter_szw

Usage:
  CompareRemoveFile [command]

Available Commands:
  BuildDB-Path   遍历路径中的所有文件，并压缩保存到数据库
  CheckDB-DB     检查数据库中的文件，是否存在于另一个数据库中
  CleanDB        清理数据库中的重复文件，将重复文件移动到同一硬盘中的“X:\DupFiles”路径下
  CleanPath      清理路径中的重复文件，将重复文件移动到同一硬盘中的“X:\DupFiles”路径下
  CleanPath-DB   清理路径中的重复文件，即数据库中已存在的文件
  CleanPath-Path 清理路径中的重复文件，即其他路径已存在的文件
  completion     Generate the autocompletion script for the specified shell
  help           Help about any command

Flags:
  -h, --help   help for CompareRemoveFile

Use "CompareRemoveFile [command] --help" for more information about a command.
```
