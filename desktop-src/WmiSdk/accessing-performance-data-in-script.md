---
description: Gli script WMI possono accedere alle classi del contatore delle prestazioni WMI preinstallate, sia nel computer locale che in remoto.
ms.assetid: 79e47173-c8b6-452d-9400-93e2bd6e9da5
ms.tgt_platform: multiple
title: Accesso ai dati sulle prestazioni nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e203acfc7fc23fe0dab466eee383223aad0bf889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319311"
---
# <a name="accessing-performance-data-in-script"></a><span data-ttu-id="f5242-103">Accesso ai dati sulle prestazioni nello script</span><span class="sxs-lookup"><span data-stu-id="f5242-103">Accessing Performance Data in Script</span></span>

<span data-ttu-id="f5242-104">Gli script WMI possono accedere alle [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI preinstallate, sia nel computer locale che in remoto.</span><span class="sxs-lookup"><span data-stu-id="f5242-104">WMI scripts can access the preinstalled WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes), either on the local computer or remotely.</span></span> <span data-ttu-id="f5242-105">Sebbene gli script possano ottenere dati da classi non calcolate, ad esempio la [**\_ \_ \_ memoria PerfRawData di prestazioni Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data)o le classi formattate, [**Win32 \_ PerfFormattedData \_ PerfOS \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), le classi di dati formattate possono essere più facili da usare.</span><span class="sxs-lookup"><span data-stu-id="f5242-105">While scripts can obtain data from uncalculated classes, such as [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), or formatted classes, [**Win32\_PerfFormattedData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data), the formatted data classes can be easier to use.</span></span>

<span data-ttu-id="f5242-106">Il monitoraggio dei dati sulle prestazioni con le classi del contatore delle prestazioni richiede l'utilizzo di un [*aggiornamento*](gloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="f5242-106">Monitoring performance data with the performance counter classes requires the use of a [*refresher*](gloss-r.md).</span></span> <span data-ttu-id="f5242-107">Utilizzare l'oggetto [**SWbemRefresher**](swbemrefresher.md) per archiviare uno o più oggetti prestazioni per l'aggiornamento o l'aggiornamento di un singolo oggetto da parte della chiamata [**SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="f5242-107">Use the [**SWbemRefresher**](swbemrefresher.md) object to store one or more performance objects for refresh or refresh a single object by the [**SWbemObjectEx.Refresh**](swbemobjectex-refresh-.md) call.</span></span> <span data-ttu-id="f5242-108">Per ulteriori informazioni, vedere [aggiornamento dei dati WMI negli script](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="f5242-108">For more information, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="f5242-109">Impostando la proprietà [**SWbemRefresher. AutoReconnect**](swbemrefresher-autoreconnect.md) su **true**, WMI si riconnette automaticamente a un provider remoto se la connessione è interruppe, in modo da non dover controllare lo stato della connessione.</span><span class="sxs-lookup"><span data-stu-id="f5242-109">By setting the [**SWbemRefresher.AutoReconnect**](swbemrefresher-autoreconnect.md) property to **TRUE**, WMI automatically reconnects to a remote provider if the connection is broken so that you do not need to check for connection status.</span></span>

<span data-ttu-id="f5242-110">Come illustrato nello script di esempio di codice di script seguente, è necessario effettuare una chiamata di aggiornamento iniziale per ottenere un valore iniziale per l'oggetto che si sta aggiornando.</span><span class="sxs-lookup"><span data-stu-id="f5242-110">As shown in the following script code example script, you must make an initial refresh call to get a starting value for the object you are refreshing.</span></span> <span data-ttu-id="f5242-111">Le chiamate di aggiornamento successive contengono quindi i dati.</span><span class="sxs-lookup"><span data-stu-id="f5242-111">Subsequent refresh calls then contain data.</span></span>

> [!Note]  
> <span data-ttu-id="f5242-112">Quando uno script accede ai dati dei contatori delle prestazioni WMI da un computer remoto, lo script può essere eseguito solo con l'account utente connesso corrente.</span><span class="sxs-lookup"><span data-stu-id="f5242-112">When a script is accessing WMI performance counter data from a remote computer, the script can only run under the current logged-on user account.</span></span> <span data-ttu-id="f5242-113">WMI non supporta una chiamata [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) che passa le credenziali utente diverse.</span><span class="sxs-lookup"><span data-stu-id="f5242-113">WMI does not support an [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) call that passes in different user credentials.</span></span> <span data-ttu-id="f5242-114">Pertanto, l'account che chiama il computer remoto deve disporre già dei privilegi appropriati per tale computer.</span><span class="sxs-lookup"><span data-stu-id="f5242-114">Therefore, the account calling the remote computer must already have the appropriate privileges on that computer.</span></span>

 

<span data-ttu-id="f5242-115">Nell'esempio di codice di script seguente viene illustrato come utilizzare un oggetto [**SWbemRefresher**](swbemrefresher.md) per aggiornare i dati negli oggetti contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f5242-115">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="f5242-116">Per ulteriori informazioni sull'utilizzo dei contatori delle prestazioni in WMI, vedere [accesso alle classi di prestazioni preinstallate di WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f5242-116">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:Win32_PerfRawdata_Perfproc_process.name='wscript'")
set CookedProc = GetObject("winmgmts:Win32_Perfformatteddata_Perfproc_process.name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="example"></a><span data-ttu-id="f5242-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="f5242-117">Example</span></span>

<span data-ttu-id="f5242-118">Nell'esempio di codice di script seguente viene illustrato che è necessario effettuare una chiamata di aggiornamento iniziale per ottenere un valore iniziale per l'oggetto aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f5242-118">The following script code example shows that you must make an initial refresh call to get a starting value for the refreshed object.</span></span> <span data-ttu-id="f5242-119">Le chiamate di aggiornamento successive contengono quindi i dati.</span><span class="sxs-lookup"><span data-stu-id="f5242-119">Subsequent refresh calls then contain data.</span></span>

<span data-ttu-id="f5242-120">Nell'esempio di codice di script seguente viene illustrato come utilizzare un oggetto [**SWbemRefresher**](swbemrefresher.md) per aggiornare i dati negli oggetti contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f5242-120">The following script code example shows how to use an [**SWbemRefresher**](swbemrefresher.md) object to update the data in performance counter objects.</span></span> <span data-ttu-id="f5242-121">Per ulteriori informazioni sull'utilizzo dei contatori delle prestazioni in WMI, vedere [accesso alle classi di prestazioni preinstallate di WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="f5242-121">For more information about using performance counters in WMI, see [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>


```VB
' Get raw and cooked data performance counter instances for the
" wscript process running this script

set RawProc = GetObject("winmgmts:" _
                        & "Win32_PerfRawdata_Perfproc_process." _
                        & "name='wscript'")
set CookedProc = GetObject("winmgmts:" _ 
                & "Win32_Perfformatteddata_Perfproc_process." _
                & "name='wscript'")

' Display the same property in raw and cooked form in a loop
for I = 1 to 6
    Wscript.Echo "wscript process raw PageFaultsPerSec = " _
                 & RawProc.PageFaultsPerSec _
                 & " cooked PageFaultsPerSec= " _
                 & CookedProc.PageFaultsPerSec 

' Wait 2 seconds
    Wscript.Sleep 2000
    
    ' Refresh the object
    RawProc.Refresh_
    CookedProc.Refresh_
next
```



## <a name="related-topics"></a><span data-ttu-id="f5242-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5242-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5242-123">Classi del contatore delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="f5242-123">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="f5242-124">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="f5242-124">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="f5242-125">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="f5242-125">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
