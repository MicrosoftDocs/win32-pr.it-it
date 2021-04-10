---
description: Evento di traccia di gestione della memoria per un'operazione di allocazione heap.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: Evento ETW_HEAP_EVENT_ALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343621"
---
# <a name="etw_heap_event_alloc-event"></a><span data-ttu-id="ef862-103">\_Evento di \_ allocazione evento heap ETW \_</span><span class="sxs-lookup"><span data-stu-id="ef862-103">ETW\_HEAP\_EVENT\_ALLOC event</span></span>

<span data-ttu-id="ef862-104">L'evento di allocazione **\_ \_ evento \_ heap ETW** è un evento di traccia di gestione della memoria per un'operazione di allocazione heap.</span><span class="sxs-lookup"><span data-stu-id="ef862-104">The **ETW\_HEAP\_EVENT\_ALLOC** event is a memory management tracing event for a heap allocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a><span data-ttu-id="ef862-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef862-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef862-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="ef862-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="ef862-107">Handle dell'heap in cui è stata allocata la memoria.</span><span class="sxs-lookup"><span data-stu-id="ef862-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="ef862-108">Si tratta dell'heap che consente di gestire un'app passata alla funzione [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando è stata allocata la memoria.</span><span class="sxs-lookup"><span data-stu-id="ef862-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="ef862-109">*Dimensioni*</span><span class="sxs-lookup"><span data-stu-id="ef862-109">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="ef862-110">Dimensioni in byte allocate dall'heap.</span><span class="sxs-lookup"><span data-stu-id="ef862-110">The size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="ef862-111">*Indirizzo*</span><span class="sxs-lookup"><span data-stu-id="ef862-111">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="ef862-112">Indirizzo della memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="ef862-112">The address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="ef862-113">*Origine*</span><span class="sxs-lookup"><span data-stu-id="ef862-113">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="ef862-114">Origine della memoria utilizzata dall'allocatore per l'allocazione dell'heap.</span><span class="sxs-lookup"><span data-stu-id="ef862-114">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="ef862-115">Nella tabella seguente sono elencati i valori possibili per il parametro di *origine* , come definito nel file di intestazione *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="ef862-115">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="ef862-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ef862-116">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="ef862-117">Significato</span><span class="sxs-lookup"><span data-stu-id="ef862-117">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="ef862-118"><dt>**Memoria \_ di DA \_ LOOKASIDE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ef862-118"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="ef862-119">Memoria dall'elenco lookaside.</span><span class="sxs-lookup"><span data-stu-id="ef862-119">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="ef862-120"><dt>**Memoria \_ di DA \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ef862-120"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="ef862-121">Memoria dall'heap di frammentazione bassa.</span><span class="sxs-lookup"><span data-stu-id="ef862-121">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="ef862-122"><dt>**Memoria \_ di DA \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ef862-122"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="ef862-123">Memoria dal percorso del codice principale.</span><span class="sxs-lookup"><span data-stu-id="ef862-123">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="ef862-124"><dt> **Memoria \_ da \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ef862-124"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="ef862-125">Memoria da percorso lento.</span><span class="sxs-lookup"><span data-stu-id="ef862-125">Memory from slow path.</span></span><br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="ef862-126"><dt>**Memoria \_ di DA \_ 5 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ef862-126"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="ef862-127">Memoria non valida.</span><span class="sxs-lookup"><span data-stu-id="ef862-127">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="ef862-128"><dt>**Memoria \_ di Dall' \_ \_ heap del segmento**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ef862-128"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="ef862-129">Questo valore è riservato per un utilizzo futuro e non verrà mai restituito.</span><span class="sxs-lookup"><span data-stu-id="ef862-129">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef862-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef862-130">Remarks</span></span>

<span data-ttu-id="ef862-131">L'evento di allocazione **\_ \_ evento \_ heap ETW** viene registrato per tutte le allocazioni di heap.</span><span class="sxs-lookup"><span data-stu-id="ef862-131">The **ETW\_HEAP\_EVENT\_ALLOC** event is logged on all heap allocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef862-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef862-132">Requirements</span></span>



| <span data-ttu-id="ef862-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef862-133">Requirement</span></span> | <span data-ttu-id="ef862-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ef862-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef862-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef862-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ef862-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ef862-136">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ef862-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef862-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ef862-138">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef862-138">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ef862-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef862-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef862-140"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef862-140"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef862-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef862-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef862-142">Eventi di traccia di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="ef862-142">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
