---
description: Negli script di monitoraggio è possibile evitare chiamate successive a GetObject usando un oggetto SWbemRefresher. L'oggetto SWbemRefresher è un contenitore che può contenere diversi oggetti WMI i cui dati possono essere aggiornati in una sola chiamata.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Aggiornamento dei dati WMI negli script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232398"
---
# <a name="refreshing-wmi-data-in-scripts"></a><span data-ttu-id="a6357-104">Aggiornamento dei dati WMI negli script</span><span class="sxs-lookup"><span data-stu-id="a6357-104">Refreshing WMI Data in Scripts</span></span>

<span data-ttu-id="a6357-105">Negli script di monitoraggio è possibile evitare chiamate successive a **GetObject** usando un oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="a6357-105">In monitoring scripts, you can avoid successive calls to **GetObject** by using an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="a6357-106">L'oggetto **SWbemRefresher** è un contenitore che può contenere diversi oggetti WMI i cui dati possono essere aggiornati in una sola chiamata.</span><span class="sxs-lookup"><span data-stu-id="a6357-106">The **SWbemRefresher** object is a container that can hold several WMI objects whose data can be refreshed in one call.</span></span>

<span data-ttu-id="a6357-107">L'utilizzo di un oggetto [**SWbemRefresher**](swbemrefresher.md) è necessario per ottenere dati accurati dalle classi delle prestazioni WMI, ad esempio [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) o altre classi preinstallate derivate da [**\_ Perf Win32**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="a6357-107">Using an [**SWbemRefresher**](swbemrefresher.md) object is required to get accurate data from WMI performance classes, such as [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) or other preinstalled classes derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span>

<span data-ttu-id="a6357-108">Nella procedura riportata di seguito viene descritto come aggiornare i dati negli script.</span><span class="sxs-lookup"><span data-stu-id="a6357-108">The following procedure describes how to refresh data in scripts.</span></span>

<span data-ttu-id="a6357-109">**Per aggiornare i dati negli script**</span><span class="sxs-lookup"><span data-stu-id="a6357-109">**To refresh data in scripts**</span></span>

