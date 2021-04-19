---
description: Evento di traccia della gestione della memoria per un'operazione di riallocazione dell'heap.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: Evento ETW_HEAP_EVENT_REALLOC (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311740"
---
# <a name="etw_heap_event_realloc-event"></a><span data-ttu-id="f4172-103">Evento \_ \_ REALLOC evento \_ heap ETW</span><span class="sxs-lookup"><span data-stu-id="f4172-103">ETW\_HEAP\_EVENT\_REALLOC event</span></span>

<span data-ttu-id="f4172-104">L'evento **ETW \_ heap \_ Event \_ REALLOC** è un evento di traccia di gestione della memoria per un'operazione di riallocazione dell'heap.</span><span class="sxs-lookup"><span data-stu-id="f4172-104">The **ETW\_HEAP\_EVENT\_REALLOC** event is a memory management tracing event for a heap reallocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a><span data-ttu-id="f4172-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4172-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4172-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="f4172-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="f4172-107">Handle dell'heap in cui è stata allocata la memoria.</span><span class="sxs-lookup"><span data-stu-id="f4172-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="f4172-108">Si tratta dell'heap che consente di gestire un'app passata alla funzione [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando è stata allocata la memoria.</span><span class="sxs-lookup"><span data-stu-id="f4172-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="f4172-109">*NewAddress*</span><span class="sxs-lookup"><span data-stu-id="f4172-109">*NewAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="f4172-110">Nuovo indirizzo della memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="f4172-110">The new address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="f4172-111">*OldAddress*</span><span class="sxs-lookup"><span data-stu-id="f4172-111">*OldAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="f4172-112">Indirizzo precedente della memoria allocata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f4172-112">The old address of the memory that was previously allocated.</span></span>

</dd> <dt>

<span data-ttu-id="f4172-113">*NewSize*</span><span class="sxs-lookup"><span data-stu-id="f4172-113">*NewSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f4172-114">Nuova dimensione in byte allocata dall'heap.</span><span class="sxs-lookup"><span data-stu-id="f4172-114">The new size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="f4172-115">*OldSize*</span><span class="sxs-lookup"><span data-stu-id="f4172-115">*OldSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f4172-116">Dimensione precedente in byte allocata in precedenza dall'heap.</span><span class="sxs-lookup"><span data-stu-id="f4172-116">The old size in bytes previously allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="f4172-117">*Origine*</span><span class="sxs-lookup"><span data-stu-id="f4172-117">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="f4172-118">Origine della memoria utilizzata dall'allocatore per l'allocazione dell'heap.</span><span class="sxs-lookup"><span data-stu-id="f4172-118">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="f4172-119">Nella tabella seguente sono elencati i valori possibili per il parametro di *origine* , come definito nel file di intestazione *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="f4172-119">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="f4172-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f4172-120">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="f4172-121">Significato</span><span class="sxs-lookup"><span data-stu-id="f4172-121">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="f4172-122"><dt>**Memoria \_ di DA \_ LOOKASIDE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f4172-122"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="f4172-123">Memoria dall'elenco lookaside.</span><span class="sxs-lookup"><span data-stu-id="f4172-123">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="f4172-124"><dt>**Memoria \_ di DA \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f4172-124"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="f4172-125">Memoria dall'heap di frammentazione bassa.</span><span class="sxs-lookup"><span data-stu-id="f4172-125">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="f4172-126"><dt>**Memoria \_ di DA \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f4172-126"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="f4172-127">Memoria dal percorso del codice principale.</span><span class="sxs-lookup"><span data-stu-id="f4172-127">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="f4172-128"><dt> **Memoria \_ da \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f4172-128"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="f4172-129">Memoria da c lento.</span><span class="sxs-lookup"><span data-stu-id="f4172-129">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="f4172-130"><dt>**Memoria \_ di DA \_ 5 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f4172-130"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="f4172-131">Memoria non valida.</span><span class="sxs-lookup"><span data-stu-id="f4172-131">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="f4172-132"><dt>**Memoria \_ di Dall' \_ \_ heap del segmento**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f4172-132"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="f4172-133">Questo valore è riservato per un utilizzo futuro e non verrà mai restituito.</span><span class="sxs-lookup"><span data-stu-id="f4172-133">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

<span data-ttu-id="f4172-134">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="f4172-134">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4172-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4172-135">Remarks</span></span>

<span data-ttu-id="f4172-136">L'evento **ETW \_ heap \_ Event \_ REALLOC** viene registrato in tutte le riallocazioni dell'heap.</span><span class="sxs-lookup"><span data-stu-id="f4172-136">The **ETW\_HEAP\_EVENT\_REALLOC** event is logged on all heap reallocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4172-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4172-137">Requirements</span></span>



| <span data-ttu-id="f4172-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4172-138">Requirement</span></span> | <span data-ttu-id="f4172-139">Valore</span><span class="sxs-lookup"><span data-stu-id="f4172-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4172-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4172-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f4172-141">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f4172-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f4172-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4172-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f4172-143">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4172-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f4172-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4172-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4172-145"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4172-145"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4172-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4172-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4172-147">Eventi di traccia di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="f4172-147">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
