---
description: WMI offre un'infrastruttura di gestione di sistema standardizzata che può essere sfruttata da diversi client.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Creazione di client WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95123d4462408a25591df2babb8b1ddd83942e5e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883071"
---
# <a name="creating-wmi-clients"></a>Creazione di client WMI

WMI offre un'infrastruttura di gestione di sistema standardizzata che può essere sfruttata da diversi client. Questi client vanno dallo strumento wmic.exe riga di comando a System Center Operations Manager. È possibile scrivere client WMI personalizzati usando l'API di scripting WMI, l'API C++ nativa o i tipi nello spazio dei nomi della libreria di classi system.Management .NET Framework.

## <a name="how-to-create-a-wmi-client"></a>Come creare un client WMI

La funzionalità principale di WMI è costituita dal recupero di oggetti dal repository WMI e dall'esame delle proprietà di tali oggetti. È anche possibile scegliere di aggiornare tali proprietà o chiamare metodi su tali proprietà. Gli esempi seguenti illustrano come eseguire un'attività di amministrazione WMI di base: recupero del nome del computer locale.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Termine</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creazione di un client con PowerShell<br/></td>
<td>WMI e PowerShell sono strettamente integrati; Di conseguenza, il recupero di oggetti WMI con PowerShell è semplicemente una questione di chiamare il cmdlet Get-WmiObject. Si noti che per coerenza, il primo frammento di codice indica in modo esplicito molti dei valori predefiniti. il secondo presuppone che i valori predefiniti siano corretti.<br/> <span data-codelanguage="PowerShell"></span>
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
<td><pre><code>#explicitly states many of the default parameters
$myComputer = Get-WmiObject -ComputerName &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Query &quot;SELECT * FROM Win32_ComputerSystem&quot;
foreach ($computer in $myComputer)
{ &quot;System Name: &quot; + $computer.name }

#assumes the default values are correct
Get-WmiObject Win32_ComputerSystem | Format-Table &quot;Name&quot;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><p><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creazione di un client con VBScript</p></td>
<td><p>VBScript era il linguaggio di scripting originale che usava comunemente WMI. Anche se PowerShell è diventato più diffuso, molti degli esempi di codice esistenti in questa documentazione sono scritti in VBScript. Si noti che questo particolare esempio di VBScript indica in modo esplicito sia il percorso del computer locale che il livello di rappresentazione. questo non è obbligatorio, ma è spesso una procedura consigliata.</p>
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

</div></td>
</tr>
<tr class="odd">
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creazione di un client con C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</p></td>
<td><p>Questo spazio dei nomi contiene la soluzione corrente per l'accesso a WMI con codice gestito ed è noto come Windows Management Infrastructure (MI o WMIv2). Attualmente, MI è la tecnologia supportata per la creazione di client di gestione gestita. Per altre informazioni, vedere <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">Come implementare un client MI gestito</a> e Come <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">implementare un client MI nativo.</a></p>
<div class="code">
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
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creazione di un client con C# (<a href="/dotnet/api/system.management">System.Management</a>)</p></td>
<td><p>Questo spazio dei nomi contiene la soluzione originale per l'accesso a WMI con codice gestito. Anche se <a href="/dotnet/api/system.management">le classi System.Management</a> sono ancora disponibili, le <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">classi Microsoft.Management.Infrastructure</a> sono in genere più efficienti e sono più scalabili. Di conseguenza, è consigliabile usare le classi MI anziché le classi WMI originali.</p>
<div class="code">
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
</tbody>
</table>



 

Nella tabella seguente sono elencati gli argomenti inclusi in questa sezione.



| Argomento                                                                                                        | Descrizione                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)                         | Descrive una serie di problemi che si verificano quando i client usano l'infrastruttura WMI in un computer remoto.                                                                                          |
| [Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)                         | Mostra il codice client WMI di esempio.                                                                                                                                                                 |
| [Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)                             | Fornisce informazioni sulla creazione di vari client WMI.                                                                                                                                       |
| [Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)                                               | Descrive come usare WMI per monitorare i dati sulle prestazioni.                                                                                                                                          |
| [Ricezione di un evento WMI](receiving-a-wmi-event.md)                                                           | Viene descritto come visualizzare gli eventi WMI.                                                                                                                                                              |
| [Monitoraggio degli eventi](monitoring-events.md)                                                                   | Viene descritto come monitorare gli eventi WMI.                                                                                                                                                           |
| [Esecuzione di query con WQL](querying-with-wql.md)                                                                   | Introduce il WMI Query Language (WQL).                                                                                                                                                       |
| [Esecuzione di query sullo stato delle funzionalità facoltative](querying-the-status-of-optional-features.md)                     | In Windows 7 WMI ha implementato la [**classe \_ OptionalFeature Win32.**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer. |
| [Descrizione del percorso di un oggetto WMI](describing-the-location-of-a-wmi-object.md)                       | Si concentra sulla sintassi per descrivere il percorso di un'entità gestita WMI.                                                                                                                     |
| [Accesso ad altre funzionalità del sistema operativo con WMI](accessing-other-operating-system-features-with-wmi.md) | Descrive come scrivere client WMI che accedono a driver di dispositivo, Active Directory e dispositivi SNMP.                                                                                             |
| [Accesso ai dati nello spazio dei nomi di interoperabilità](accessing-data-in-the-interop-namespace.md)                       | I provider di associazioni Windows client di Strumentazione gestione Windows (WMI) per attraversare e recuperare profili e istanze di classe associate da spazi dei nomi diversi.                      |
| [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md)               | Descrive le attività comuni che i client WMI devono eseguire.                                                                                                                                      |
| [Collegamento di classi tra loro](linking-classes-together.md)                                                     | Illustra il provider di visualizzazione e come può essere usato per riunire le informazioni di più classi WMI.                                                                                    |
| [Modifica del Registro di sistema](modifying-the-system-registry.md)                                           | Descrive come i client WMI possono usare WMI per gestire le informazioni del Registro di sistema.                                                                                                                   |



 

