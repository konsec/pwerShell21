# PowershellDay3
### Getting help

>If you aren’t willing to read PowerShell’s help files, you won’t be effective with Power-Shell. You won’t learn how to use it, you won’t learn how to administer products like Windows and Exchange with it, and you might as well stick with the GUI .

man  (A wrapper , not an alias)  
help  (pipes output to more)  
get-help
Get-Command

help \*KEYWORD*


#### parameter sets (choose your set)

>SYNTAX

>Get-EventLog [-AsString] [-ComputerName <string[]>] [-List] [<Com
monParameters>]
  
> Get-EventLog [-LogName] <string> [[-InstanceId] <Int64[]>] [-Afte
r <DateTime>] [-AsBaseObject] [-Before <DateTime>] [-ComputerName
<string[]>] [-EntryType <string[]>] [-Index <Int32[]>] [-Message
<string>] [-Newest <int>] [-Source <string[]>] [-UserName <strin
g[]>] [<CommonParameters>]
 >
 Either -Astring || option2  
  >SYNTAX  
>Get-EventLog [-AsString] [-ComputerName <string[]>] [-List] [<CommonParameters>]
Get-EventLog [-LogName] <string> [[-InstanceId] <Int64[]>] [-After <DateTime>] [-AsBaseObject] [-Before <DateTime>] [-ComputerName
<string[]>] [-EntryType <string[]>] [-Index <Int32[]>] [-Message
<string>] [-Newest <int>] [-Source <string[]>] [-UserName <strin
g[]>] [<CommonParameters>]
  
  optional  params **[-ComputerName <string[]>]**  
  positional params **[-LogName] \<string> [[-InstanceId] <Int64[]>]**  
  name, val of -logname is not wrapped in brackts, mandatory
  -instanceid is, so optional
  
  Switches   
  **[-AsString]** (in abreviated mode)  
  **-AsString [\<SwitchParameter>]** (in full mode help)
  
  **string[]**: array, list or collection of strings    
  >Get-EventLog Security -computer Server-R2,DC4,Files02
  
  
  Help Get-EventLog -example  
  help about*
  
  
  
  #### useful help sources
  http://mng.bz/5w8E
  
  http://www.primaltools.com/downloads/communitytools/
  
  http://download.microsoft.com
  

  
  
 
  

