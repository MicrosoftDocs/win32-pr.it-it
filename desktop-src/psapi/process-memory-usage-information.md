---
title: Informazioni sull'utilizzo della memoria del processo
description: La funzione GetProcessMemoryInfo accetta un handle di processo come input e riempie una \_ struttura di contatori della memoria \_ del processo con informazioni sulle statistiche della memoria per il processo.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856606"
---
# <a name="process-memory-usage-information"></a><span data-ttu-id="983fd-103">Informazioni sull'utilizzo della memoria del processo</span><span class="sxs-lookup"><span data-stu-id="983fd-103">Process Memory Usage Information</span></span>

<span data-ttu-id="983fd-104">La funzione [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) accetta un handle di processo come input e riempie una struttura di [**\_ \_ contatori della memoria del processo**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) con informazioni sulle statistiche della memoria per il processo.</span><span class="sxs-lookup"><span data-stu-id="983fd-104">The [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function takes a process handle as input and fills a [**PROCESS\_MEMORY\_COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) structure with information about the memory statistics for the process.</span></span> <span data-ttu-id="983fd-105">Il membro **CB** riceve le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="983fd-105">The **cb** member receives the size of the structure.</span></span> <span data-ttu-id="983fd-106">Il membro **PageFaultCount** riceve il numero di errori di pagina.</span><span class="sxs-lookup"><span data-stu-id="983fd-106">The **PageFaultCount** member receives the number of page faults.</span></span> <span data-ttu-id="983fd-107">I membri rimanenti ricevono l'utilizzo di memoria corrente e massimo nelle categorie seguenti:</span><span class="sxs-lookup"><span data-stu-id="983fd-107">The remaining members receive the current and peak memory usage in the following categories:</span></span>

-   <span data-ttu-id="983fd-108">working set</span><span class="sxs-lookup"><span data-stu-id="983fd-108">working set</span></span>
-   <span data-ttu-id="983fd-109">pool di paging</span><span class="sxs-lookup"><span data-stu-id="983fd-109">paged pool</span></span>
-   <span data-ttu-id="983fd-110">pool non di paging</span><span class="sxs-lookup"><span data-stu-id="983fd-110">nonpaged pool</span></span>
-   <span data-ttu-id="983fd-111">paging</span><span class="sxs-lookup"><span data-stu-id="983fd-111">pagefile</span></span>

<span data-ttu-id="983fd-112">Il *working set* è la quantità di memoria mappata fisicamente al contesto del processo in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="983fd-112">The *working set* is the amount of memory physically mapped to the process context at a given time.</span></span> <span data-ttu-id="983fd-113">La memoria nel *pool* di paging è una memoria di sistema che può essere trasferita nel file di paging su disco (di paging) quando non è in uso.</span><span class="sxs-lookup"><span data-stu-id="983fd-113">Memory in the *paged pool* is system memory that can be transferred to the paging file on disk (paged) when it is not being used.</span></span> <span data-ttu-id="983fd-114">La memoria nel *pool* non di paging è una memoria di sistema di cui non è possibile eseguire il paging su disco fino a quando vengono allocati gli oggetti corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="983fd-114">Memory in the *nonpaged pool* is system memory that cannot be paged to disk as long as the corresponding objects are allocated.</span></span> <span data-ttu-id="983fd-115">L'utilizzo del file di *paging* rappresenta la quantità di memoria riservata per il processo nel file di paging del sistema.</span><span class="sxs-lookup"><span data-stu-id="983fd-115">The *pagefile* usage represents how much memory is set aside for the process in the system paging file.</span></span> <span data-ttu-id="983fd-116">Quando l'utilizzo della memoria è troppo elevato, le pagine del gestore della memoria virtuale hanno selezionato la memoria su disco.</span><span class="sxs-lookup"><span data-stu-id="983fd-116">When memory usage is too high, the virtual memory manager pages selected memory to disk.</span></span> <span data-ttu-id="983fd-117">Quando un thread richiede una pagina che non si trova in memoria, il gestore della memoria lo ricarica dal file di paging.</span><span class="sxs-lookup"><span data-stu-id="983fd-117">When a thread needs a page that is not in memory, the memory manager reloads it from the paging file.</span></span>

 

 




