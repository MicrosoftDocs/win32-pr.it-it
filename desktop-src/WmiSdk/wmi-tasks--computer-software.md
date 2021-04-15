---
description: Le attività WMI per il software per computer ottengono informazioni quali il software installato dalle Microsoft Windows Installer (MSI) e le versioni del software. Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo https://www.microsoft.com/technet .
ms.assetid: 65a61be3-7870-4178-9e96-78b82898271f
ms.tgt_platform: multiple
title: 'Attività WMI: software per computer'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 800a42764cbb1b9552a8ecc87debc04685d28850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530073"
---
# <a name="wmi-tasks-computer-software"></a><span data-ttu-id="1a42f-104">Attività WMI: software per computer</span><span class="sxs-lookup"><span data-stu-id="1a42f-104">WMI Tasks: Computer Software</span></span>

<span data-ttu-id="1a42f-105">Le attività WMI per il software per computer ottengono informazioni quali il software installato dalle Microsoft Windows Installer (MSI) e le versioni del software.</span><span class="sxs-lookup"><span data-stu-id="1a42f-105">WMI tasks for computer software obtain information such as which software is installed by the Microsoft Windows Installer (MSI) and software versions.</span></span> <span data-ttu-id="1a42f-106">Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1a42f-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="1a42f-107">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="1a42f-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="1a42f-108">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="1a42f-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="1a42f-109">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="1a42f-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="1a42f-110">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="1a42f-110">**To run a script**</span></span>

1.  <span data-ttu-id="1a42f-111">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="1a42f-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="1a42f-112">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="1a42f-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="1a42f-113">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="1a42f-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="1a42f-114">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1a42f-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="1a42f-115">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="1a42f-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="1a42f-116">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="1a42f-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="1a42f-117">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1a42f-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="1a42f-118">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="1a42f-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="1a42f-119">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="1a42f-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a42f-120">L'esecuzione di una \* query "Select from Win32 \_ Product" può causare un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1a42f-120">Running a "Select \* from Win32\_Product" query may result in unexpected behavior.</span></span> <span data-ttu-id="1a42f-121">Questo perché il provider che supporta il \_ prodotto Win32 non è ottimizzato per la query.</span><span class="sxs-lookup"><span data-stu-id="1a42f-121">This is because the provider that supports Win32\_Product is not query optimized.</span></span> <span data-ttu-id="1a42f-122">Per ulteriori informazioni, vedere l' [articolo KB 974524](https://support.microsoft.com/kb/974524).</span><span class="sxs-lookup"><span data-stu-id="1a42f-122">For more information, see [KB Article 974524](https://support.microsoft.com/kb/974524).</span></span>

 

<span data-ttu-id="1a42f-123">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="1a42f-123">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a42f-124">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="1a42f-124">How do I...</span></span></th>
<th><span data-ttu-id="1a42f-125">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="1a42f-125">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a42f-126">... disinstallare il software utilizzando uno script?</span><span class="sxs-lookup"><span data-stu-id="1a42f-126">...uninstall software using a script?</span></span></td>
<td><span data-ttu-id="1a42f-127">Se il software è stato installato tramite Microsoft Windows Installer (MSI), utilizzare la classe WMI <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> e il metodo di <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>disinstallazione</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="1a42f-127">If the software was installed using Microsoft Windows Installer (MSI), use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> and the <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> method.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a42f-128">VB</span><span class="sxs-lookup"><span data-stu-id="1a42f-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product &quot; _
        & &quot;Where Name = &#39;Personnel database&#39;&quot;)
For Each objSoftware in colSoftware
    objSoftware.Uninstall()
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
<th><span data-ttu-id="1a42f-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a42f-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.name -eq &quot;Personnel database&quot;}

foreach ($colItem in $colSoftware)
{
    $colItem.Uninstall()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a42f-130">... inventario di tutto il software installato in un computer con uno script?</span><span class="sxs-lookup"><span data-stu-id="1a42f-130">...inventory all the software installed on a computer with a script?</span></span></td>
<td><p><span data-ttu-id="1a42f-131">Se il software è stato installato tramite Microsoft Windows Installer (MSI), utilizzare la classe WMI <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1a42f-131">If the software was installed using Microsoft Windows Installer (MSI) use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a42f-132">VB</span><span class="sxs-lookup"><span data-stu-id="1a42f-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product&quot;)

For Each objSoftware in colSoftware
    Wscript.Echo &quot;Name: &quot; & objSoftware.Name
    Wscript.Echo &quot;Version: &quot; & objSoftware.Version
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
<th><span data-ttu-id="1a42f-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a42f-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot;+ $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a42f-134">... determinare quale versione di Microsoft Office è installata?</span><span class="sxs-lookup"><span data-stu-id="1a42f-134">...determine what version of Microsoft Office is installed?</span></span></td>
<td><p><span data-ttu-id="1a42f-135">Usare la classe <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> e controllare il valore della proprietà <strong>Version</strong> .</span><span class="sxs-lookup"><span data-stu-id="1a42f-135">Use the <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> class and check the value of the <strong>Version</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a42f-136">VB</span><span class="sxs-lookup"><span data-stu-id="1a42f-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery(_
    &quot;Select * from Win32_Product &quot; & _
    &quot;Where IdentifyingNumber =&quot; _
        & &quot; &#39;{90280409-6000-11D3-8CFE-0050048383C9}&#39;&quot;)
For Each objItem in colSoftware
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Version: &quot; & objItem.Version
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
<th><span data-ttu-id="1a42f-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a42f-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.IdentifyingNumber -eq &quot;{90280409-6000-11D3-8CFE-0050048383C9}&quot;}

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot; + $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="1a42f-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="1a42f-138">Examples</span></span>

<span data-ttu-id="1a42f-139">L'esempio di codice PowerShell [Remote PC info script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) PowerShell usa una serie di classi hardware e software, tra cui Win32Product, per trovare varie informazioni su un computer remoto tramite WMI e il registro di sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="1a42f-139">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) PowerShell code sample uses a number of hardware and software classes, including Win32Product, to find various information about a remote PC using WMI and the remote registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a42f-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a42f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a42f-141">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="1a42f-141">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="1a42f-142">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="1a42f-142">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="1a42f-143">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="1a42f-143">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