1.  <span data-ttu-id="a6357-110">Chiamare **CreateObject** per creare un oggetto di aggiornamento [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="a6357-110">Call **CreateObject** to create an [**SWbemRefresher**](swbemrefresher.md) refresher object.</span></span>

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  <span data-ttu-id="a6357-111">Connettersi allo spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="a6357-111">Connect to the WMI namespace.</span></span> <span data-ttu-id="a6357-112">Per usare le classi performance [**performance \_ Win32**](/windows/desktop/CIMWin32Prov/win32-perf) preinstallate, connettersi alla **radice \\ CIMV2**.</span><span class="sxs-lookup"><span data-stu-id="a6357-112">To use preinstalled [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) performances classes, connect to **root\\cimv2**.</span></span>

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  <span data-ttu-id="a6357-113">Aggiungere un singolo oggetto (Call [**SWbemRefresher. Add**](swbemrefresher-add.md)) o una raccolta (Call [**SWbemRefresher. AddEnum**](swbemrefresher-addenum.md)) all'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a6357-113">Add a single object (call [**SWbemRefresher.Add**](swbemrefresher-add.md)) or a collection (call [**SWbemRefresher.AddEnum**](swbemrefresher-addenum.md)) to the refresher.</span></span>

    <span data-ttu-id="a6357-114">Usare le classi di dati precalcolate derivate da [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), ad esempio [**Win32 \_ PerfFormattedData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) anziché [**Win32 \_ PerfRawData \_ \_**](./retrieving-raw-and-formatted-performance-data.md)perfdisk disco logico.</span><span class="sxs-lookup"><span data-stu-id="a6357-114">Use the precalculated data classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), for example, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) instead of [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="a6357-115">In caso contrario, è necessario calcolare i valori per tutte le proprietà diverse da semplici contatori.</span><span class="sxs-lookup"><span data-stu-id="a6357-115">Otherwise, you must calculate the values for all of the properties other than simple counters.</span></span>

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  <span data-ttu-id="a6357-116">Aggiornare i dati una volta per ottenere i dati sulle prestazioni iniziali.</span><span class="sxs-lookup"><span data-stu-id="a6357-116">Refresh the data one time to get the initial performance data.</span></span>

    <span data-ttu-id="a6357-117">Chiamare il metodo [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) o il metodo generico [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="a6357-117">Call either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the generic [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

    ```VB
    objRefresher.Refresh
    ```

    

5.  <span data-ttu-id="a6357-118">Se si esegue il monitoraggio delle prestazioni e si dispone di una raccolta nell'oggetto di aggiornamento, eseguire il ciclo degli oggetti della raccolta.</span><span class="sxs-lookup"><span data-stu-id="a6357-118">If you are monitoring performance and have a collection in the refresher object, loop through the collection objects.</span></span>

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  <span data-ttu-id="a6357-119">Cancellare gli elementi dall'aggiornamento chiamando [**SWbemRefresher. DeleteAll**](swbemrefresher-deleteall.md) o rimuovere elementi specifici chiamando [**SWbemRefresher. Remove**](swbemrefresher-remove.md).</span><span class="sxs-lookup"><span data-stu-id="a6357-119">Clear the items from the refresher by calling [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) or remove specific items by calling [**SwbemRefresher.Remove**](swbemrefresher-remove.md).</span></span>

<span data-ttu-id="a6357-120">Nell'esempio di codice VBScript riportato di seguito viene illustrato come aggiornare un singolo oggetto nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="a6357-120">The following VBScript code example shows how to refresh a single object on the local computer.</span></span> <span data-ttu-id="a6357-121">Lo script crea un contenitore di aggiornamento e aggiunge un'istanza di un enumeratore per le istanze di [**\_ \_ \_ processo PerfProc Win32 PerfFormattedData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="a6357-121">The script creates a refresher container and adds an instance of an enumerator for [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instances.</span></span> <span data-ttu-id="a6357-122">La chiamata di [**aggiornamento**](swbemrefresher-refresh.md) viene effettuata tre volte per illustrare le modifiche apportate alla proprietà **PercentProcessorTime** per i processi che utilizzano più di una percentuale del tempo del processore.</span><span class="sxs-lookup"><span data-stu-id="a6357-122">The [**Refresh**](swbemrefresher-refresh.md) call is made three times to demonstrate the changes in the **PercentProcessorTime** property for processes using more than one percent of the processor time.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



<span data-ttu-id="a6357-123">La proprietà [**index**](swbemrefreshableitem-index.md) dell'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) restituito rappresenta l'indice dell'oggetto nella raccolta di aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="a6357-123">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span> <span data-ttu-id="a6357-124">È possibile chiamare la proprietà [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) per determinare se un elemento in un aggiornamento è un singolo elemento o una raccolta.</span><span class="sxs-lookup"><span data-stu-id="a6357-124">You can call [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) property to determine whether or not an item in a refresher is a single item or a collection.</span></span> <span data-ttu-id="a6357-125">Per accedere a un singolo elemento, utilizzare la proprietà [**SWbemRefreshableItem. Object**](swbemrefreshableitem-object.md) .</span><span class="sxs-lookup"><span data-stu-id="a6357-125">To access a single item, use the [**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) property.</span></span> <span data-ttu-id="a6357-126">Se non si effettua la chiamata a **SWbemRefreshableItem. Object**, lo script avrà esito negativo quando si tenta di accedere all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a6357-126">If you do not make the call to **SWbemRefreshableItem.Object**, then the script fails when you try to access the object.</span></span> <span data-ttu-id="a6357-127">Per accedere a una raccolta, usare la proprietà [**SWbemRefreshableItem. ObjectSet**](swbemrefreshableitem-objectset.md) .</span><span class="sxs-lookup"><span data-stu-id="a6357-127">To access a collection, use the [**SWbemRefreshableItem.ObjectSet**](swbemrefreshableitem-objectset.md) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6357-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a6357-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6357-129">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="a6357-129">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="a6357-130">Accesso ai dati sulle prestazioni nello script</span><span class="sxs-lookup"><span data-stu-id="a6357-130">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="a6357-131">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="a6357-131">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="a6357-132">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="a6357-132">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
