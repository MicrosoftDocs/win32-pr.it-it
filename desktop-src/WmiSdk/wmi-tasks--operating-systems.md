---
description: Le attività WMI per i sistemi operativi ottengono informazioni sul sistema operativo, ad esempio la versione, se è attivato o quali hotfix sono installati.
ms.assetid: a216ad56-2650-4d93-86e1-449b56019361
ms.tgt_platform: multiple
title: 'Attività WMI: sistemi operativi'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8d4dff83cebf5fd3336aeec2cc45ac4d8498cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318154"
---
# <a name="wmi-tasks-operating-systems"></a><span data-ttu-id="13c5a-103">Attività WMI: sistemi operativi</span><span class="sxs-lookup"><span data-stu-id="13c5a-103">WMI Tasks: Operating Systems</span></span>

<span data-ttu-id="13c5a-104">Le attività WMI per i sistemi operativi ottengono informazioni sul sistema operativo, ad esempio la versione, se è attivato o quali hotfix sono installati.</span><span class="sxs-lookup"><span data-stu-id="13c5a-104">WMI tasks for operating systems obtain information about the operating system, such as version, whether it is activated, or which hotfixes are installed.</span></span>

<span data-ttu-id="13c5a-105">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="13c5a-105">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="13c5a-106">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="13c5a-106">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="13c5a-107">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="13c5a-107">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="13c5a-108">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="13c5a-108">**To run a script**</span></span>

1.  <span data-ttu-id="13c5a-109">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="13c5a-109">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="13c5a-110">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="13c5a-110">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="13c5a-111">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="13c5a-111">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="13c5a-112">Digitare **CScript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="13c5a-112">Type **CScript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="13c5a-113">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="13c5a-113">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="13c5a-114">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="13c5a-114">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="13c5a-115">Per impostazione predefinita, CScript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="13c5a-115">By default, CScript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="13c5a-116">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="13c5a-116">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="13c5a-117">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="13c5a-117">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="13c5a-118">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="13c5a-118">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13c5a-119">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="13c5a-119">How do I...</span></span></th>
<th><span data-ttu-id="13c5a-120">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="13c5a-120">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13c5a-121">... determinare se un Service Pack è stato installato in un computer?</span><span class="sxs-lookup"><span data-stu-id="13c5a-121">...determine if a service pack has been installed on a computer?</span></span></td>
<td><span data-ttu-id="13c5a-122">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e controllare il valore delle proprietà <strong>ServicePackMajorVersion</strong> e <strong>ServicePackMinorVersion</strong> .</span><span class="sxs-lookup"><span data-stu-id="13c5a-122">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and check the value of the <strong>ServicePackMajorVersion</strong> and <strong>ServicePackMinorVersion</strong> properties.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13c5a-123">VB</span><span class="sxs-lookup"><span data-stu-id="13c5a-123">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.ServicePackMajorVersion & &quot;.&quot; & objOperatingSystem.ServicePackMinorVersion
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
<th><span data-ttu-id="13c5a-124">PowerShell</span><span class="sxs-lookup"><span data-stu-id="13c5a-124">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | `
   format-list ServicePackMajorVersion, ServicePackMinorVersion</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="13c5a-125">... determinare quando il sistema operativo è stato installato in un computer?</span><span class="sxs-lookup"><span data-stu-id="13c5a-125">...determine when the operating system was installed on a computer?</span></span></td>
<td><p><span data-ttu-id="13c5a-126">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e la proprietà <strong>InstallDate</strong> .</span><span class="sxs-lookup"><span data-stu-id="13c5a-126">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>InstallDate</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13c5a-127">VB</span><span class="sxs-lookup"><span data-stu-id="13c5a-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Install Date: &quot; & objOperatingSystem.InstallDate 
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
<th><span data-ttu-id="13c5a-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="13c5a-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list InstallDate</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13c5a-129">... determinare quale versione del sistema operativo Windows è installata in un computer?</span><span class="sxs-lookup"><span data-stu-id="13c5a-129">...determine which version of the Windows operating system is installed on a computer?</span></span></td>
<td><p><span data-ttu-id="13c5a-130">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e recuperare le proprietà <strong>Name</strong> e <strong>Version</strong> .</span><span class="sxs-lookup"><span data-stu-id="13c5a-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and retrieve both the <strong>Name</strong> and <strong>Version</strong> properties.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13c5a-131">VB</span><span class="sxs-lookup"><span data-stu-id="13c5a-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.Caption & &quot;  &quot; & objOperatingSystem.Version
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
<th><span data-ttu-id="13c5a-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="13c5a-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list Caption, Version</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13c5a-133">... determinare quale cartella è la cartella Windows (% windir%) in un computer?</span><span class="sxs-lookup"><span data-stu-id="13c5a-133">...determine which folder is the Windows folder (%Windir%) on a computer?</span></span></td>
<td><p><span data-ttu-id="13c5a-134">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> e controllare il valore della proprietà <strong>WindowsDirectory</strong> .</span><span class="sxs-lookup"><span data-stu-id="13c5a-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and check the value of the <strong>WindowsDirectory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13c5a-135">VB</span><span class="sxs-lookup"><span data-stu-id="13c5a-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Windows Folder: &quot; & objOperatingSystem.WindowsDirectory
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
<th><span data-ttu-id="13c5a-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="13c5a-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list WindowsDirectory</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13c5a-137">... determinare quali hotfix sono stati installati in un computer?</span><span class="sxs-lookup"><span data-stu-id="13c5a-137">...determine what hotfixes have been installed on a computer?</span></span></td>
<td><p><span data-ttu-id="13c5a-138">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="13c5a-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13c5a-139">VB</span><span class="sxs-lookup"><span data-stu-id="13c5a-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuickFixes = objWMIService.ExecQuery (&quot;Select * from Win32_QuickFixEngineering&quot;)
For Each objQuickFix in colQuickFixes
    Wscript.Echo &quot;Description: &quot; & objQuickFix.Description
    Wscript.Echo &quot;Hotfix ID: &quot; & objQuickFix.HotFixID
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
<th><span data-ttu-id="13c5a-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="13c5a-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_QuickFixEngineering -Namespace &quot;root\cimv2&quot; | format-list Description, HotFixIDs</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13c5a-141">... determinare se è necessario attivare il sistema operativo in un computer?</span><span class="sxs-lookup"><span data-stu-id="13c5a-141">...determine if I need to activate the operating system on a computer?</span></span></td>
<td><p><span data-ttu-id="13c5a-142">Usare la classe <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> e controllare il valore della proprietà <strong>ActivationRequired</strong> .</span><span class="sxs-lookup"><span data-stu-id="13c5a-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> class and check the value of the <strong>ActivationRequired</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13c5a-143">VB</span><span class="sxs-lookup"><span data-stu-id="13c5a-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colWPA = objWMIService.ExecQuery (&quot;Select * from Win32_WindowsProductActivation&quot;)
For Each objWPA in colWPA
    Wscript.Echo &quot;Activation Required: &quot; & objWPA.ActivationRequired
    Wscript.Echo &quot;Remaining Evaluation Period: &quot; & objWPA.RemainingEvaluationPeriod
    Wscript.Echo &quot;Remaining Grace Period: &quot; & objWPA.RemainingGracePeriod
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
<th><span data-ttu-id="13c5a-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="13c5a-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_WindowsProductActivation -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | `
     format-list ActivationRequired, RemainingEvaluationPeriod, RemainingGracePeriod</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="13c5a-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13c5a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13c5a-146">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="13c5a-146">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="13c5a-147">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="13c5a-147">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="13c5a-148">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="13c5a-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

