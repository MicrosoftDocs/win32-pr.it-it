---
description: Tramite WMI è possibile accedere ai dati dei contatori di sistema a livello di codice dagli oggetti nelle librerie delle prestazioni.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Monitoraggio dei dati sulle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4f3ddd5024fb27d83f08225fa65faaa2e7d02cdd28189c86fc979175861453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317105"
---
# <a name="monitoring-performance-data"></a>Monitoraggio dei dati sulle prestazioni

Tramite WMI è possibile accedere ai dati dei contatori di sistema a livello di codice dagli oggetti nelle librerie delle prestazioni. Si tratta degli stessi dati sulle prestazioni visualizzati in Monitoraggio di sistema nell'utilità Perfmon. Usare le classi di contatori [delle prestazioni preinstallate](/windows/desktop/CIMWin32Prov/performance-counter-classes) per ottenere dati sulle prestazioni negli script o nelle applicazioni C++.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Classi di prestazioni WMI](#wmi-performance-classes)
-   [Provider di dati sulle prestazioni](#performance-data-providers)
-   [Uso delle classi di dati delle prestazioni formattate](#using-formatted-performance-data-classes)
-   [Uso di classi di dati sulle prestazioni non elaborati](#using-raw-performance-data-classes)
-   [Argomenti correlati](#related-topics)

## <a name="wmi-performance-classes"></a>Classi di prestazioni WMI

Ad esempio, l'oggetto "NetworkInterface", in Monitoraggio di sistema, è rappresentato in WMI dalla classe [**\_ Win32 PerfRawData \_ Tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) per i dati non elaborati e dalla classe [**\_ \_ \_ NetworkInterface Win32 PerfFormattedData Tcpip**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) per i dati precalcolati o formattati. Le classi derivate [**da \_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**da \_ Win32 PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) devono essere usate con un [*oggetto refresher.*](gloss-r.md) Nelle classi di dati non elaborati, l'applicazione o lo script C++ deve eseguire calcoli per ottenere lo stesso output Perfmon.exe. Le classi di dati formattate forniscono dati precalcolati. Per altre informazioni su come ottenere dati nelle applicazioni C++, vedere Accesso ai dati [sulle prestazioni in C++.](accessing-performance-data-in-c--.md) Per la creazione di script, [vedere Accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md) e Aggiornamento dei dati WMI negli [script.](refreshing-wmi-data-in-scripts.md)

L'esempio di codice VBScript seguente usa [**\_ Win32 PerfFormattedData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) per ottenere i dati sulle prestazioni per il processo Idle. Lo script visualizza gli stessi dati visualizzati in Perfmon per il contatore % Tempo processore dell'oggetto Processo. La chiamata a [**SWbemObjectEx.Refresh \_**](swbemobjectex-refresh-.md) esegue l'operazione di aggiornamento. Tenere presente che i dati devono essere aggiornati, in lease una sola volta, per ottenere una baseline.


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



Le classi dei contatori delle prestazioni possono inoltre fornire dati statistici. Per altre informazioni, vedere [Recupero di dati statistici sulle prestazioni.](obtaining-statistical-performance-data.md)

## <a name="performance-data-providers"></a>Provider di dati sulle prestazioni

WMI dispone di provider preinstallati che monitorano le prestazioni del sistema sia nel sistema locale che in remoto. Il provider [WmiPerfClass](wmiperfclass-provider.md) crea le classi derivate da [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**da \_ Win32 PerfFormattedData.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) Il provider [WmiPerfInst](wmiperfinst-provider.md) fornisce i dati in modo dinamico alle classi non elaborato e formattato.

## <a name="using-formatted-performance-data-classes"></a>Uso delle classi di dati delle prestazioni formattate

L'esempio di codice VBScript seguente ottiene i dati sulle prestazioni relativi a memoria, partizioni del disco e code di lavoro del server. Lo script determina quindi se i valori sono all'interno di un intervallo accettabile.

Lo script usa gli oggetti provider WMI e gli oggetti di scripting seguenti:

-   Classi di contatori delle prestazioni WMI preinstallate.
-   Oggetto refresher, [**SWbemRefresher.**](swbemrefresher.md)
-   Elementi da aggiungere al contenitore di [ **aggiornamento, SWbemRefreshableItem**](swbemrefreshableitem.md)


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



## <a name="using-raw-performance-data-classes"></a>Uso di classi di dati sulle prestazioni non elaborati

L'esempio di codice VBScript seguente ottiene la percentuale di tempo del processore non elaborato corrente nel computer locale e la converte in una percentuale. L'esempio illustra come ottenere dati sulle prestazioni non elaborati dalla proprietà **PercentProcessorTime** della classe del processore [**\_ \_ PerfRawData \_ PerfOS Win32.**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)

Per calcolare il valore percentuale del tempo processore, è necessario individuare la formula. Cercare il valore nel qualificatore **CounterType** per la proprietà **PercentProcessorTime** nella tabella [**CounterType Qualifier**](countertype-qualifier.md) per ottenere il nome della costante. Individuare il nome della costante in [Tipi di](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) contatore per ottenere la formula.


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

[Uso di WMI](using-wmi.md)
</dt> </dl>

 

 
