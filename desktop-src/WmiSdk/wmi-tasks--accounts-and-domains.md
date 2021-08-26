---
description: Le attività amministrative di account e di dominio ottengono informazioni quali il dominio del computer o l'utente attualmente connesso.
ms.assetid: 1a9cc44b-c366-465d-a0d0-536d5dc818b5
ms.tgt_platform: multiple
title: 'Attività WMI: Account e domini'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bacf37ebab07ab60e347efa1645c3cf320700fb3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884693"
---
# <a name="wmi-tasks-accounts-and-domains"></a>Attività WMI: Account e domini

Le attività amministrative di account e di dominio ottengono informazioni quali il dominio del computer o l'utente attualmente connesso. Molte di queste attività vengono eseguite in modo ottimale con [gli script ADSI.](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Per altre informazioni e altri esempi, vedere il repository di script [TechNet ScriptCenter.](https://www.microsoft.com/technet/scriptcenter)

Gli esempi di script illustrati in questo argomento ottengono i dati solo dal computer locale. Per altre informazioni su come usare lo script per ottenere dati da computer remoti, vedere [Connessione a WMI in un computer remoto.](connecting-to-wmi-on-a-remote-computer.md)


Nella procedura seguente viene descritto come eseguire uno script.

**Per eseguire uno script**

1.  Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*. Assicurarsi che l'editor di testo non a .txt'estensione al file.
2.  Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.
3.  Digitare **cscript filename.vbs** al prompt dei comandi.
4.  Se non è possibile accedere a un registro eventi, verificare se è in esecuzione da un prompt dei comandi con privilegi elevati. Alcuni registri eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da Controlli di accesso utente.

> [!Note]  
> Per impostazione predefinita, cscript visualizza l'output di uno script nella finestra del prompt dei comandi. Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file. Digitare **cscript filename.vbs > outfile.txt** prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.

 

Nella tabella seguente sono elencati esempi di script che possono essere utilizzati per ottenere vari tipi di dati dal computer locale.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Ricerca per categorie</th>
<th>Classi o metodi WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... determinare il dominio a cui appartiene un computer?</td>
<td>Usare la <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e controllare il valore della <strong>proprietà Domain.</strong> È anche possibile usare la <strong>proprietà DNSDomain</strong> in <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)

For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Domain: &quot; & objComputer.Domain
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$computer = Get-WmiObject -Class Win32_ComputerSystem
&quot;System Name: {0}&quot; -f $computer.name
&quot;Domain : {0}&quot; -f $computer.domain</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Domain&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... determinare se un computer è un server o una workstation?</td>
<td><p>Usare la <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e la <strong>proprietà DomainRole.</strong></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colComputers = objWMIService.ExecQuery(&quot;Select DomainRole from Win32_ComputerSystem&quot;)
For Each objComputer in colComputers
    Select Case objComputer.DomainRole 
        Case 0 
            strComputerRole = &quot;Standalone Workstation&quot;
        Case 1        
            strComputerRole = &quot;Member Workstation&quot;
        Case 2
            strComputerRole = &quot;Standalone Server&quot;
        Case 3
            strComputerRole = &quot;Member Server&quot;
        Case 4
            strComputerRole = &quot;Backup Domain Controller&quot;
        Case 5
            strComputerRole = &quot;Primary Domain Controller&quot;
    End Select
    Wscript.Echo strComputerRole
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = Get-WmiObject -Class Win32_ComputerSystem 

&quot;Computer `&quot;{0}.{1}`&quot; is a: &quot;-f $Computer.Name,$computer.domain

switch  ($computer.DomainRole) {
    0 {&quot;Standalone Workstation&quot;}
    1 {&quot;Member Workstation&quot;}
    2 {&quot;Standalone Server&quot;}
    3 {&quot;Member Server&quot;}
    4 {&quot;Backup Domain Controller&quot;}
    5 {&quot;Primary Domain Controller&quot;}
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... determinare il nome del computer?</td>
<td><p>Usare la <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e la <strong>proprietà</strong> Name. È anche possibile usare la <strong>proprietà DNSHostName</strong> in <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a>.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Computer Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = Get-WmiObject -Class Win32_ComputerSystem
&quot;Computer Name is: {0}&quot; -f $Computer.Name</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... trovare il nome della persona attualmente connesso a un computer?</td>
<td><p>Usare la <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e la <strong>proprietà UserName.</strong></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
Set colComputer = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
 
For Each objComputer in colComputer
    Wscript.Echo &quot;User Name = &quot; & objComputer.UserName & VBNewLine & &quot;Computer Name = &quot; & objComputer.Name
WScript.Echo objComputer.UserName
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$computers = Get-WmiObject -Class Win32_ComputerSystem 
&quot;Logged on user(s):&quot;
foreach($computer in $computers) {
   &quot;User: {0}&quot; -f $computer.UserName
}</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable&lt;CimInstance&gt; queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(&quot;User Name: &quot; + cimObj.CimInstanceProperties[&quot;UserName&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... rinominare un computer?</td>
<td><p>Usare la <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> e il <strong>metodo Rename.</strong></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colComputers = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colComputers
    errReturn = ObjComputer.Rename(&quot;NewName&quot;)
    WScript.Echo &quot;Computer name is now &quot; & objComputer.Name
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>param (
[$String] $NewName = &#39;NewName&#39;,
[$string] $Comp = &quot;.&quot;
}

<# Get computer object #>
$Computer = Get-WmiObject -Class Win32_ComputerSystem -ComputerName $comp

<# Rename the Computer #>
$Return  = $Computer.Rename($NewName)

if ($return.ReturnValue -eq 0) {
   &quot;Computer name is now: $NewName&quot;
   &quot; but you need to reboot first&quot;
} else {
&quot;  RenameFailed, return code: {0}&quot; -f $return.ReturnValue
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... recuperare solo i gruppi locali tramite WMI?</td>
<td><p>Usare la <a href="/windows/desktop/CIMWin32Prov/win32-group"><strong>Win32_Group</strong></a> e includere la <strong>clausola WHERE seguente</strong> nella query <a href="querying-with-wql.md">WQL.</a></p>
<p><code>Where LocalAccount = True</code></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( _
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Group  Where LocalAccount = True&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Local Account: &quot; & objItem.LocalAccount & VBNewLine _
        & &quot;Name: &quot; & objItem.Name & VBNewLine _
        & &quot;SID: &quot; & objItem.SID & VBNewLine _
        & &quot;SID Type: &quot; & objItem.SIDType & VBNewLine _
        & &quot;Status: &quot; & objItem.Status & VBNewLine
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Accts=Get-WMIObjectWin32_Group|where {$_.LocalAccount}
$accts |ftName, Sid, SidType, Status-autosize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Esempi di applicazioni WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
