---
description: Per ottenere dati da WMI, sia nel computer locale che in un computer remoto, è necessario connettersi al servizio WMI connettendosi a uno spazio dei nomi specifico.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'Attività WMI: connessione al servizio WMI'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310328"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>Attività WMI: connessione al servizio WMI

Per ottenere dati da WMI, sia nel computer locale che in un computer remoto, è necessario connettersi al servizio WMI connettendosi a uno [*spazio dei nomi*](gloss-n.md)specifico. Nella maggior parte dei casi, usare la connessione del [moniker](creating-a-wmi-script.md) abbreviato o la connessione del [**localizzatore**](swbemlocator-connectserver.md) . Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Per le connessioni remote sono necessarie le impostazioni appropriate per il Windows Firewall e DCOM. Per ulteriori informazioni, vedere [la pagina relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md) e alla [connessione tramite Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista). A partire da Windows Vista, il controllo dell'account utente (UAC) può influire sull'accesso WMI. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).

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
<td>... connettersi a un computer remoto tramite WMI?</td>
<td>Specificare una delle opzioni seguenti come parte della stringa di connessione del <a href="constructing-a-moniker-string.md">moniker</a> :<br/>
<ul>
<li>Nome del computer NetBIOS, ad esempio &quot; ATL-DC-01&quot;</li>
<li>Un nome di dominio completo, ad esempio &quot; ATL-DC-01.fabrikam.com&quot;</li>
<li>Un indirizzo IPv4, ad esempio &quot; 192.168.1.1&quot;</li>
<li>A partire da Windows Vista, è possibile specificare un indirizzo IPv6 se il computer di destinazione e il computer da cui si sta effettuando la connessione eseguono entrambi IPv6.<br/></li>
</ul>
Per ulteriori informazioni, vedere <a href="connecting-to-wmi-on-a-remote-computer.md">connessione a WMI in un computer remoto</a> e <a href="ipv6-and-ipv4-support-in-wmi.md">supporto per IPv6 e IPv4 in WMI</a>.<br/> <span data-codelanguage="VisualBasic"></span>
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... eseguire uno script WMI con credenziali alternative?</td>
<td><p>Usare il metodo <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. ConnectServer</strong></a> o <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator:: ConnectServer</strong></a> in C++ e includere il nome utente e la password appropriati. Non è possibile modificare le credenziali durante la connessione al computer locale. Per ulteriori informazioni, vedere <a href="creating-a-wmi-script.md">creazione di uno script WMI</a> e <a href="connecting-to-wmi-on-a-remote-computer.md">connessione a WMI in un computer remoto</a>.</p>
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
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

 

 



`
