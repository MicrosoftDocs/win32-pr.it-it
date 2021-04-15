---
description: Le attività WMI per i processi ottengono informazioni come l'account con cui viene eseguito un processo. È possibile eseguire azioni come la creazione di processi. Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo https://www.microsoft.com/technet .
ms.assetid: 2ae7c302-ab8b-4150-8ece-ffb66374b3f7
ms.tgt_platform: multiple
title: 'Attività WMI: processi '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a720046d8f5cd25c55f2d5f367d2c23d5e4fc882
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104485933"
---
# <a name="wmi-tasks-processes"></a><span data-ttu-id="00267-105">Attività WMI: processi </span><span class="sxs-lookup"><span data-stu-id="00267-105">WMI Tasks: Processes</span></span>

<span data-ttu-id="00267-106">Le attività WMI per i processi ottengono informazioni come l'account con cui viene eseguito un processo.</span><span class="sxs-lookup"><span data-stu-id="00267-106">WMI tasks for processes obtain information such as the account under which a process is running.</span></span> <span data-ttu-id="00267-107">È possibile eseguire azioni come la creazione di processi.</span><span class="sxs-lookup"><span data-stu-id="00267-107">You can perform actions like creating processes.</span></span> <span data-ttu-id="00267-108">Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="00267-108">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="00267-109">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="00267-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="00267-110">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="00267-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="00267-111">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="00267-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="00267-112">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="00267-112">**To run a script**</span></span>

