---
description: Utilizzare le classi WMI che ottengono dati dai contatori delle prestazioni per accedere e aggiornare i dati sulle prestazioni del computer.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'Attività WMI: monitoraggio delle prestazioni'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbb254e14280bec5a928bdc32aaa9a3e03c7a4f4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323788"
---
# <a name="wmi-tasks-performance-monitoring"></a><span data-ttu-id="60320-103">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="60320-103">WMI Tasks: Performance Monitoring</span></span>

<span data-ttu-id="60320-104">Utilizzare le classi WMI che ottengono dati dai contatori delle prestazioni per accedere e aggiornare i dati sulle prestazioni del computer.</span><span class="sxs-lookup"><span data-stu-id="60320-104">Use the WMI classes that obtain data from performance counters to access and refresh data about computer performance.</span></span> <span data-ttu-id="60320-105">Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="60320-105">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span> <span data-ttu-id="60320-106">Per altre informazioni, vedere [librerie di prestazioni e WMI](performance-libraries-and-wmi.md) e [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="60320-106">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

<span data-ttu-id="60320-107">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="60320-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="60320-108">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="60320-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="60320-109">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="60320-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="60320-110">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="60320-110">**To run a script**</span></span>

1.  <span data-ttu-id="60320-111">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="60320-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="60320-112">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="60320-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="60320-113">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="60320-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="60320-114">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="60320-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="60320-115">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="60320-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="60320-116">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="60320-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="60320-117">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="60320-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="60320-118">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="60320-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="60320-119">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="60320-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="60320-120">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="60320-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60320-121">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="60320-121">How do I...</span></span></th>
<th><span data-ttu-id="60320-122">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="60320-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60320-123">... ottenere i dati dei contatori delle prestazioni che è possibile visualizzare nell'utilità PerfMon in uno script?</span><span class="sxs-lookup"><span data-stu-id="60320-123">...obtain the performance counter data that I can see in the Perfmon utility in a script?</span></span></td>
<td><span data-ttu-id="60320-124">Usare le classi con nomi che iniziano con &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , ad esempio <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="60320-124">Use classes that have names that begin with &quot;<a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>&quot;, for example <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="60320-125">Le proprietà con nomi come <strong>paging</strong> corrispondono ai contatori delle prestazioni visualizzati in Perfmon.</span><span class="sxs-lookup"><span data-stu-id="60320-125">Properties with names like <strong>PageFileBytes</strong> correspond to performance counters you see in Perfmon.</span></span> <span data-ttu-id="60320-126">Le &quot; &quot; classi Win32_PerfFormattedData calcolano i valori finali dei contatori.</span><span class="sxs-lookup"><span data-stu-id="60320-126">The &quot;Win32_PerfFormattedData&quot; classes calculate the final values of counters for you.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60320-127">... Ottieni dati sulle prestazioni in corso per un singolo processo, unità disco e altri dati?</span><span class="sxs-lookup"><span data-stu-id="60320-127">...get on-going performance data for a single process, disk drive, and other data?</span></span></td>
<td><span data-ttu-id="60320-128">Usare il <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> o la classe del <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">contatore delle prestazioni</a> formattata appropriata e il metodo <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="60320-128">Use the <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> or the appropriate formatted <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Performance Counter Class</a> and the <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> method.</span></span> <span data-ttu-id="60320-129">Per ulteriori informazioni, vedere Creazione di <a href="scripting-with-swbemobject.md">script con SWbemObject</a>.</span><span class="sxs-lookup"><span data-stu-id="60320-129">For more information, see <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.</span></span><br/> <span data-ttu-id="60320-130">In C++ usare <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher:: AddObjectByPath</strong></a> e <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher:: Refresh</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="60320-130">In C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> and <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>.</span></span> <span data-ttu-id="60320-131">Per ulteriori informazioni, vedere <a href="monitoring-performance-data.md">monitoraggio dei dati sulle prestazioni</a>.</span><span class="sxs-lookup"><span data-stu-id="60320-131">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span><br/> <span data-ttu-id="60320-132">Lo script seguente viene eseguito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="60320-132">The following script runs until the computer is restarted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="60320-133">Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo.</span><span class="sxs-lookup"><span data-stu-id="60320-133">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="60320-134">Per arrestarla a livello di codice, usare il metodo <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> nella classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="60320-134">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60320-135">VB</span><span class="sxs-lookup"><span data-stu-id="60320-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set PerfProcess = objWMIService.Get(_
    &quot;Win32_PerfFormattedData_PerfProc_Process.Name=&#39;Idle&#39;&quot;)

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60320-136">... Ottieni dati sulle prestazioni in corso per tutti i processi senza polling ripetuto?</span><span class="sxs-lookup"><span data-stu-id="60320-136">...get on-going performance data for all processes without repeated polling?</span></span></td>
<td><p><span data-ttu-id="60320-137">Usare le classi con nomi che iniziano con &quot; Win32_PerfFormattedData &quot; e un oggetto <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="60320-137">Use classes that have names that begin with &quot;Win32_PerfFormattedData&quot; and an <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> object.</span></span> <span data-ttu-id="60320-138">L'aggiornamento include gli oggetti in modo da non dover ottenere ripetutamente la raccolta.</span><span class="sxs-lookup"><span data-stu-id="60320-138">The refresher holds the objects so you do not need to get the collection repeatedly.</span></span> <span data-ttu-id="60320-139">Per calcolare i dati sulle prestazioni sono necessari almeno due valori, perché la maggior parte dei contatori sono contatori di frequenza.</span><span class="sxs-lookup"><span data-stu-id="60320-139">A minimum of two values are needed to calculate performance data because most counters are rate counters.</span></span> <span data-ttu-id="60320-140">La prima volta che si visualizzano i dati di aggiornamento, è vuota.</span><span class="sxs-lookup"><span data-stu-id="60320-140">The first time you display the refresher data it is empty.</span></span></p>
<p><span data-ttu-id="60320-141">Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="60320-141">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="60320-142">Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo.</span><span class="sxs-lookup"><span data-stu-id="60320-142">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="60320-143">Per arrestarla a livello di codice, usare il metodo <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> nella classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="60320-143">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60320-144">VB</span><span class="sxs-lookup"><span data-stu-id="60320-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set objRefresher = CreateObject(&quot;WbemScripting.Swbemrefresher&quot;)
Set objProcessor = objRefresher.AddEnum _
    (objWMIService, _
    &quot;Win32_PerfFormattedData_PerfOS_Processor&quot;).ObjectSet

While (True)
    objRefresher.Refresh
        For each RefreshItem in objRefresher
            For each objProcess in RefreshItem.ObjectSet
                Wscript.Echo objProcess.GetObjectText_
            Next
        Next
     Wscript.Sleep 5000
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60320-145">... ottenere e calcolare i dati sulle prestazioni per i processi in Windows 2000?</span><span class="sxs-lookup"><span data-stu-id="60320-145">...get and calculate performance data for processes on Windows 2000?</span></span></td>
<td><p><span data-ttu-id="60320-146">Usare le &quot; &quot; classi di Win32_PerfRawData, ad esempio <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="60320-146">Use the &quot;Win32_PerfRawData&quot; classes, such as <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="60320-147">Ottenere i dati della proprietà, ad esempio <strong>PercentProcessorTime</strong>, due volte per un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="60320-147">Get the property data, such as <strong>PercentProcessorTime</strong>, twice for a specific process.</span></span> <span data-ttu-id="60320-148">Cercare la formula specificata nel qualificatore <a href="countertype-qualifier.md"><strong>CounterType</strong></a> per la proprietà e calcolare.</span><span class="sxs-lookup"><span data-stu-id="60320-148">Look up the formula specified in the <a href="countertype-qualifier.md"><strong>CounterType</strong></a> qualifier for the property and calculate.</span></span> <span data-ttu-id="60320-149">Il CounterType nell'esempio è <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span><span class="sxs-lookup"><span data-stu-id="60320-149">The CounterType in the example is <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span></span> <span data-ttu-id="60320-150">Per ulteriori informazioni, vedere <a href="monitoring-performance-data.md">monitoraggio dei dati sulle prestazioni</a>.</span><span class="sxs-lookup"><span data-stu-id="60320-150">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span></p>
<p><span data-ttu-id="60320-151">Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="60320-151">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="60320-152">Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo.</span><span class="sxs-lookup"><span data-stu-id="60320-152">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="60320-153">Per arrestarla a livello di codice, usare il metodo <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> nella classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="60320-153">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60320-154">VB</span><span class="sxs-lookup"><span data-stu-id="60320-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)

While (True)
    Set object1 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N1 = object1.PercentProcessorTime
    D1 = object1.TimeStamp_Sys100NS
    Wscript.Sleep(1000)
    set object2 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N2 = object2.PercentProcessorTime
    D2 = object2.TimeStamp_Sys100NS
    &#39; CounterType - PERF_100NSEC_TIMER_INV
    &#39; Formula - (1- ((N2 - N1) / (D2 - D1))) x 100
    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    Wscript.Echo &quot;% Processor Time=&quot; , PercentProcessorTime
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="60320-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60320-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60320-156">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="60320-156">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="60320-157">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="60320-157">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="60320-158">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="60320-158">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
