---
description: Utilizzando WMI, è possibile accedere ai dati del contatore di sistema a livello di codice dagli oggetti nelle librerie delle prestazioni.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Monitoraggio dei dati sulle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cee18ba88a8aff920c2d14b5709a0fd913e2ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318183"
---
# <a name="monitoring-performance-data"></a>Monitoraggio dei dati sulle prestazioni

Utilizzando WMI, è possibile accedere ai dati del contatore di sistema a livello di codice dagli oggetti nelle librerie delle prestazioni. Si tratta degli stessi dati sulle prestazioni visualizzati in monitoraggio di sistema nell'utilità PerfMon. Utilizzare le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) preinstallate per ottenere i dati sulle prestazioni in script o applicazioni C++.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Classi di prestazioni WMI](#wmi-performance-classes)
-   [Provider di dati sulle prestazioni](#performance-data-providers)
-   [Utilizzo di classi di dati di prestazioni formattate](#using-formatted-performance-data-classes)
-   [Utilizzo di classi di dati di prestazioni non elaborate](#using-raw-performance-data-classes)
-   [Argomenti correlati](#related-topics)

## <a name="wmi-performance-classes"></a>Classi di prestazioni WMI

Ad esempio, l'oggetto "interfaccia", in Monitor di sistema, è rappresentato in WMI dalla classe [**Win32 \_ PerfRawData \_ TCPIP \_ interfaccia**](./retrieving-raw-and-formatted-performance-data.md) per i dati non elaborati e la classe [**Win32 \_ PerfFormattedData \_ TCPIP \_ interfaccia**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) per i dati precalcolati o formattati. Le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) devono essere usate con un oggetto di [*aggiornamento*](gloss-r.md) . Nelle classi di dati non elaborati, l'applicazione o lo script C++ deve eseguire calcoli per ottenere lo stesso output Perfmon.exe. Le classi di dati formattate forniscono dati precalcolati. Per ulteriori informazioni su come ottenere dati nelle applicazioni C++, vedere [accesso ai dati sulle prestazioni in c++](accessing-performance-data-in-c--.md). Per gli script, vedere [accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md) e [aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md).

Nell'esempio di codice VBScript seguente viene usato il [**\_ \_ \_ processo Win32 PerfFormattedData PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) per ottenere i dati sulle prestazioni per il processo inattivo. Lo script Visualizza gli stessi dati visualizzati in PerfMon per il contatore% tempo processore dell'oggetto processo. La chiamata a [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) esegue l'operazione di aggiornamento. Tenere presente che i dati devono essere aggiornati, in lease una volta, per ottenere una baseline.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")
set PerfProcess = objWMIService.Get(_
    "Win32_PerfFormattedData_PerfProc_Process.Name='Idle'")

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend
```



Le classi del contatore delle prestazioni possono inoltre fornire dati statistici. Per ulteriori informazioni, vedere [ottenere dati statistici sulle prestazioni](obtaining-statistical-performance-data.md).

## <a name="performance-data-providers"></a>Provider di dati sulle prestazioni

In WMI sono disponibili provider preinstallati che monitorano le prestazioni del sistema nel sistema locale e in modalità remota. Il provider [wmiperfclass](wmiperfclass-provider.md) crea le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Il provider [WmiPerfInst](wmiperfinst-provider.md) fornisce i dati in modo dinamico a classi non elaborate e formattate.

## <a name="using-formatted-performance-data-classes"></a>Utilizzo di classi di dati di prestazioni formattate

Nell'esempio di codice VBScript seguente vengono ottenuti i dati sulle prestazioni relativi a memoria, partizioni del disco e code di lavoro del server. Lo script determina quindi se i valori sono compresi in un intervallo accettabile.

Lo script utilizza gli oggetti del provider WMI e gli oggetti di scripting seguenti:

-   Classi del contatore delle prestazioni WMI preinstallate.
-   Oggetto di aggiornamento, [**SWbemRefresher**](swbemrefresher.md).
-   Elementi da aggiungere al contenitore di aggiornamento, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)


```VB
Set objCimv2 = GetObject("winmgmts:root\cimv2")
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add items to the SWbemRefresher
' Without the SWbemRefreshableItem.ObjectSet call,
' the script will fail
Set objMemory = objRefresher.AddEnum _
    (objCimv2, _ 
    "Win32_PerfFormattedData_PerfOS_Memory").ObjectSet
Set objDiskQueue = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfDisk_LogicalDisk").ObjectSet
Set objQueueLength = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfNet_ServerWorkQueues").ObjectSet

' Initial refresh needed to get baseline values
objRefresher.Refresh
intTotalHealth = 0
' Do three refreshes to get data
For i = 1 to 3
    WScript.Echo "Refresh " & i
    For each intAvailableBytes in objMemory
        WScript.Echo "Available megabytes of memory: " _
            & intAvailableBytes.AvailableMBytes
        If intAvailableBytes.AvailableMBytes < 4 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intDiskQueue in objDiskQueue
        WScript.Echo "Current disk queue length " & "Name: " _
            & intDiskQueue.Name & ":" _
            & intDiskQueue.CurrentDiskQueueLength
        If intDiskQueue.CurrentDiskQueueLength > 2 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intServerQueueLength in objQueueLength
        WScript.Echo "Server work queue length: " _
            & intServerQueueLength.QueueLength
        If intServerQueueLength.QueueLength > 4 Then
            intTotalHealth = intTotalHealth + 1                       
        End If
    Wscript.Echo "  "
    Next
    If intTotalHealth > 0 Then
        Wscript.Echo "Unhealthy."
    Else
        Wscript.Echo "Healthy."
    End If
    intTotalHealth = 0
    Wscript.Sleep 5000
' Refresh data for all objects in the collection
    objRefresher.Refresh
Next
```



## <a name="using-raw-performance-data-classes"></a>Utilizzo di classi di dati di prestazioni non elaborate

Nell'esempio di codice VBScript seguente viene ottenuta una percentuale di tempo del processore RAW e corrente nel computer locale e viene convertita in una percentuale. Nell'esempio viene illustrato come ottenere i dati sulle prestazioni non elaborati dalla proprietà **PercentProcessorTime** della classe [**\_ \_ \_ processore PerfRawData PerfOS Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .

Per calcolare il valore di percentuale tempo processore, è necessario individuare la formula. Cercare il valore del qualificatore **CounterType** per la proprietà **PercentProcessorTime** nella tabella del [**qualificatore CounterType**](countertype-qualifier.md) per ottenere il nome della costante. Individuare il nome della costante nei [tipi di contatore](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) per ottenere la formula.


```VB
Set objService = GetObject( _
    "Winmgmts:{impersonationlevel=impersonate}!\Root\Cimv2")

For i = 1 to 8
    Set objInstance1 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N1 = objInstance1.PercentProcessorTime
    D1 = objInstance1.TimeStamp_Sys100NS

'Sleep for two seconds = 2000 ms
    WScript.Sleep(2000)

    Set perf_instance2 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N2 = perf_instance2.PercentProcessorTime
    D2 = perf_instance2.TimeStamp_Sys100NS
' Look up the CounterType qualifier for the PercentProcessorTime 
' and obtain the formula to calculate the meaningful data. 
' CounterType - PERF_100NSEC_TIMER_INV
' Formula - (1- ((N2 - N1) / (D2 - D1))) x 100

    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    WScript.Echo "% Processor Time=" , Round(PercentProcessorTime,2)
Next
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> </dl>

 

 
