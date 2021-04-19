---
description: Le attività WMI per file e cartelle modificano le proprietà del file o della cartella tramite WMI, inclusa la creazione di una condivisione o la ridenominazione di un file.
ms.assetid: 91281fe1-0461-48da-ac5c-cab7e8e1b285
ms.tgt_platform: multiple
title: 'Attività WMI: file e cartelle'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b24d5f7708b88507cd08b73c0b08a83c94f6bb28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318155"
---
# <a name="wmi-tasks-files-and-folders"></a><span data-ttu-id="71cf0-103">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="71cf0-103">WMI Tasks: Files and Folders</span></span>

<span data-ttu-id="71cf0-104">Le attività WMI per file e cartelle modificano le proprietà del file o della cartella tramite WMI, inclusa la creazione di una condivisione o la ridenominazione di un file.</span><span class="sxs-lookup"><span data-stu-id="71cf0-104">WMI tasks for files and folders change file or folder properties through WMI, including creating a share or renaming a file.</span></span> <span data-ttu-id="71cf0-105">Se si desidera copiare un file o leggere e scrivere un file, il modo più semplice consiste nell'utilizzare Windows script host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) invece di WMI.</span><span class="sxs-lookup"><span data-stu-id="71cf0-105">If you want to copy a file or read and write a file, the easiest way is to use the Windows Script Host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) rather than WMI.</span></span> <span data-ttu-id="71cf0-106">Per altri esempi, vedere la sezione [file e cartelle](/previous-versions/tn-archive/ee176985(v=technet.10)) di [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span><span class="sxs-lookup"><span data-stu-id="71cf0-106">For other examples, see the [Files and Folders](/previous-versions/tn-archive/ee176985(v=technet.10)) section of the [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span></span>

<span data-ttu-id="71cf0-107">[**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) è una delle poche [classi CIM](cimclas.md) di WMI implementate.</span><span class="sxs-lookup"><span data-stu-id="71cf0-107">[**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) is one of the few [CIM classes](cimclas.md) in WMI that is implemented.</span></span> <span data-ttu-id="71cf0-108">Evitare l'enumerazione o l'esecuzione di query per tutte le istanze del file di dati CIM in un computer perché il volume di dati potrebbe influire negativamente sulle prestazioni o causare l'interruzione della risposta del computer. **\_**</span><span class="sxs-lookup"><span data-stu-id="71cf0-108">Avoid enumerating or querying for all instances of **CIM\_DataFile** on a computer because the volume of data is likely to either affect performance or cause the computer to stop responding.</span></span>

<span data-ttu-id="71cf0-109">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="71cf0-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="71cf0-110">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="71cf0-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="71cf0-111">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="71cf0-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="71cf0-112">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="71cf0-112">**To run a script**</span></span>

