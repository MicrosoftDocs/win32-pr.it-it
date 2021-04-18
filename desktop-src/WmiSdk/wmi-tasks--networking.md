---
description: Le attività WMI per la rete gestiscono e ottengono informazioni sulle connessioni e sugli indirizzi IP o MAC. Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo https://www.microsoft.com/technet .
ms.assetid: 25da32c3-34bf-4c88-9b09-ff371f2cf8db
ms.tgt_platform: multiple
title: 'Attività WMI: rete'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31e8346a064fe2f6c7ab624897be8e789474f7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310325"
---
# <a name="wmi-tasks-networking"></a>Attività WMI: rete

Le attività WMI per la rete gestiscono e ottengono informazioni sulle connessioni e sugli indirizzi IP o MAC. Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale. Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).


Nella procedura riportata di seguito viene descritto come eseguire uno script.

**Per eseguire uno script**

1.  Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*. Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.
2.  Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.
3.  Digitare **cscript filename.vbs** al prompt dei comandi.
4.  Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati. Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).

> [!Note]  
> Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi. Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file. Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.

 

Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ricerca per categorie</th>
<th>Classi o metodi WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... disabilitare una connessione di rete tramite WMI?</td>
<td>Se si usa DHCP, usare il <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/releasedhcplease-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLease</strong></a> per rilasciare l'indirizzo IP. Se non si utilizza DHCP, non è possibile utilizzare WMI per disabilitare una connessione di rete. Per abilitare di nuovo la connessione di rete, usare <a href="/windows/desktop/CIMWin32Prov/renewdhcplease-method-in-class-win32-networkadapterconfiguration"><strong>objNetCard. RenewDHCPLease</strong></a>. È anche possibile rilasciare o rinnovare tutti i lease DHCP usando i metodi <a href="/windows/desktop/CIMWin32Prov/releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>ReleaseDHCPLeaseAll</strong></a> e <a href="/windows/desktop/CIMWin32Prov/renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration"><strong>RenewDHCPLeaseAll</strong></a> .<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
Set colNetCards = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration &quot; _
        & &quot;Where IPEnabled = True&quot;)
For Each objNetCard in colNetCards
    objNetCard.ReleaseDHCPLease()
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$net = Get-WMIObject -class Win32_NetworkAdapterConfiguration -ComputerName $computer
$netenabled = $net | where {$_.IPenabled}
foreach ($NetCard in $netenabled) {
    &quot;Releasing lease on: {0}&quot; -f $netcard.caption
 $netcard.ReleaseDHCPLease()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... disabilitare o abilitare una scheda di interfaccia di rete?</td>
<td><p>Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> e i metodi <a href="/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter"><strong>Disable</strong></a> o <a href="/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter"><strong>Enable</strong></a> .</p></td>
</tr>
<tr class="odd">
<td>... determinare l'indirizzo IP assegnato a una connessione di rete specificata.</td>
<td><p>Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapter"><strong>Win32_NetworkAdapter</strong></a> e la proprietà <strong>NetConnectionID</strong> per determinare l'indirizzo MAC della connessione di rete. Usare quindi la classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> per trovare l'indirizzo IP associato all'indirizzo Mac.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection 2&#39;&quot;)

For Each objItem in colItems
    strMACAddress = objItem.MACAddress
Next

Set colItems = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapterConfiguration&quot;)

For Each objItem in colItems
    If objItem.MACAddress = strMACAddress Then
        For Each strIPAddress in objItem.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
