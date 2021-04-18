---
description: Le attività WMI per i servizi ottengono informazioni sui servizi, inclusi i servizi dipendenti o precedenti. Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo https://www.microsoft.com/technet .
ms.assetid: 1cd92981-c074-4ff7-a32c-ce492e6d6aa5
ms.tgt_platform: multiple
title: 'Attività WMI: Servizi'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b786ce0e358a59922728be4e90bc8cdeaa37a298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316557"
---
# <a name="wmi-tasks-services"></a><span data-ttu-id="8c671-104">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="8c671-104">WMI Tasks: Services</span></span>

<span data-ttu-id="8c671-105">Le attività WMI per i servizi ottengono informazioni sui servizi, inclusi i servizi dipendenti o precedenti.</span><span class="sxs-lookup"><span data-stu-id="8c671-105">WMI tasks for services obtain information about services, including dependent or antecedent services.</span></span> <span data-ttu-id="8c671-106">Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8c671-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="8c671-107">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="8c671-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="8c671-108">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="8c671-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="8c671-109">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="8c671-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="8c671-110">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="8c671-110">**To run a script**</span></span>

1.  <span data-ttu-id="8c671-111">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="8c671-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="8c671-112">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="8c671-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="8c671-113">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="8c671-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="8c671-114">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="8c671-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="8c671-115">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="8c671-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="8c671-116">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="8c671-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="8c671-117">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="8c671-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="8c671-118">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="8c671-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="8c671-119">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="8c671-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="8c671-120">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="8c671-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>




