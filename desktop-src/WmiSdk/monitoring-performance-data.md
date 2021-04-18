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
# <a name="monitoring-performance-data"></a><span data-ttu-id="bdc13-103">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="bdc13-103">Monitoring Performance Data</span></span>

<span data-ttu-id="bdc13-104">Utilizzando WMI, è possibile accedere ai dati del contatore di sistema a livello di codice dagli oggetti nelle librerie delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="bdc13-104">Using WMI, you can access system counter data programmatically from objects in the performance libraries.</span></span> <span data-ttu-id="bdc13-105">Si tratta degli stessi dati sulle prestazioni visualizzati in monitoraggio di sistema nell'utilità PerfMon.</span><span class="sxs-lookup"><span data-stu-id="bdc13-105">This is the same performance data that appears in the System Monitor in the Perfmon utility.</span></span> <span data-ttu-id="bdc13-106">Utilizzare le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) preinstallate per ottenere i dati sulle prestazioni in script o applicazioni C++.</span><span class="sxs-lookup"><span data-stu-id="bdc13-106">Use the preinstalled [performance counter classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) to obtain performance data in scripts or C++ applications.</span></span>

<span data-ttu-id="bdc13-107">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="bdc13-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="bdc13-108">Classi di prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="bdc13-108">WMI Performance Classes</span></span>](#wmi-performance-classes)
-   [<span data-ttu-id="bdc13-109">Provider di dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="bdc13-109">Performance Data Providers</span></span>](#performance-data-providers)
-   [<span data-ttu-id="bdc13-110">Utilizzo di classi di dati di prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="bdc13-110">Using Formatted Performance Data Classes</span></span>](#using-formatted-performance-data-classes)
-   [<span data-ttu-id="bdc13-111">Utilizzo di classi di dati di prestazioni non elaborate</span><span class="sxs-lookup"><span data-stu-id="bdc13-111">Using Raw Performance Data Classes</span></span>](#using-raw-performance-data-classes)
-   [<span data-ttu-id="bdc13-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bdc13-112">Related topics</span></span>](#related-topics)

## <a name="wmi-performance-classes"></a><span data-ttu-id="bdc13-113">Classi di prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="bdc13-113">WMI Performance Classes</span></span>

<span data-ttu-id="bdc13-114">Ad esempio, l'oggetto "interfaccia", in Monitor di sistema, è rappresentato in WMI dalla classe [**Win32 \_ PerfRawData \_ TCPIP \_ interfaccia**](./retrieving-raw-and-formatted-performance-data.md) per i dati non elaborati e la classe [**Win32 \_ PerfFormattedData \_ TCPIP \_ interfaccia**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) per i dati precalcolati o formattati.</span><span class="sxs-lookup"><span data-stu-id="bdc13-114">As an example, the "NetworkInterface" object, in System Monitor, is represented in WMI by the [**Win32\_PerfRawData\_Tcpip\_NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) class for raw data and the [**Win32\_PerfFormattedData\_Tcpip\_NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class for precalculated, or formatted data.</span></span> <span data-ttu-id="bdc13-115">Le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) devono essere usate con un oggetto di [*aggiornamento*](gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc13-115">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) must be used with a [*refresher*](gloss-r.md) object.</span></span> <span data-ttu-id="bdc13-116">Nelle classi di dati non elaborati, l'applicazione o lo script C++ deve eseguire calcoli per ottenere lo stesso output Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="bdc13-116">On raw data classes, your C++ application or script must perform calculations to obtain the same output as Perfmon.exe.</span></span> <span data-ttu-id="bdc13-117">Le classi di dati formattate forniscono dati precalcolati.</span><span class="sxs-lookup"><span data-stu-id="bdc13-117">Formatted data classes supply precalculated data.</span></span> <span data-ttu-id="bdc13-118">Per ulteriori informazioni su come ottenere dati nelle applicazioni C++, vedere [accesso ai dati sulle prestazioni in c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="bdc13-118">For more information about obtaining data in C++ applications, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="bdc13-119">Per gli script, vedere [accesso ai dati sulle prestazioni nello script](accessing-performance-data-in-script.md) e [aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="bdc13-119">For scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="bdc13-120">Nell'esempio di codice VBScript seguente viene usato il [**\_ \_ \_ processo Win32 PerfFormattedData PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) per ottenere i dati sulle prestazioni per il processo inattivo.</span><span class="sxs-lookup"><span data-stu-id="bdc13-120">The following VBScript code example uses [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) to obtain performance data for the Idle process.</span></span> <span data-ttu-id="bdc13-121">Lo script Visualizza gli stessi dati visualizzati in PerfMon per il contatore% tempo processore dell'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="bdc13-121">The script displays the same data that appears in Perfmon for the % Processor Time counter of the Process object.</span></span> <span data-ttu-id="bdc13-122">La chiamata a [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) esegue l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bdc13-122">The call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) performs the refresh operation.</span></span> <span data-ttu-id="bdc13-123">Tenere presente che i dati devono essere aggiornati, in lease una volta, per ottenere una baseline.</span><span class="sxs-lookup"><span data-stu-id="bdc13-123">Be aware that the data must be refreshed, at lease once, to obtain a baseline.</span></span>


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



<span data-ttu-id="bdc13-124">Le classi del contatore delle prestazioni possono inoltre fornire dati statistici.</span><span class="sxs-lookup"><span data-stu-id="bdc13-124">Performance counter classes can also provide statistical data.</span></span> <span data-ttu-id="bdc13-125">Per ulteriori informazioni, vedere [ottenere dati statistici sulle prestazioni](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="bdc13-125">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="performance-data-providers"></a><span data-ttu-id="bdc13-126">Provider di dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="bdc13-126">Performance Data Providers</span></span>

<span data-ttu-id="bdc13-127">In WMI sono disponibili provider preinstallati che monitorano le prestazioni del sistema nel sistema locale e in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="bdc13-127">WMI has preinstalled providers that monitor system performance on both the local system and remotely.</span></span> <span data-ttu-id="bdc13-128">Il provider [wmiperfclass](wmiperfclass-provider.md) crea le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="bdc13-128">The [WmiPerfClass](wmiperfclass-provider.md) provider creates the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="bdc13-129">Il provider [WmiPerfInst](wmiperfinst-provider.md) fornisce i dati in modo dinamico a classi non elaborate e formattate.</span><span class="sxs-lookup"><span data-stu-id="bdc13-129">The [WmiPerfInst](wmiperfinst-provider.md) provider supplies data dynamically to both raw and formatted classes.</span></span>

## <a name="using-formatted-performance-data-classes"></a><span data-ttu-id="bdc13-130">Utilizzo di classi di dati di prestazioni formattate</span><span class="sxs-lookup"><span data-stu-id="bdc13-130">Using Formatted Performance Data Classes</span></span>

<span data-ttu-id="bdc13-131">Nell'esempio di codice VBScript seguente vengono ottenuti i dati sulle prestazioni relativi a memoria, partizioni del disco e code di lavoro del server.</span><span class="sxs-lookup"><span data-stu-id="bdc13-131">The following VBScript code example obtains performance data about memory, disk partitions, and server work queues.</span></span> <span data-ttu-id="bdc13-132">Lo script determina quindi se i valori sono compresi in un intervallo accettabile.</span><span class="sxs-lookup"><span data-stu-id="bdc13-132">The script then determines if the values are within an acceptable range.</span></span>

<span data-ttu-id="bdc13-133">Lo script utilizza gli oggetti del provider WMI e gli oggetti di scripting seguenti:</span><span class="sxs-lookup"><span data-stu-id="bdc13-133">The script uses the following WMI provider objects and scripting objects:</span></span>

-   <span data-ttu-id="bdc13-134">Classi del contatore delle prestazioni WMI preinstallate.</span><span class="sxs-lookup"><span data-stu-id="bdc13-134">Preinstalled WMI performance counter classes.</span></span>
-   <span data-ttu-id="bdc13-135">Oggetto di aggiornamento, [**SWbemRefresher**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="bdc13-135">The refresher object, [**SWbemRefresher**](swbemrefresher.md).</span></span>
-   <span data-ttu-id="bdc13-136">Elementi da aggiungere al contenitore di aggiornamento, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)</span><span class="sxs-lookup"><span data-stu-id="bdc13-136">Items to add to the refresher container, [**SWbemRefreshableItem**](swbemrefreshableitem.md)</span></span>


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



## <a name="using-raw-performance-data-classes"></a><span data-ttu-id="bdc13-137">Utilizzo di classi di dati di prestazioni non elaborate</span><span class="sxs-lookup"><span data-stu-id="bdc13-137">Using Raw Performance Data Classes</span></span>

<span data-ttu-id="bdc13-138">Nell'esempio di codice VBScript seguente viene ottenuta una percentuale di tempo del processore RAW e corrente nel computer locale e viene convertita in una percentuale.</span><span class="sxs-lookup"><span data-stu-id="bdc13-138">The following VBScript code example obtains raw, current percent processor time on the local computer and converts it to a percentage.</span></span> <span data-ttu-id="bdc13-139">Nell'esempio viene illustrato come ottenere i dati sulle prestazioni non elaborati dalla proprietà **PercentProcessorTime** della classe [**\_ \_ \_ processore PerfRawData PerfOS Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="bdc13-139">The example shows you how to obtain raw performance data from the **PercentProcessorTime** property of the [**Win32\_PerfRawData\_PerfOS\_Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class.</span></span>

<span data-ttu-id="bdc13-140">Per calcolare il valore di percentuale tempo processore, è necessario individuare la formula.</span><span class="sxs-lookup"><span data-stu-id="bdc13-140">To calculate the percent processor time value, you must locate the formula.</span></span> <span data-ttu-id="bdc13-141">Cercare il valore del qualificatore **CounterType** per la proprietà **PercentProcessorTime** nella tabella del [**qualificatore CounterType**](countertype-qualifier.md) per ottenere il nome della costante.</span><span class="sxs-lookup"><span data-stu-id="bdc13-141">Look up the value in the **CounterType** qualifier for the **PercentProcessorTime** property in the [**CounterType Qualifier**](countertype-qualifier.md) table to get the constant name.</span></span> <span data-ttu-id="bdc13-142">Individuare il nome della costante nei [tipi di contatore](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) per ottenere la formula.</span><span class="sxs-lookup"><span data-stu-id="bdc13-142">Locate the constant name in [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) to obtain the formula.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="bdc13-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bdc13-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc13-144">Utilizzo di WMI</span><span class="sxs-lookup"><span data-stu-id="bdc13-144">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
