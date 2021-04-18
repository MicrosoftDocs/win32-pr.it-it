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
# <a name="wmi-tasks-performance-monitoring"></a>Attività WMI: monitoraggio delle prestazioni

Utilizzare le classi WMI che ottengono dati dai contatori delle prestazioni per accedere e aggiornare i dati sulle prestazioni del computer. Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Per altre informazioni, vedere [librerie di prestazioni e WMI](performance-libraries-and-wmi.md) e [monitoraggio dei dati sulle prestazioni](monitoring-performance-data.md).

Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale. Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).


Nella procedura riportata di seguito viene descritto come eseguire uno script.

**Per eseguire uno script**

1.  Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*. Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.
2.  Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.
3.  Digitare **cscript filename.vbs** al prompt dei comandi.
4.  Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati. Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).

> [!Note]  
> Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi. Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file. Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.

 

Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ricerca per categorie</th>
<th>Classi o metodi WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... ottenere i dati dei contatori delle prestazioni che è possibile visualizzare nell'utilità PerfMon in uno script?</td>
<td>Usare le classi con nomi che iniziano con &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , ad esempio <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>. Le proprietà con nomi come <strong>paging</strong> corrispondono ai contatori delle prestazioni visualizzati in Perfmon. Le &quot; &quot; classi Win32_PerfFormattedData calcolano i valori finali dei contatori.<br/></td>
</tr>
<tr class="even">
<td>... Ottieni dati sulle prestazioni in corso per un singolo processo, unità disco e altri dati?</td>
<td>Usare il <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> o la classe del <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">contatore delle prestazioni</a> formattata appropriata e il metodo <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> . Per ulteriori informazioni, vedere Creazione di <a href="scripting-with-swbemobject.md">script con SWbemObject</a>.<br/> In C++ usare <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher:: AddObjectByPath</strong></a> e <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher:: Refresh</strong></a>. Per ulteriori informazioni, vedere <a href="monitoring-performance-data.md">monitoraggio dei dati sulle prestazioni</a>.<br/> Lo script seguente viene eseguito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato. Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo. Per arrestarla a livello di codice, usare il metodo <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> nella classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .<br/> <span data-codelanguage="VisualBasic"></span>
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
<td>... Ottieni dati sulle prestazioni in corso per tutti i processi senza polling ripetuto?</td>
<td><p>Usare le classi con nomi che iniziano con &quot; Win32_PerfFormattedData &quot; e un oggetto <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> . L'aggiornamento include gli oggetti in modo da non dover ottenere ripetutamente la raccolta. Per calcolare i dati sulle prestazioni sono necessari almeno due valori, perché la maggior parte dei contatori sono contatori di frequenza. La prima volta che si visualizzano i dati di aggiornamento, è vuota.</p>
<p>Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato. Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo. Per arrestarla a livello di codice, usare il metodo <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> nella classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</p>
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
<td>... ottenere e calcolare i dati sulle prestazioni per i processi in Windows 2000?</td>
<td><p>Usare le &quot; &quot; classi di Win32_PerfRawData, ad esempio <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>. Ottenere i dati della proprietà, ad esempio <strong>PercentProcessorTime</strong>, due volte per un processo specifico. Cercare la formula specificata nel qualificatore <a href="countertype-qualifier.md"><strong>CounterType</strong></a> per la proprietà e calcolare. Il CounterType nell'esempio è <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Per ulteriori informazioni, vedere <a href="monitoring-performance-data.md">monitoraggio dei dati sulle prestazioni</a>.</p>
<p>Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato. Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo. Per arrestarla a livello di codice, usare il metodo <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> nella classe <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</p>
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



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Esempi di applicazioni WMI C++](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