1.  <span data-ttu-id="71cf0-113">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="71cf0-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="71cf0-114">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="71cf0-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="71cf0-115">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="71cf0-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="71cf0-116">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="71cf0-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="71cf0-117">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="71cf0-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="71cf0-118">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="71cf0-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="71cf0-119">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="71cf0-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="71cf0-120">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="71cf0-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="71cf0-121">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="71cf0-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="71cf0-122">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="71cf0-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71cf0-123">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="71cf0-123">How do I...</span></span></th>
<th><span data-ttu-id="71cf0-124">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="71cf0-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71cf0-125">... rinominare un file senza ricevere un messaggio di errore?</span><span class="sxs-lookup"><span data-stu-id="71cf0-125">...rename a file without getting an error message?</span></span></td>
<td><span data-ttu-id="71cf0-126">Usare la classe <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="71cf0-126">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class.</span></span> <span data-ttu-id="71cf0-127">Assicurarsi di passare l'intero nome di percorso quando si chiama il metodo <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> , ad esempio &quot;C:\Scripts\Test.txt&quot; anziché &quot;Text.txt&quot; .</span><span class="sxs-lookup"><span data-stu-id="71cf0-127">Ensure that you pass the entire path name when calling the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> method, for example, &quot;C:\Scripts\Test.txt&quot; instead of &quot;Text.txt&quot;.</span></span> <span data-ttu-id="71cf0-128">Per PowerShell, l'uso di <strong>CIM_Datafile</strong> può risultare inefficiente.</span><span class="sxs-lookup"><span data-stu-id="71cf0-128">For PowerShell, using <strong>CIM_DataFile</strong> may be inefficient.</span></span> <span data-ttu-id="71cf0-129">Di conseguenza, è possibile usare semplicemente il cmdlet Rename-Item.</span><span class="sxs-lookup"><span data-stu-id="71cf0-129">As such, you may simply use the Rename-Item cmdlet.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71cf0-130">VB</span><span class="sxs-lookup"><span data-stu-id="71cf0-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery (&quot;Select * from CIM_DataFile where Name = &quot; & &quot;&#39;c:\\scripts\\toggle_service.vbs&#39;&quot;)
For Each objFile in colFiles
    errResult = objFile.Rename(&quot;c:\scripts\toggle_service.old&quot;)
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
<th><span data-ttu-id="71cf0-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="71cf0-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>rename-item c:\scripts\toggle_service.vbs toggle_service.old</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="71cf0-132">... determinare se gli utenti hanno. File MP3 archiviati nel computer?</span><span class="sxs-lookup"><span data-stu-id="71cf0-132">...determine whether users have .MP3 files stored on their computer?</span></span></td>
<td><p><span data-ttu-id="71cf0-133">Usare la classe <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> e selezionare i file usando la clausola <strong>where</strong> di <a href="querying-with-wql.md">WQL</a> seguente: where Extension = &quot; MP3 &quot; .</span><span class="sxs-lookup"><span data-stu-id="71cf0-133">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class and select files using the following <a href="querying-with-wql.md">WQL</a> <strong>WHERE</strong> clause: Where Extension = &quot;MP3&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71cf0-134">VB</span><span class="sxs-lookup"><span data-stu-id="71cf0-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery(&quot;Select * from CIM_DataFile where Extension = &#39;mp3&#39;&quot;)
For Each objFile in colFiles
    Wscript.Echo &quot;File Name: &quot; & objFile.Name & &quot;.&quot; & objFile.Extension
    Wscript.Echo &quot;Path: &quot; & objFile.Path
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
<th><span data-ttu-id="71cf0-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="71cf0-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class CIM_DataFile -namespace &quot;root\cimv2&quot; -Filter &quot;Extension = &#39;mp3&#39;&quot; | `
   format-list Name, Extension, Path</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71cf0-136">... creazione di cartelle condivise in un computer</span><span class="sxs-lookup"><span data-stu-id="71cf0-136">...create shared folders on a computer?</span></span></td>
<td><p><span data-ttu-id="71cf0-137">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>create</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="71cf0-137">Use the <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71cf0-138">VB</span><span class="sxs-lookup"><span data-stu-id="71cf0-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 25
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objNewShare = objWMIService.Get(&quot;Win32_Share&quot;)
errReturn = objNewShare.Create(&quot;C:\Finance&quot;, &quot;FinanceShare&quot;, FILE_SHARE, MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;)</code></pre></td>
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
<th><span data-ttu-id="71cf0-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="71cf0-139">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$FILE_SHARE = 0
$MAXIMUM_CONNECTIONS = 25

$NewDir = new-item C:\Finance -type directory 
$Shares= [WMICLASS]&quot;Win32_Share&quot;
[void]$Shares.Create(&quot;C:\Finance&quot;,&quot;FinanceShare&quot;, $FILE_SHARE, $MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;) </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71cf0-140">... copiare una cartella?</span><span class="sxs-lookup"><span data-stu-id="71cf0-140">...copy a folder?</span></span></td>
<td><p><span data-ttu-id="71cf0-141">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="71cf0-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> method.</span></span> <span data-ttu-id="71cf0-142">Per PowerShell, è possibile usare semplicemente il cmdlet Copy-Item.</span><span class="sxs-lookup"><span data-stu-id="71cf0-142">For PowerShell, you can simply use the Copy-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71cf0-143">VB</span><span class="sxs-lookup"><span data-stu-id="71cf0-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery(&quot;Select * from Win32_Directory where Name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy(&quot;D:\Archive&quot;) 
Next </code></pre></td>
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
<th><span data-ttu-id="71cf0-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="71cf0-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Copy-Item C:\Scripts -Destination D:\Archive -Recurse</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71cf0-145">... spostare una cartella?</span><span class="sxs-lookup"><span data-stu-id="71cf0-145">...move a folder?</span></span></td>
<td><p><span data-ttu-id="71cf0-146">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="71cf0-146">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> method.</span></span> <span data-ttu-id="71cf0-147">Per PowerShell, è possibile usare semplicemente il cmdlet Move-Item.</span><span class="sxs-lookup"><span data-stu-id="71cf0-147">For PowerShell, you can simply use the Move-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71cf0-148">VB</span><span class="sxs-lookup"><span data-stu-id="71cf0-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; _ 
    & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery _ 
    (&quot;Select * from Win32_Directory where name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename(&quot;C:\Admins\Documents\Archive\VBScript&quot;) 
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
<th><span data-ttu-id="71cf0-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="71cf0-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>move-item -path C:\Scripts -destination C:\Admins\Documents\Archive\PowerShell</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="71cf0-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71cf0-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71cf0-151">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="71cf0-151">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="71cf0-152">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="71cf0-152">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="71cf0-153">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="71cf0-153">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
