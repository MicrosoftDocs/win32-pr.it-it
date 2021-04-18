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
# <a name="creating-wmi-clients"></a><span data-ttu-id="694fd-103">Creazione di client WMI</span><span class="sxs-lookup"><span data-stu-id="694fd-103">Creating WMI Clients</span></span>

<span data-ttu-id="694fd-104">WMI fornisce un'infrastruttura di gestione del sistema standardizzata che può essere sfruttata da numerosi client diversi.</span><span class="sxs-lookup"><span data-stu-id="694fd-104">WMI provides a standardized system management infrastructure that can be leveraged by a number of different clients.</span></span> <span data-ttu-id="694fd-105">Questi client sono compresi tra lo strumento da riga di comando wmic.exe e System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="694fd-105">These clients range from the wmic.exe command line tool to System Center Operations Manager.</span></span> <span data-ttu-id="694fd-106">È possibile scrivere i propri client WMI usando l'API di scripting WMI, l'API C++ nativa oppure i tipi nello spazio dei nomi System. Management .NET Framework Library Class.</span><span class="sxs-lookup"><span data-stu-id="694fd-106">You can write your own WMI clients by using either the WMI Scripting API, the native C++ API or by using the types in the System.Management .NET Framework class library namespace.</span></span>

## <a name="how-to-create-a-wmi-client"></a><span data-ttu-id="694fd-107">Come creare un client WMI</span><span class="sxs-lookup"><span data-stu-id="694fd-107">How to create a WMI client</span></span>

<span data-ttu-id="694fd-108">Le funzionalità principali di WMI sono costituite dal recupero di oggetti dal repository WMI e dall'analisi delle proprietà di tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="694fd-108">The core functionality of WMI consists of retrieving objects from the WMI repository and examining the properties of those objects.</span></span> <span data-ttu-id="694fd-109">È anche possibile scegliere di aggiornare tali proprietà o chiamare metodi su tali proprietà.</span><span class="sxs-lookup"><span data-stu-id="694fd-109">You can also choose to update those properties, or call methods on those properties.</span></span> <span data-ttu-id="694fd-110">Negli esempi seguenti viene illustrato come eseguire un'attività di amministrazione WMI di base: recupero del nome del computer locale.</span><span class="sxs-lookup"><span data-stu-id="694fd-110">The following examples show how to perform a basic WMI administration task: retrieving the name of the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="694fd-111">Termine</span><span class="sxs-lookup"><span data-stu-id="694fd-111">Term</span></span></th>
<th><span data-ttu-id="694fd-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="694fd-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="694fd-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creazione di un client con PowerShell</span><span class="sxs-lookup"><span data-stu-id="694fd-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creating a client with PowerShell</span></span><br/></td>
<td><span data-ttu-id="694fd-114">WMI e PowerShell sono strettamente integrati; per questo motivo, il recupero di oggetti WMI con PowerShell è semplicemente una chiamata al cmdlet Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="694fd-114">WMI and PowerShell are tightly integrated; as such, retrieving WMI objects with PowerShell is simply a matter of calling the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="694fd-115">Si noti che, per coerenza, il primo frammento di codice dichiara in modo esplicito molti dei valori predefiniti. il secondo presuppone che i valori predefiniti siano corretti.</span><span class="sxs-lookup"><span data-stu-id="694fd-115">Note that for consistency, the first code snippet explicitly states many of the default values; the second assumes that the default values are correct.</span></span><br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="694fd-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="694fd-116">PowerShell</span></span></th>
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
<td><p><span data-ttu-id="694fd-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creazione di un client con VBScript</span><span class="sxs-lookup"><span data-stu-id="694fd-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creating a client with VBScript</span></span></p></td>
<td><p><span data-ttu-id="694fd-118">VBScript era il linguaggio di scripting originale che era stato usato comunemente con WMI.</span><span class="sxs-lookup"><span data-stu-id="694fd-118">VBScript was the original scripting language that had common use with WMI.</span></span> <span data-ttu-id="694fd-119">Mentre PowerShell è diventato più popolare, molti degli esempi di codice esistenti in questa documentazione sono scritti in VBScript.</span><span class="sxs-lookup"><span data-stu-id="694fd-119">While PowerShell has become more popular, many of the existing code samples in this documentation are written in VBScript.</span></span> <span data-ttu-id="694fd-120">Si noti che questo particolare esempio VBScript indica in modo esplicito sia il percorso del computer locale sia il livello di rappresentazione. Questa operazione non è obbligatoria, ma è spesso una procedura consigliata.</span><span class="sxs-lookup"><span data-stu-id="694fd-120">Note that this particular VBScript sample explicitly states both the local machine path as well as the impersonation level; this is not required, but is often a best practice.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="694fd-121">VB</span><span class="sxs-lookup"><span data-stu-id="694fd-121">VB</span></span></th>
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
<td><p><span data-ttu-id="694fd-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creazione di un client con C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</span><span class="sxs-lookup"><span data-stu-id="694fd-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creating a client with C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</span></span></p></td>
<td><p><span data-ttu-id="694fd-123">Questo spazio dei nomi contiene la soluzione corrente per l'accesso a WMI con codice gestito ed è noto come Windows Management Infrastructure (MI o WMIv2).</span><span class="sxs-lookup"><span data-stu-id="694fd-123">This namespace contains the current solution for accessing WMI with managed code, and is known as the Windows Management Infrastructure (MI, or WMIv2).</span></span> <span data-ttu-id="694fd-124">Attualmente, MI è la tecnologia supportata per la creazione di client di gestione gestiti.</span><span class="sxs-lookup"><span data-stu-id="694fd-124">Currently, MI is the supported technology for creating managed management clients.</span></span> <span data-ttu-id="694fd-125">Per ulteriori informazioni, vedere <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">come implementare un client mi gestito</a> e <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">come implementare un client mi nativo</a>.</span><span class="sxs-lookup"><span data-stu-id="694fd-125">For more information, see <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">How to Implement a Managed MI Client</a> and <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">How to Implement a Native MI Client</a>.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="694fd-126">C#</span><span class="sxs-lookup"><span data-stu-id="694fd-126">C#</span></span></th>
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
<td><p><span data-ttu-id="694fd-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creazione di un client con C# (<a href="/dotnet/api/system.management">System. Management</a>)</span><span class="sxs-lookup"><span data-stu-id="694fd-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creating a client with C# (<a href="/dotnet/api/system.management">System.Management</a>)</span></span></p></td>
<td><p><span data-ttu-id="694fd-128">Questo spazio dei nomi contiene la soluzione originale per accedere a WMI con codice gestito.</span><span class="sxs-lookup"><span data-stu-id="694fd-128">This namespace contains the original solution for accessing WMI with managed code.</span></span> <span data-ttu-id="694fd-129">Sebbene le classi <a href="/dotnet/api/system.management">System. Management</a> siano ancora disponibili, le classi <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> sono in genere più efficienti e migliorano la scalabilità.</span><span class="sxs-lookup"><span data-stu-id="694fd-129">While the <a href="/dotnet/api/system.management">System.Management</a> classes are still available, the <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a> classes are generally more efficient and scale better.</span></span> <span data-ttu-id="694fd-130">È quindi consigliabile usare le classi MI, anziché le classi WMI originali.</span><span class="sxs-lookup"><span data-stu-id="694fd-130">As such, it is recommended that you use the MI classes, rather than the original WMI classes.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="694fd-131">C#</span><span class="sxs-lookup"><span data-stu-id="694fd-131">C#</span></span></th>
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



 

