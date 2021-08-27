---
description: Usare le classi WMI che ottengono dati dai contatori delle prestazioni per accedere e aggiornare i dati sulle prestazioni del computer.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'Attività WMI: Monitoraggio delle prestazioni'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ff50e0a4656caf33289b534307043694dbe2cdce
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623917"
---
# <a name="wmi-tasks-performance-monitoring"></a>Attività WMI: Monitoraggio delle prestazioni

Usare le classi WMI che ottengono dati dai contatori delle prestazioni per accedere e aggiornare i dati sulle prestazioni del computer. Per altri esempi, vedere TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Per altre informazioni, vedere [Librerie delle prestazioni e WMI](performance-libraries-and-wmi.md) e Monitoraggio dei dati sulle [prestazioni](monitoring-performance-data.md).

Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale. Per altre informazioni su come usare lo script per ottenere dati da computer remoti, vedere [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).


La procedura seguente descrive come eseguire uno script.

**Per eseguire uno script**

1.  Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*. Assicurarsi che l'editor di testo non aggiunge un'.txt al file.
2.  Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.
3.  Digitare **cscript filename.vbs** al prompt dei comandi.
4.  Se non è possibile accedere a un registro eventi, verificare se è in esecuzione da un prompt dei comandi con privilegi elevati. Alcuni registri eventi, ad esempio il registro eventi di sicurezza, possono essere protetti dai controlli di accesso utente.

> [!Note]  
> Per impostazione predefinita, cscript visualizza l'output di uno script nella finestra del prompt dei comandi. Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file. Digitare **cscript filename.vbs > outfile.txt** prompt dei comandi per reindirizzare l'output dello *script* filename.vbsa *outfile.txt*.

 

Nella tabella seguente sono elencati esempi di script che possono essere usati per ottenere vari tipi di dati dal computer locale.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Ricerca per categorie</th>
<th>Classi o metodi WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... ottenere i dati del contatore delle prestazioni che è possibile visualizzare nell'utilità Perfmon in uno script?</td>
<td>Usare classi con nomi che iniziano &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">con Win32_PerfFormattedData</a> &quot; , ad esempio <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>. Le proprietà con nomi <strong>come PageFileBytes</strong> corrispondono ai contatori delle prestazioni visualizzati in Perfmon. Le &quot; Win32_PerfFormattedData &quot; calcolano automaticamente i valori finali dei contatori.<br/></td>
</tr>
<tr class="even">
<td>... ottenere dati sulle prestazioni in corso per un singolo processo, unità disco e altri dati?</td>
<td>Usare il <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> o la classe del contatore delle prestazioni formattata <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">appropriata</a> e il <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> metodo . Per altre informazioni, vedere <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.<br/> In C++ usare <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> e <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>. Per altre informazioni, vedere <a href="monitoring-performance-data.md">Monitoraggio dei dati sulle prestazioni</a>.<br/> Lo script seguente viene eseguito fino al riavvio del computer, all'arresto di WMI o all'arresto dello script. Per arrestare manualmente lo script, usare Gestione attività per arrestare il processo. Per arrestarlo a livello di codice, usare il <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>metodo Terminate</strong></a> nella <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> classe .<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
<td>... ottenere dati sulle prestazioni in corso per tutti i processi senza polling ripetuto?</td>
<td><p>Usare classi con nomi che iniziano &quot; con Win32_PerfFormattedData e un oggetto &quot; <a href="swbemrefresher.md"><strong>SWbemRefresher.</strong></a> L'aggiornamento contiene gli oggetti in modo che non sia necessario ottenere la raccolta ripetutamente. Per calcolare i dati sulle prestazioni sono necessari almeno due valori, perché la maggior parte dei contatori sono contatori delle frequenze. La prima volta che si visualizzano i dati dell'aggiornamento, i dati sono vuoti.</p>
<p>Lo script seguente viene eseguito a tempo indeterminato fino al riavvio del computer, all'arresto di WMI o all'arresto dello script. Per arrestare manualmente lo script, usare Gestione attività per arrestare il processo. Per arrestarlo a livello di codice, usare il <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>metodo Terminate</strong></a> nella <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> classe .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
<td>... ottenere e calcolare i dati sulle prestazioni per i processi Windows 2000?</td>
<td><p>Usare le &quot; classi &quot; Win32_PerfRawData, ad esempio <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>. Ottenere i dati delle proprietà, ad esempio <strong>PercentProcessorTime</strong>, due volte per un processo specifico. Cercare la formula specificata nel qualificatore <a href="countertype-qualifier.md"><strong>CounterType</strong></a> per la proprietà e calcolare. CounterType nell'esempio è <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Per altre informazioni, vedere <a href="monitoring-performance-data.md">Monitoraggio dei dati sulle prestazioni</a>.</p>
<p>Lo script seguente viene eseguito a tempo indeterminato fino al riavvio del computer, all'arresto di WMI o all'arresto dello script. Per arrestare manualmente lo script, usare Gestione attività per arrestare il processo. Per arrestarlo a livello di codice, usare il <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>metodo Terminate</strong></a> nella <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> classe .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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

[Esempi di applicazioni C++ WMI](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