<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c671-121">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="8c671-121">How do I...</span></span></th>
<th><span data-ttu-id="8c671-122">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="8c671-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c671-123">... determinare quali servizi sono in esecuzione e quali no?</span><span class="sxs-lookup"><span data-stu-id="8c671-123">...determine which services are running and which ones are not?</span></span></td>
<td><span data-ttu-id="8c671-124">Utilizzare la classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> per verificare lo stato di tutti i servizi.</span><span class="sxs-lookup"><span data-stu-id="8c671-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class to check the state of all of the services.</span></span> <span data-ttu-id="8c671-125">La proprietà state indica se un servizio è stato interrotto o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8c671-125">The state property lets you know if a service is stopped or running.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c671-126">VB</span><span class="sxs-lookup"><span data-stu-id="8c671-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Service&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;Service Name: &quot; & objItem.Name & VBNewLine & &quot;State: &quot; & objItem.State
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
<th><span data-ttu-id="8c671-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c671-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | format-list Name, State</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c671-128">... arrestare l'avvio di determinati servizi da parte di Power Users?</span><span class="sxs-lookup"><span data-stu-id="8c671-128">...stop Power Users from starting certain services?</span></span></td>
<td><p><span data-ttu-id="8c671-129">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> per impostare la proprietà <strong>StartMode</strong> su Disabled.</span><span class="sxs-lookup"><span data-stu-id="8c671-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> method to set the <strong>StartMode</strong> property to Disabled.</span></span> <span data-ttu-id="8c671-130">I servizi disabilitati non possono essere avviati e, per impostazione predefinita, Power Users non può modificare la modalità di avvio di un servizio.</span><span class="sxs-lookup"><span data-stu-id="8c671-130">Disabled services cannot be started, and, by default, Power Users cannot change the start mode of a service.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c671-131">VB</span><span class="sxs-lookup"><span data-stu-id="8c671-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service where StartMode = &#39;Manual&#39;&quot;)
For Each objService in colServiceList
    errReturnCode = objService.Change( , , , , &quot;Disabled&quot;)
    WScript.Echo &quot;Changed manual service to disabled: &quot; & objService.Name   
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
<th><span data-ttu-id="8c671-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c671-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.startMode -eq &quot;Manual&quot;} | `
    foreach-object { [void]$_.changeStartMode(&#39;Disabled&#39;) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c671-133">... avviare e arrestare i servizi?</span><span class="sxs-lookup"><span data-stu-id="8c671-133">...start and stop services?</span></span></td>
<td><p><span data-ttu-id="8c671-134">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> e i metodi <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>StopService</strong></a> e <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c671-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>StopService</strong></a> and <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c671-135">VB</span><span class="sxs-lookup"><span data-stu-id="8c671-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colListOfServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where Name =&#39;Alerter&#39;&quot;)
For Each objService in colListOfServices
    objService.StartService()
    Wscript.Echo &quot;Started Alerter service&quot;
Next
</code></pre></td>
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
<th><span data-ttu-id="8c671-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c671-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.Name -eq &quot;Alerter&quot;} | `
    foreach-object { [void]$_.StartService() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c671-137">... modificare le password degli account del servizio utilizzando uno script?</span><span class="sxs-lookup"><span data-stu-id="8c671-137">...change service account passwords using a script?</span></span></td>
<td><p><span data-ttu-id="8c671-138">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Change</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8c671-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Change</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c671-139">VB</span><span class="sxs-lookup"><span data-stu-id="8c671-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service&quot;)
For Each objservice in colServiceList
    If objService.StartName = &quot;.\netsvc&quot; Then
        errReturn = objService.Change( , , , , , , , &quot;password&quot;)  
    End If 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c671-140">.. determinare quali servizi posso arrestare?</span><span class="sxs-lookup"><span data-stu-id="8c671-140">..determine which services I can stop?</span></span></td>
<td><p><span data-ttu-id="8c671-141">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> e controllare il valore della proprietà <strong>AcceptStop</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c671-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class, and check the value of the <strong>AcceptStop</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c671-142">VB</span><span class="sxs-lookup"><span data-stu-id="8c671-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where AcceptStop = True&quot;)
For Each objService in colServices
    Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="8c671-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c671-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.AcceptStop -eq &quot;True&quot;} | `
     format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c671-144">... individuare i servizi che devono essere in esecuzione prima di poter avviare il servizio DHCP?</span><span class="sxs-lookup"><span data-stu-id="8c671-144">...find the services that must be running before I can start the DHCP service?</span></span></td>
<td><p><span data-ttu-id="8c671-145">Eseguire una query per gli <a href="associators-of-statement.md">associatori della</a> classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> denominata &quot; DHCP &quot; che si trovano nella classe <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> e che &quot; dipendono dalla &quot; proprietà <strong>Role</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c671-145">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Dependent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="8c671-146"><strong>Role</strong> indica il ruolo del servizio DHCP: in questo caso, dipende dagli altri servizi in fase di avvio.</span><span class="sxs-lookup"><span data-stu-id="8c671-146"><strong>Role</strong> means the role of the DHCP service: in this case, it is dependent on the other services that are being started.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c671-147">VB</span><span class="sxs-lookup"><span data-stu-id="8c671-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery(&quot;Associators Of &quot; _ 
    & &quot;{Win32_Service.Name=&#39;dhcp&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Dependent&quot;) 
For Each objService in colServiceList
Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="8c671-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c671-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators Of {Win32_Service.Name=&#39;dhcp&#39;} Where AssocClass=Win32_DependentService Role=Dependent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c671-149">... individuare i servizi per i quali è necessario che il servizio WMI (Winmgmt) sia in esecuzione prima di poter iniziare?</span><span class="sxs-lookup"><span data-stu-id="8c671-149">...find the services that require the WMI service (Winmgmt) service to be running before they can start?</span></span></td>
<td><p><span data-ttu-id="8c671-150">Eseguire una query per gli <a href="associators-of-statement.md">associatori della</a> classe <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> denominata &quot; DHCP &quot; che si trovano nella classe <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> e hanno &quot; antecendent &quot; nella proprietà <strong>Role</strong> .</span><span class="sxs-lookup"><span data-stu-id="8c671-150">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Antecendent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="8c671-151"><strong>Role</strong> indica il ruolo del servizio RASMAN: in questo caso, è necessario avviare prima i servizi dipendenti.</span><span class="sxs-lookup"><span data-stu-id="8c671-151"><strong>Role</strong> means the role of the rasman service: in this case, it is antecedent to must be started before the dependent services.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c671-152">VB</span><span class="sxs-lookup"><span data-stu-id="8c671-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\ & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = _
    objWMIService.ExecQuery(&quot;Associators of &quot; _
    & &quot;{Win32_Service.Name=&#39;winmgmt&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Antecedent&quot; )
For Each objService in colServiceList
Wscript.Echo &quot;Name: &quot; & objService.Name & VBTab & &quot;Display Name: &quot; & objService.DisplayName 
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
<th><span data-ttu-id="8c671-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c671-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators of {Win32_Service.Name=&#39;winmgmt&#39;} Where AssocClass=Win32_DependentService Role=Antecedent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list Name, DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8c671-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c671-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c671-155">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="8c671-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="8c671-156">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="8c671-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="8c671-157">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="8c671-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