Set colNics = objWMIService.ExecQuery _
    (&quot;Select * From Win32_NetworkAdapter &quot; _
        & &quot;Where NetConnectionID = &quot; & _
        &quot;&#39;Local Area Connection&#39;&quot;)
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      (&quot;ASSOCIATORS OF &quot; _
          & &quot;{Win32_NetworkAdapter.DeviceID=&#39;&quot; & _
      objNic.DeviceID & &quot;&#39;}&quot; & _
      &quot; WHERE AssocClass=Win32_NetworkAdapterSetting&quot;)
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo &quot;IP Address: &quot; &  strIPAddress
        Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... determinare l'indirizzo MAC di una scheda di rete?</td>
<td><p>Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e controllare il valore della proprietà <strong>MACAddress</strong> .</p></td>
</tr>
<tr class="odd">
<td>... determinare l'indirizzo IP di un computer?</td>
<td><p>Utilizzare la classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e controllare il valore della proprietà <strong>IPAddress</strong> . Viene restituito come matrice, quindi usare un ciclo For-Each per ottenere il valore.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration &quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
            to UBound(IPConfig.IPAddress)
                WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$IPconfigset = Get-WmiObject Win32_NetworkAdapterConfiguration
  
# Iterate and get IP address
$count = 0
foreach ($IPConfig in $IPConfigSet) {
   if ($Ipconfig.IPaddress) {
      foreach ($addr in $Ipconfig.Ipaddress) {
   &quot;IP Address   : {0}&quot; -f  $addr;
   $count++ 
   }
   }
}
if ($count -eq 0) {&quot;No IP addresses found&quot;}
else {&quot;$Count IP addresses found on this system&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>...configUre un computer per iniziare a ottenere il proprio indirizzo IP tramite DHCP?</td>
<td><p>Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/enabledhcp-method-in-class-win32-networkadapterconfiguration"><strong>EnableDHCP</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
 
For Each objNetAdapter In colNetAdapters
    errEnable = objNetAdapter.EnableDHCP()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... assegnare un computer a un indirizzo IP statico?</td>
<td><p>Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/enablestatic-method-in-class-win32-networkadapterconfiguration"><strong>EnableStatic</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
Set colNetAdapters = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NetworkAdapterConfiguration &quot; _
        & &quot;where IPEnabled=TRUE&quot;)
strIPAddress = Array(&quot;192.168.1.141&quot;)
strSubnetMask = Array(&quot;255.255.255.0&quot;)
strGateway = Array(&quot;192.168.1.100&quot;)
strGatewayMetric = Array(1)
 
For Each objNetAdapter in colNetAdapters
    errEnable = objNetAdapter.EnableStatic( _
        strIPAddress, strSubnetMask)
    errGateways = objNetAdapter.SetGateways(_
        strGateway, strGatewaymetric)
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... ottenere informazioni sulle schede di rete senza recuperare anche le informazioni su elementi come le connessioni RAS e VPN?</td>
<td><p>Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration"><strong>Win32_NetworkAdapterConfiguration</strong></a> . Nella query <a href="querying-with-wql.md">WQL</a> usare questa clausola: Where <strong>IPEnabled</strong>  =  <strong>true</strong>.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
Set IPConfigSet = objWMIService.ExecQuery _
    (&quot;Select IPAddress from Win32_NetworkAdapterConfiguration&quot; _
        & &quot; where IPEnabled=TRUE&quot;)
 
For Each IPConfig in IPConfigSet
    If Not IsNull(IPConfig.IPAddress) Then 
        For i=LBound(IPConfig.IPAddress) _
        to UBound(IPConfig.IPAddress)
            WScript.Echo IPConfig.IPAddress(i)
        Next
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... effettuare il ping di un computer senza usare Ping.exe?</td>
<td><p>Usare la classe <a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> .</p>
<p><a href="/previous-versions/windows/desktop/wmipicmp/win32-pingstatus"><strong>Win32_PingStatus</strong></a> possibile restituire i dati per i computer che includono sia indirizzi IPv4 che indirizzi IPv6.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_ 
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colPings = objWMIService.ExecQuery _
    (&quot;Select * From Win32_PingStatus where Address = &#39;192.168.1.1&#39;&quot;)

For Each objStatus in colPings
    If IsNull(objStatus.StatusCode) _
        or objStatus.StatusCode<>0 Then 
        WScript.Echo &quot;Computer did not respond.&quot; 
    Else
        Wscript.Echo &quot;Computer responded.&quot;
    End If
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;client1&quot;
Set objShell = CreateObject(&quot;WScript.Shell&quot;)
Set objScriptExec = objShell.Exec( _
    &quot;ping -n 2 -w 1000 &quot; & strComputer)
strPingResults = LCase(objScriptExec.StdOut.ReadAll)
If InStr(strPingResults, &quot;reply from&quot;) Then
    If InStr(strPingResults, &quot;destination net unreachable&quot;) Then
        WScript.Echo strComputer & &quot;did not respond to ping.&quot;
    Else
        WScript.Echo strComputer & &quot; responded to ping.&quot;
    End If 
Else
    WScript.Echo strComputer & &quot; did not respond to ping.&quot;
End If
  </code></pre></td>
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