<span data-ttu-id="694fd-132">Nella tabella seguente sono elencati gli argomenti inclusi in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="694fd-132">The following table lists the topics covered in this section.</span></span>



| <span data-ttu-id="694fd-133">Argomento</span><span class="sxs-lookup"><span data-stu-id="694fd-133">Topic</span></span>                                                                                                        | <span data-ttu-id="694fd-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="694fd-134">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="694fd-135">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="694fd-135">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)                         | <span data-ttu-id="694fd-136">Viene descritto un numero di problemi che si verificano quando i client utilizzano l'infrastruttura WMI in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="694fd-136">Describes a number of issues that arise when clients use the WMI infrastructure on a remote computer.</span></span>                                                                                          |
| [<span data-ttu-id="694fd-137">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="694fd-137">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)                         | <span data-ttu-id="694fd-138">Mostra un esempio di codice client WMI.</span><span class="sxs-lookup"><span data-stu-id="694fd-138">Shows example WMI client code.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="694fd-139">Creazione di un'applicazione o di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="694fd-139">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)                             | <span data-ttu-id="694fd-140">Vengono fornite informazioni sulla creazione di diversi client WMI.</span><span class="sxs-lookup"><span data-stu-id="694fd-140">Provides information about creating various WMI clients.</span></span>                                                                                                                                       |
| [<span data-ttu-id="694fd-141">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="694fd-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)                                               | <span data-ttu-id="694fd-142">Viene descritto come utilizzare WMI per monitorare i dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="694fd-142">Describes how to use WMI to monitor performance data.</span></span>                                                                                                                                          |
| [<span data-ttu-id="694fd-143">Ricezione di un evento WMI</span><span class="sxs-lookup"><span data-stu-id="694fd-143">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)                                                           | <span data-ttu-id="694fd-144">Viene descritto come visualizzare gli eventi WMI.</span><span class="sxs-lookup"><span data-stu-id="694fd-144">Describes how to view WMI events.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="694fd-145">Monitoraggio degli eventi</span><span class="sxs-lookup"><span data-stu-id="694fd-145">Monitoring Events</span></span>](monitoring-events.md)                                                                   | <span data-ttu-id="694fd-146">Viene descritto come monitorare gli eventi WMI.</span><span class="sxs-lookup"><span data-stu-id="694fd-146">Describes how to monitor WMI events.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="694fd-147">Esecuzione di query con WQL</span><span class="sxs-lookup"><span data-stu-id="694fd-147">Querying with WQL</span></span>](querying-with-wql.md)                                                                   | <span data-ttu-id="694fd-148">Introduce la WMI Query Language (WQL).</span><span class="sxs-lookup"><span data-stu-id="694fd-148">Introduces the WMI Query Language (WQL).</span></span>                                                                                                                                                       |
| [<span data-ttu-id="694fd-149">Esecuzione di query sullo stato delle funzionalità facoltative</span><span class="sxs-lookup"><span data-stu-id="694fd-149">Querying the Status of Optional Features</span></span>](querying-the-status-of-optional-features.md)                     | <span data-ttu-id="694fd-150">In Windows 7, WMI ha implementato la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="694fd-150">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="694fd-151">Questa classe recupera lo stato delle funzionalità facoltative presenti in un computer.</span><span class="sxs-lookup"><span data-stu-id="694fd-151">This class retrieves the status of the optional features that are present on a computer.</span></span> |
| [<span data-ttu-id="694fd-152">Descrizione della posizione di un oggetto WMI</span><span class="sxs-lookup"><span data-stu-id="694fd-152">Describing the Location of a WMI Object</span></span>](describing-the-location-of-a-wmi-object.md)                       | <span data-ttu-id="694fd-153">Si concentra sulla sintassi per descrivere la posizione di un'entità gestita WMI.</span><span class="sxs-lookup"><span data-stu-id="694fd-153">Focuses on the syntax for describing the location of a WMI managed entity.</span></span>                                                                                                                     |
| [<span data-ttu-id="694fd-154">Accesso ad altre funzionalità del sistema operativo con WMI</span><span class="sxs-lookup"><span data-stu-id="694fd-154">Accessing Other Operating System Features with WMI</span></span>](accessing-other-operating-system-features-with-wmi.md) | <span data-ttu-id="694fd-155">Viene descritto come scrivere client WMI che accedono a driver di dispositivo, Active Directory e dispositivi SNMP.</span><span class="sxs-lookup"><span data-stu-id="694fd-155">Describes how to write WMI clients that access device drivers, Active Directory, and SNMP devices.</span></span>                                                                                             |
| [<span data-ttu-id="694fd-156">Accesso ai dati nello spazio dei nomi Interop</span><span class="sxs-lookup"><span data-stu-id="694fd-156">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)                       | <span data-ttu-id="694fd-157">I provider di associazioni consentono ai client di Strumentazione gestione Windows (WMI) di attraversare e recuperare i profili e le istanze di classe associate da spazi dei nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="694fd-157">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>                      |
| [<span data-ttu-id="694fd-158">Modifica delle informazioni sulle classi e sulle istanze</span><span class="sxs-lookup"><span data-stu-id="694fd-158">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)               | <span data-ttu-id="694fd-159">Descrive le attività comuni che i client WMI devono eseguire.</span><span class="sxs-lookup"><span data-stu-id="694fd-159">Describes the common tasks that WMI clients must perform.</span></span>                                                                                                                                      |
| [<span data-ttu-id="694fd-160">Collegamento di classi</span><span class="sxs-lookup"><span data-stu-id="694fd-160">Linking Classes Together</span></span>](linking-classes-together.md)                                                     | <span data-ttu-id="694fd-161">Viene illustrato il provider di viste e il modo in cui può essere utilizzato per riunire le informazioni da più classi WMI.</span><span class="sxs-lookup"><span data-stu-id="694fd-161">Discusses the view provider and how it can be used to bring together information from multiple WMI classes.</span></span>                                                                                    |
| [<span data-ttu-id="694fd-162">Modifica del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="694fd-162">Modifying the System Registry</span></span>](modifying-the-system-registry.md)                                           | <span data-ttu-id="694fd-163">Viene descritto come i client WMI possono utilizzare WMI per gestire le informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="694fd-163">Describes how WMI clients can use WMI to manage system registry information.</span></span>                                                                                                                   |



 

