# Powershell day1 
*arch=Windows Server 2008 R2 64 bits*  

The problem with languages like Vbscript is that microsoft did not give them a chance at a seeamless integration into its ecosystem. With powershell, Microsoft tried to fix that issue. Hence powershell is a great tool to have in your arsenal.

>Want to change the IP address of a network adapter using
VBS cript? Okay, you can. Want to check its link speed? You can’t, because nobody
remembered to hook that up in a way that VBS cript could get to



>The goal behind Windows PowerShell is that Microsoft builds 100 percent of a prod-
uct’s administrative functionality in the shell


>[...]your choice is learn PowerShell, or would you
like fries with that?


## Todo
* Get a virtual machine up and running
* Installing the ADDS role
* Promoting a domain controller

Suggested:
<http://mng.bz/S085>

## Hints for creating that domain


* The FQDN for your forest root domain should be company.pri .
* The W indows N et BIOS name for your domain should be COMPANY .
* You should set the forest functional level and domain functional level to the highest levels available (which will either be Windows Server 2008 or Windows Server 2008 R2).
* For Additional Domain Controller Options, select only the option to install DNS S erver.
* If you receive a warning about the computer having a dynamically assigned IP address, select “Yes, the computer will use a dynamically assigned IP address.”
* It’s okay that it isn’t recommended—this is just a test computer.
You may receive a warning about a delegation creation problem; just select Yes.
* Accept the default filesystem paths.
* Provide a Restore Mode password. I recommend something easy to remember, such as P@ssw0rd .
* When you see it, select the check box to Reboot on Completion.

***Note***   
Have you already installed the Active Directory Domain Services role by using Server Manager? If not you can do that as a first step.

> Open Server Manager, tell it you want to add a role, and add the Domain Ser-
vices role. Once that finishes, you can begin the domain controller promotion
(Dcpromo) process outlined in the two tutorials

<http://MoreLunches.com> Check it out
