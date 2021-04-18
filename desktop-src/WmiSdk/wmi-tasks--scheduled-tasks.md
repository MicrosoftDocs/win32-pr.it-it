---
description: Le attività pianificate WMI creano e ottengono informazioni sulle attività pianificate. Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'Attività WMI: attività pianificate'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4051df4348ee47710b5d2d1f5dcc3f59f607d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310323"
---
# <a name="wmi-tasks-scheduled-tasks"></a><span data-ttu-id="18290-104">Attività WMI: attività pianificate</span><span class="sxs-lookup"><span data-stu-id="18290-104">WMI Tasks: Scheduled Tasks</span></span>

<span data-ttu-id="18290-105">Le attività pianificate WMI creano e ottengono informazioni sulle attività pianificate.</span><span class="sxs-lookup"><span data-stu-id="18290-105">WMI scheduled tasks create and get information about scheduled tasks.</span></span> <span data-ttu-id="18290-106">Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="18290-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="18290-107">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="18290-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="18290-108">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="18290-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="18290-109">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="18290-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="18290-110">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="18290-110">**To run a script**</span></span>

1.  <span data-ttu-id="18290-111">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="18290-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="18290-112">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="18290-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="18290-113">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="18290-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="18290-114">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="18290-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="18290-115">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="18290-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="18290-116">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="18290-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="18290-117">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="18290-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="18290-118">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="18290-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="18290-119">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="18290-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="18290-120">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="18290-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18290-121">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="18290-121">How do I...</span></span></th>
<th><span data-ttu-id="18290-122">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="18290-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18290-123">... creazione di attività pianificate tramite script</span><span class="sxs-lookup"><span data-stu-id="18290-123">...create scheduled tasks using scripts?</span></span></td>
<td><span data-ttu-id="18290-124">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> e il metodo <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>create</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="18290-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method.</span></span> <span data-ttu-id="18290-125">Se si verificano difficoltà nell'esecuzione di questa attività in Windows 7 o versioni successive, vedere la sezione Osservazioni <strong>Win32_ScheduledJob</strong> ; è probabile che le impostazioni impediscano l'uso della classe.</span><span class="sxs-lookup"><span data-stu-id="18290-125">If you are having difficulty making this task work on Windows 7 or later, see the <strong>Win32_ScheduledJob</strong> Remarks section; likely your settings are preventing you from using the class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18290-126">VB</span><span class="sxs-lookup"><span data-stu-id="18290-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="18290-127">Nella stringa \* \* \* \* \* &quot; \* \* \* 143000.000000-420 &quot; (usata nel valore del parametro <em>StartTime</em> del metodo <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>create</strong></a> ), \* \* \* \* &quot; \* \* \* \* 143000,000000 &quot; specifica che l'attività inizia alle 14,30 (2:30) e &quot; -420 &quot; specifica il fuso orario.</span><span class="sxs-lookup"><span data-stu-id="18290-127">In the string &quot;\*\*\*\*\*\*\*\*143000.000000-420&quot; (used in the <em>StartTime</em> parameter value of the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method), &quot;\*\*\*\*\*\*\*\*143000.000000&quot; specifies that the task starts at 14.30 (2:30 P.M.) and &quot;-420&quot; specifies the time zone.</span></span> <span data-ttu-id="18290-128">Il numero del fuso orario è la distorsione corrente della conversione dell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="18290-128">The time zone number is the current bias of the local time translation.</span></span> <span data-ttu-id="18290-129">La distorsione è la differenza tra l'ora UTC e l'ora locale.</span><span class="sxs-lookup"><span data-stu-id="18290-129">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="18290-130">Per calcolare la distorsione per il fuso orario, moltiplicare il numero di ore per cui il fuso orario è in anticipo o dietro la ora di Greenwich (GMT) di 60 (usare un numero positivo per il numero di ore se il fuso orario è preceduto da GMT e un numero negativo se il fuso orario è dietro GMT).</span><span class="sxs-lookup"><span data-stu-id="18290-130">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="18290-131">Aggiungere un ulteriore 60 al calcolo se il fuso orario USA l'ora legale.</span><span class="sxs-lookup"><span data-stu-id="18290-131">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="18290-132">Ad esempio, il fuso orario solare Pacifico è di otto ore dietro le GMT, quindi la distorsione è uguale a-420 (-8 \* 60 + 60) quando l'ora legale è in uso e-480 (-8 \* 60) quando l'ora legale non è in uso.</span><span class="sxs-lookup"><span data-stu-id="18290-132">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="18290-133">È anche possibile determinare il valore della distorsione eseguendo una query sulla proprietà bias della classe <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="18290-133">You can also determine the value of the bias by querying the bias property of the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18290-134">... Restituisce un elenco di tutte le attività pianificate in un computer?</span><span class="sxs-lookup"><span data-stu-id="18290-134">...return a list of all the scheduled tasks on a computer?</span></span></td>
<td><p><span data-ttu-id="18290-135">Usare la classe <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="18290-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class.</span></span> <span data-ttu-id="18290-136">Si noti che questa classe può restituire solo i processi creati usando uno script o AT.exe.</span><span class="sxs-lookup"><span data-stu-id="18290-136">Note that this class can only return jobs that are created using either a script or AT.exe.</span></span> <span data-ttu-id="18290-137">Non può restituire informazioni sui processi creati o modificati dalla procedura guidata attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="18290-137">It cannot return information about jobs that are either created by or modified by the Scheduled Task wizard.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="18290-138">VB</span><span class="sxs-lookup"><span data-stu-id="18290-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="18290-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18290-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18290-140">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="18290-140">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="18290-141">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="18290-141">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="18290-142">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="18290-142">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

