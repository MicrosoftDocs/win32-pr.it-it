---
title: Heap
description: Un heap tiene traccia di un gruppo di allocazioni liberate come unità.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Servizi Web heap per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399967"
---
# <a name="heap"></a><span data-ttu-id="879ba-106">Heap</span><span class="sxs-lookup"><span data-stu-id="879ba-106">Heap</span></span>

<span data-ttu-id="879ba-107">Un heap tiene traccia di un gruppo di allocazioni liberate come unità.</span><span class="sxs-lookup"><span data-stu-id="879ba-107">A heap tracks a group of allocations that are freed as a unit.</span></span>

<span data-ttu-id="879ba-108">In questo modo è possibile evitare modelli complessi di allocazione e deallocazione della memoria quando si usa WWSAPI.</span><span class="sxs-lookup"><span data-stu-id="879ba-108">This allows you to avoid complex patterns of allocating and deallocating memory when you use the WWSAPI.</span></span>


<span data-ttu-id="879ba-109">È presente un heap associato a ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="879ba-109">There is a heap associated with every message.</span></span> <span data-ttu-id="879ba-110">Durante l'invio di un messaggio o la ricezione di un messaggio, l'heap del messaggio viene utilizzato per tutte le allocazioni relative al messaggio specifico.</span><span class="sxs-lookup"><span data-stu-id="879ba-110">As a message is being sent, or as a message is being received, the heap of the message is used for any allocations relating to that particular message.</span></span> <span data-ttu-id="879ba-111">Dopo l'invio o la ricezione di un messaggio, l'heap viene reimpostato, che consente di eseguire la pulizia di tutte le allocazioni correlate al messaggio specifico.</span><span class="sxs-lookup"><span data-stu-id="879ba-111">After a message is sent or received, the heap is reset (which cleans up any allocations related to the particular message).</span></span>

<span data-ttu-id="879ba-112">Gli heap possono essere utilizzati anche per archiviare i dati dei messaggi separatamente rispetto alla durata di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="879ba-112">Heaps can also be used to store message data separately from the lifetime of a message.</span></span> <span data-ttu-id="879ba-113">Gran parte della specifica dell'API Consenti dell'heap da usare durante la lettura dei dati fornisce un controllo esplicito sulla durata dei dati letti.</span><span class="sxs-lookup"><span data-stu-id="879ba-113">Many of the API's allow specification of the heap to use when reading data give explicit control over the lifetime of any data read.</span></span>

<span data-ttu-id="879ba-114">Le allocazioni da un heap sono sicuramente allineate in almeno un limite di 8 byte.</span><span class="sxs-lookup"><span data-stu-id="879ba-114">Allocations from a heap are guaranteed to be aligned on at least an 8 byte boundary.</span></span>

<span data-ttu-id="879ba-115">Le allocazioni di zero byte restituiranno un puntatore non NULL.</span><span class="sxs-lookup"><span data-stu-id="879ba-115">Zero byte allocations will return a non-NULL pointer.</span></span>

<span data-ttu-id="879ba-116">In Windows 7, se PageHeap è abilitato, per gestire la memoria viene usato un heap restituito da HeapCreate.</span><span class="sxs-lookup"><span data-stu-id="879ba-116">In Windows 7, if PageHeap is enabled, a heap returned from HeapCreate is used to manage the memory.</span></span> <span data-ttu-id="879ba-117">In questo caso, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) esegue il mapping diretto a HeapAlloc e [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) a HeapDestroy.</span><span class="sxs-lookup"><span data-stu-id="879ba-117">In this case, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) maps directly to HeapAlloc and [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) maps to HeapDestroy.</span></span>

<span data-ttu-id="879ba-118">L'enumerazione seguente viene utilizzata con l'heap:</span><span class="sxs-lookup"><span data-stu-id="879ba-118">The following enumeration is used with the heap:</span></span>

-   [<span data-ttu-id="879ba-119">**\_ID della \_ proprietà \_ heap WS**</span><span class="sxs-lookup"><span data-stu-id="879ba-119">**WS\_HEAP\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

<span data-ttu-id="879ba-120">Con l'heap vengono usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="879ba-120">The following functions are used with the heap:</span></span>

-   [<span data-ttu-id="879ba-121">**WsAlloc**</span><span class="sxs-lookup"><span data-stu-id="879ba-121">**WsAlloc**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [<span data-ttu-id="879ba-122">**WsCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="879ba-122">**WsCreateHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [<span data-ttu-id="879ba-123">**WsFreeHeap**</span><span class="sxs-lookup"><span data-stu-id="879ba-123">**WsFreeHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [<span data-ttu-id="879ba-124">**WsGetHeapProperty**</span><span class="sxs-lookup"><span data-stu-id="879ba-124">**WsGetHeapProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [<span data-ttu-id="879ba-125">**WsResetHeap**</span><span class="sxs-lookup"><span data-stu-id="879ba-125">**WsResetHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

<span data-ttu-id="879ba-126">Con l'heap viene utilizzato l'handle seguente:</span><span class="sxs-lookup"><span data-stu-id="879ba-126">The following handle is used with the heap:</span></span>

-   [<span data-ttu-id="879ba-127">\_heap WS</span><span class="sxs-lookup"><span data-stu-id="879ba-127">WS\_HEAP</span></span>](ws-heap.md)

<span data-ttu-id="879ba-128">Con l'heap vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="879ba-128">The following structures are used with the heap:</span></span>

-   [<span data-ttu-id="879ba-129">**\_Proprietà heap \_ WS**</span><span class="sxs-lookup"><span data-stu-id="879ba-129">**WS\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [<span data-ttu-id="879ba-130">**\_Proprietà heap \_ WS**</span><span class="sxs-lookup"><span data-stu-id="879ba-130">**WS\_HEAP\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