1.  <span data-ttu-id="00267-113">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="00267-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="00267-114">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="00267-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="00267-115">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="00267-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="00267-116">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="00267-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="00267-117">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="00267-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="00267-118">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="00267-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="00267-119">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="00267-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="00267-120">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="00267-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="00267-121">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="00267-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="00267-122">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="00267-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00267-123">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="00267-123">How do I...</span></span></th>
<th><span data-ttu-id="00267-124">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="00267-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00267-125">... eseguire un'applicazione in una finestra nascosta?</span><span class="sxs-lookup"><span data-stu-id="00267-125">...run an application in a hidden window?</span></span></td>
<td><span data-ttu-id="00267-126">Chiamare l'applicazione da uno script che utilizza le classi <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="00267-126">Call the application from a script that uses the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> and <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> classes.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00267-127">VB</span><span class="sxs-lookup"><span data-stu-id="00267-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HIDDEN_WINDOW = 0
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objStartup = objWMIService.Get(&quot;Win32_ProcessStartup&quot;)
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject(&quot;winmgmts:root\cimv2:Win32_Process&quot;)
errReturn = objProcess.Create( &quot;Notepad.exe&quot;, null, objConfig, intProcessID)</code></pre></td>
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
<th><span data-ttu-id="00267-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="00267-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$startup=[wmiclass]&quot;Win32_ProcessStartup&quot;
$startup.Properties[&#39;ShowWindow&#39;].value=$False
([wmiclass]&quot;win32_Process&quot;).create(&#39;notepad.exe&#39;,&#39;C:\&#39;,$Startup)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="00267-129">... determinare quali script sono in esecuzione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="00267-129">...determine which scripts are running on the local computer?</span></span></td>
<td><p><span data-ttu-id="00267-130">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e restituire tutti i processi con il nome Cscript.exe o Wscript.exe.</span><span class="sxs-lookup"><span data-stu-id="00267-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and return all processes with the name Cscript.exe or Wscript.exe.</span></span> <span data-ttu-id="00267-131">Per determinare i singoli script in esecuzione in questi processi, controllare il valore della proprietà <strong>CommandLine</strong> .</span><span class="sxs-lookup"><span data-stu-id="00267-131">To determine the individual scripts running in these processes, check the value of the <strong>CommandLine</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00267-132">VB</span><span class="sxs-lookup"><span data-stu-id="00267-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Process&quot; & _
           &quot; WHERE Name = &#39;cscript.exe&#39;&quot; & &quot; OR Name = &#39;wscript.exe&#39;&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;-------------------------------------------&quot;
    Wscript.Echo &quot;CommandLine: &quot; & objItem.CommandLine
    Wscript.Echo &quot;Name: &quot; & objItem.Name
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
<th><span data-ttu-id="00267-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="00267-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32_Process&quot; -ComputerName &quot;.&quot; | `
     where {($_.name -eq &#39;cscript.exe&#39;) -or ($_.name -eq &#39;wscript.exe&#39;) } | `
     Format-List -Property CommandLine, Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00267-134">... individuare il nome dell'account con cui viene eseguito un processo.</span><span class="sxs-lookup"><span data-stu-id="00267-134">...find out the account name under which a process is running?</span></span></td>
<td><p><span data-ttu-id="00267-135">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="00267-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00267-136">VB</span><span class="sxs-lookup"><span data-stu-id="00267-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    colProperties = objProcess.GetOwner( strNameOfUser,strUserDomain)
    Wscript.Echo &quot;Process &quot; & objProcess.Name & &quot; is owned by &quot; & strUserDomain & &quot;\&quot; & strNameOfUser & &quot;.&quot;
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
<th><span data-ttu-id="00267-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="00267-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -class win32_process -ComputerName &quot;.&quot; | ForEach-Object { $_.GetOwner() | Select -Property domain, user }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00267-138">... modificare la priorità di un processo in esecuzione?</span><span class="sxs-lookup"><span data-stu-id="00267-138">...change the priority of a running process?</span></span></td>
<td><p><span data-ttu-id="00267-139">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>sepriority</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="00267-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>SetPriority</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00267-140">VB</span><span class="sxs-lookup"><span data-stu-id="00267-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const ABOVE_NORMAL = 32768
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcesses
    objProcess.SetPriority(ABOVE_NORMAL) 
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
<th><span data-ttu-id="00267-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="00267-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$ABOVE_NORMAL = 32768
$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.SetPriority($ABOVE_NORMAL) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00267-142">... terminare un processo usando uno script?</span><span class="sxs-lookup"><span data-stu-id="00267-142">...terminate a process using a script?</span></span></td>
<td><p><span data-ttu-id="00267-143">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="00267-143">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00267-144">VB</span><span class="sxs-lookup"><span data-stu-id="00267-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcessList
    objProcess.Terminate()
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
<th><span data-ttu-id="00267-145">PowerShell</span><span class="sxs-lookup"><span data-stu-id="00267-145">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.Terminate() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00267-146">... determinare la quantità di tempo processore e memoria utilizzata da ogni processo.</span><span class="sxs-lookup"><span data-stu-id="00267-146">...determine how much processor time and memory each process is using?</span></span></td>
<td><p><span data-ttu-id="00267-147">Usare la classe e le proprietà <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> , ad esempio <strong>KernelModeTime</strong>, <strong>WorkingSetSize</strong>, <strong>PageFileUsage</strong>e <strong>PageFaults</strong>.</span><span class="sxs-lookup"><span data-stu-id="00267-147">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class and properties such as <strong>KernelModeTime</strong>, <strong>WorkingSetSize</strong>, <strong>PageFileUsage</strong>, and <strong>PageFaults</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00267-148">VB</span><span class="sxs-lookup"><span data-stu-id="00267-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery(&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcesses
    Wscript.Echo &quot;Process: &quot; & objProcess.Name
    sngProcessTime = (CSng(objProcess.KernelModeTime) + CSng(objProcess.UserModeTime)) / 10000000
    Wscript.Echo &quot;Processor Time: &quot; & sngProcessTime
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults
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
<th><span data-ttu-id="00267-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="00267-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32s_Process&quot; -ComputerName $strComputer | `
     Format-List -Property Name, KernelModeTime, UserModeTime, ProcessID, WorkingSetSize, PageFileUsage, PageFaults</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00267-150">... indicare le applicazioni in esecuzione in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="00267-150">...tell what applications are running on a remote computer?</span></span></td>
<td><p><span data-ttu-id="00267-151">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="00267-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00267-152">VB</span><span class="sxs-lookup"><span data-stu-id="00267-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process: &quot; & objProcess.Name 
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID 
    Wscript.Echo &quot;Thread Count: &quot; & objProcess.ThreadCount 
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage 
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults 
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize 
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
<th><span data-ttu-id="00267-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="00267-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
get-wmiObject -class Win32_Process -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
   Format-list Name, ProcessID, ThreadCount, PageFileUsage, PageFaults, WorkingSetSize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="00267-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00267-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00267-155">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="00267-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="00267-156">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="00267-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="00267-157">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="00267-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

