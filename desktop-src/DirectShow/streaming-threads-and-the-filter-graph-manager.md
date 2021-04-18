---
description: Thread di streaming e gestione del grafo dei filtri
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Thread di streaming e gestione del grafo dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314843"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a><span data-ttu-id="3849c-103">Thread di streaming e gestione del grafo dei filtri</span><span class="sxs-lookup"><span data-stu-id="3849c-103">Streaming Threads and the Filter Graph Manager</span></span>

<span data-ttu-id="3849c-104">Quando il gestore del grafico del filtro arresta il grafico, attende che tutti i thread di streaming vengano arrestati.</span><span class="sxs-lookup"><span data-stu-id="3849c-104">When the Filter Graph Manager stops the graph, it waits for all streaming threads to shut down.</span></span> <span data-ttu-id="3849c-105">Questa operazione presenta le implicazioni seguenti per i filtri:</span><span class="sxs-lookup"><span data-stu-id="3849c-105">This has the following implications for filters:</span></span>

-   <span data-ttu-id="3849c-106">Un filtro non deve mai chiamare i metodi sul gestore del grafo del filtro da un thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="3849c-106">A filter must never call methods on the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="3849c-107">Filter Graph Manager usa una sezione critica per sincronizzare le proprie operazioni.</span><span class="sxs-lookup"><span data-stu-id="3849c-107">The Filter Graph Manager uses a critical section to synchronize its own operations.</span></span> <span data-ttu-id="3849c-108">Se un thread di streaming tenta di conservare questa sezione critica, può causare un deadlock.</span><span class="sxs-lookup"><span data-stu-id="3849c-108">If a streaming thread tries to hold this critical section, it can cause a deadlock.</span></span> <span data-ttu-id="3849c-109">Ad esempio, si supponga che un altro thread interrompa il grafo.</span><span class="sxs-lookup"><span data-stu-id="3849c-109">For example: Suppose that another thread stops the graph.</span></span> <span data-ttu-id="3849c-110">Il thread accetta il blocco del grafico del filtro e attende che il filtro interrompa la distribuzione dei dati.</span><span class="sxs-lookup"><span data-stu-id="3849c-110">That thread takes the filter graph lock and waits for your filter to stop delivering data.</span></span> <span data-ttu-id="3849c-111">Se il filtro è in attesa del blocco, non verrà mai arrestato, causando un deadlock.</span><span class="sxs-lookup"><span data-stu-id="3849c-111">If your filter is waiting for the lock, it will never stop, causing a deadlock.</span></span>

-   <span data-ttu-id="3849c-112">Un filtro non deve mai **AddRef** o **QueryInterface** Filter Graph Manager da un thread di streaming.</span><span class="sxs-lookup"><span data-stu-id="3849c-112">A filter must never **AddRef** or **QueryInterface** the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="3849c-113">Se il filtro include un conteggio dei riferimenti nel gestore del grafo del filtro (tramite **AddRef** o **QueryInterface**), potrebbe diventare l'ultimo oggetto a contenere un conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="3849c-113">If the filter holds a reference count on the Filter Graph Manager (through **AddRef** or **QueryInterface**), it might become the last object to hold a reference count.</span></span> <span data-ttu-id="3849c-114">Quando il filtro chiama il **rilascio**, il gestore del grafico del filtro viene distrutto automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3849c-114">When the filter calls **Release**, the Filter Graph Manager destroys itself.</span></span> <span data-ttu-id="3849c-115">All'interno della routine di pulitura, il gestore del grafico del filtro tenta di arrestare il grafo, facendo in modo che il thread di streaming venga chiuso.</span><span class="sxs-lookup"><span data-stu-id="3849c-115">Inside its cleanup routine, the Filter Graph Manager attempts to stop the graph, causing it to wait for the streaming thread to exit.</span></span> <span data-ttu-id="3849c-116">Tuttavia, è in attesa all'interno del thread di streaming, quindi il thread di streaming non può uscire.</span><span class="sxs-lookup"><span data-stu-id="3849c-116">However, it is waiting inside the streaming thread, so the streaming thread cannot exit.</span></span> <span data-ttu-id="3849c-117">Il risultato è un deadlock.</span><span class="sxs-lookup"><span data-stu-id="3849c-117">The result is a deadlock.</span></span>

 

 



