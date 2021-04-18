---
description: WMI fornisce un'infrastruttura di gestione del sistema standardizzata che può essere sfruttata da numerosi client diversi.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Creazione di client WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd6d89c63218ffd20ef66b2115e581bdb9c4373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310386"
---
# <a name="creating-wmi-clients"></a>Creazione di client WMI

WMI fornisce un'infrastruttura di gestione del sistema standardizzata che può essere sfruttata da numerosi client diversi. Questi client sono compresi tra lo strumento da riga di comando wmic.exe e System Center Operations Manager. È possibile scrivere i propri client WMI usando l'API di scripting WMI, l'API C++ nativa oppure i tipi nello spazio dei nomi System. Management .NET Framework Library Class.

## <a name="how-to-create-a-wmi-client"></a>Come creare un client WMI

Le funzionalità principali di WMI sono costituite dal recupero di oggetti dal repository WMI e dall'analisi delle proprietà di tali oggetti. È anche possibile scegliere di aggiornare tali proprietà o chiamare metodi su tali proprietà. Negli esempi seguenti viene illustrato come eseguire un'attività di amministrazione WMI di base: recupero del nome del computer locale.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td>WMI e PowerShell sono strettamente integrati; per questo motivo, il recupero di oggetti WMI con PowerShell è semplicemente una chiamata al cmdlet Get-WmiObject. Si noti che, per coerenza, il primo frammento di codice dichiara in modo esplicito molti dei valori predefiniti. il secondo presuppone che i valori predefiniti siano corretti.<br/> <span data-codelanguage="PowerShell"></span>
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
<td><p>VBScript era il linguaggio di scripting originale che era stato usato comunemente con WMI. Mentre PowerShell è diventato più popolare, molti degli esempi di codice esistenti in questa documentazione sono scritti in VBScript. Si noti che questo particolare esempio VBScript indica in modo esplicito sia il percorso del computer locale sia il livello di rappresentazione. Questa operazione non è obbligatoria, ma è spesso una procedura consigliata.</p>
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
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creazione di un client con C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</p></td>
<td><p>Questo spazio dei nomi contiene la soluzione corrente per l'accesso a WMI con codice gestito ed è noto come Windows Management Infrastructure (MI o WMIv2). Attualmente, MI è la tecnologia supportata per la creazione di client di gestione gestiti. Per ulteriori informazioni, vedere <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">come implementare un client mi gestito</a> e <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">come implementare un client mi nativo</a>.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

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
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creazione di un client con C# (<a href="/dotnet/api/system.management">System. Management</a>)</p></td>
<td><p>Questo spazio dei nomi contiene la soluzione originale per accedere a WMI con codice gestito. Sebbene le classi <a href="/dotnet/api/system.management">System. Management</a> siano ancora disponibili, le classi <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> sono in genere più efficienti e migliorano la scalabilità. È quindi consigliabile usare le classi MI, anziché le classi WMI originali.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
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
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

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
| [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)                         | Viene descritto un numero di problemi che si verificano quando i client utilizzano l'infrastruttura WMI in un computer remoto.                                                                                          |
| [Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)                         | Mostra un esempio di codice client WMI.                                                                                                                                                                 |
| [Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)                             | Vengono fornite informazioni sulla creazione di diversi client WMI.                                                                                                                                       |
| [Monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md)                                               | Viene descritto come utilizzare WMI per monitorare i dati sulle prestazioni.                                                                                                                                          |
| [Ricezione di un evento WMI](receiving-a-wmi-event.md)                                                           | Viene descritto come visualizzare gli eventi WMI.                                                                                                                                                              |
| [Monitoraggio degli eventi](monitoring-events.md)                                                                   | Viene descritto come monitorare gli eventi WMI.                                                                                                                                                           |
| [Esecuzione di query con WQL](querying-with-wql.md)                                                                   | Introduce la WMI Query Language (WQL).                                                                                                                                                       |
| [Esecuzione di query sullo stato delle funzionalità facoltative](querying-the-status-of-optional-features.md)                     | In Windows 7, WMI ha implementato la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer. |
| [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md)                       | Si concentra sulla sintassi per descrivere la posizione di un'entità gestita WMI.                                                                                                                     |
| [Accesso ad altre funzionalità del sistema operativo con WMI](accessing-other-operating-system-features-with-wmi.md) | Viene descritto come scrivere client WMI che accedono a driver di dispositivo, Active Directory e dispositivi SNMP.                                                                                             |
| [Accesso ai dati nello spazio dei nomi Interop](accessing-data-in-the-interop-namespace.md)                       | I provider di associazioni consentono ai client di Strumentazione gestione Windows (WMI) di attraversare e recuperare i profili e le istanze di classe associate da spazi dei nomi diversi.                      |
| [Modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md)               | Descrive le attività comuni che i client WMI devono eseguire.                                                                                                                                      |
| [Collegamento di classi](linking-classes-together.md)                                                     | Viene illustrato il provider di viste e il modo in cui può essere utilizzato per riunire le informazioni da più classi WMI.                                                                                    |
| [Modifica del registro di sistema](modifying-the-system-registry.md)                                           | Viene descritto come i client WMI possono utilizzare WMI per gestire le informazioni del registro di sistema.                                                                                                                   |



 

