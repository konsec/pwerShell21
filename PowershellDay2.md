# PowershellDay2 

It is a dotnet-framework based scripting language? It is a programming language? A shell?

It gives you the full underlying power of the dotnet framework.

Some cmd.exe and bash commands such as ls, dir, ren, copy will work with powershell but once parameters are supplied (eg. dir /S), we get errors since they don't behave the same way in powershell as their native shell.

```
>PS /tmp> dir /S  
Get-ChildItem: Cannot find path '/S' because it does not exist.  
PS /tmp> 
```

>The filesystem is a hierarchical database.    
>
There are many such hierearchical dbs, including ldap and the registry. So dir will work with file directories as well as registers.  

>A PSDdrive is a mapping between the shell and some kind of data store—the filesystem, the registry, or evenActive Directory. a PSDdrive provider sits between the shell and that storage system, making the storage system appear to be a disk drive within the shell

PSDrive providers can be added to the shell so that the shell learns about other types of storage. Mysql for example. 

>The shell always starts with the samePSD rives mapped

Type Get-Psdrives and see.

*Note*
Remember to add ":" when using a drive. For example "cd hkcu:". But not when creating one.

Mapping a new PSdrive
New-PSDrive -name DEMO -psprovider FileSystem -root
\\\\Server\Share\Folder

Some internal commands such as Net (use), ping work fine with powershell, but others might not as parmeters can become confusing. When faced with such a situation, try to break down the command. (Or maybe use cmd.exe?)
```code
$exe = "C:\Vmware\vcbMounter.exe"
$host = "server"
$user = "joe"
$password = "password"
$machine = "somepc"
$location = "somelocation"
$backupType = "incremental"

& $exe -h $host -u $user -p $password -s "name:$machine" -r $location -t
$backupType
```
Some aliases

```Get-ChildItem (for Dir , Ls )
Set-Location (for Cd )
Move-Item (for Move )
Rename-Item (for Ren )
Remove-Item (for Del , Rm , RmDir )
Copy-Item (for Copy , Cp )
Get-Content (for Type , Cat )
New-Item (for MkDir )
```

Observations about powershell commandlets
structure verb-noun

Parameter names start with "-". eg. get-items -recurse ?

Efficiency: If a parameter of a cmdlet is the only one starting with a certain later, it can be shortened so. eg. get-i -r(ecurse)


Some more commands

Display a list of services 						Get-Service
Display a list of running processes 			Get-Process
Display the contents of an event log 			Get-EventLog
Create a new service 							New-Service
Retrieve Exchange mailboxes						Get-Mailbox
Create a new Exchange mailbox 					New-Mailbox

parameters that take no value get a dash before their name