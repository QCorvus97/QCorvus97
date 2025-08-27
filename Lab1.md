## Lab 01

- Name: Jayden Swartzel
- Email: swartzel.10@wright.edu

## Part 1 - GitHub Profile

1. [QCorvus97's GitHub Profile](https://github.com/QCorvus97)

## Part 2 - Research

| Windows | Linux / Mac | Action |
| ---     | ---         | ---    |
| help    | man         |Provides a description of the help system and how to get more information about other commands      |
| Get-Location | pwd    |Returns the current directory        |
| Get-ChildItem | ls    |Returns the item(s) contained at the current location        |
| mkdir   | mkdir       |Creates a directory (folder)        |
| Set-Location | cd     |Sets the working location to whatever is specified        |
| New-Item | touch      |Creates a new item        |
| Move-Item | mv        |Moves an item to a specified location        |
| Copy-Item | cp        |Copies an item to a specified location        |
| Remove-Item | rm      |Deletes a specified item        |
| notepad.exe | vim     |Opens notepad        |

## Part 3 - Command Line Navigation

My OS is:
- [x] Windows
- [] Linux
- [] Mac

My Command Line Shell is: PowerShell

### Navigating My OS on the Command Line

1. Full / absolute path to your user's home directory: 
PS C:\Users\quake>
2. Create a directory named `DirA`: 
PS C:\Users\quake> mkdir DirA


    Directory: C:\Users\quake


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         8/27/2025     11:44                DirA
3. Create a directory named `Dir B`: 
PS C:\Users\quake> mkdir "Dir B"


    Directory: C:\Users\quake


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         8/27/2025     11:45                Dir B
4. Go into `DirA`: 
PS C:\Users\quake> Set-Location DirA
5. Go into `Dir B` from `DirA`: 
PS C:\Users\quake\DirA> Set-Location C:\Users\quake\"Dir B"
6. Return to your user's home directory: 
PS C:\Users\quake\Dir B> cd ..
7. Create a file named `test.txt`: 
PS C:\Users\quake> New-Item "test.txt"


    Directory: C:\Users\quake


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         8/27/2025     11:49              0 test.txt
8. Move the file named `test.txt` into `DirA`: 
PS C:\Users\quake> Move-Item "test.txt" DirA
PS C:\Users\quake> Set-Location DirA
PS C:\Users\quake\DirA> ls


    Directory: C:\Users\quake\DirA


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         8/27/2025     11:49              0 test.txt
9. Contents of `test.txt`:
```
This is a test
```
10. Make a copy of `test.txt` named `copy.txt` in `DirA`: 
PS C:\Users\quake\DirA> Copy-Item test.txt copy.txt
11. View the contents of `DirA`: 
PS C:\Users\quake\DirA> ls


    Directory: C:\Users\quake\DirA


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         8/27/2025     11:52             14 copy.txt
-a----         8/27/2025     11:52             14 test.txt
12. Make a copy of `test.txt` in `Dir B` named `fodder.txt`: 
PS C:\Users\quake\DirA> Copy-Item test.txt C:\Users\quake\"Dir B"\fodder.txt
PS C:\Users\quake\DirA> cd ..
PS C:\Users\quake> Set-Location "Dir B"
PS C:\Users\quake\Dir B> ls


    Directory: C:\Users\quake\Dir B


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         8/27/2025     11:52             14 fodder.txt
13. Delete / remove both `fodder.txt` AND `Dir B`:
PS C:\Users\quake\Dir B> Remove-Item fodder.txt
PS C:\Users\quake\Dir B> ls
PS C:\Users\quake\Dir B> cd ..
PS C:\Users\quake> Remove-Item "Dir B"
PS C:\Users\quake> ls


    Directory: C:\Users\quake


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         8/13/2025     10:07                .vscode
d-r---          1/1/2025     14:33                Contacts
d-----         8/27/2025     11:54                DirA
d-----          1/1/2025     14:54                Documents
d-r---         8/26/2025     19:19                Downloads
d-r---          1/1/2025     14:33                Favorites
d-----         8/25/2025     13:52                Hello
d-r---          1/1/2025     14:33                Links
d-r---          1/1/2025     14:33                Music
dar--l         8/24/2025     14:02                OneDrive
d-r---          1/1/2025     14:33                Saved Games
d-r---          1/1/2025     14:52                Searches
d-r---         1/22/2025     00:53                Videos

## Citations

[Provided information about what PowerShell commands do and how to use them.](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.management/?view=powershell-7.5)



