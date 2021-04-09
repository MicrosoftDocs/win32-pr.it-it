---
description: Evento di traccia della gestione della memoria per un'operazione di heap disponibile.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: Evento ETW_HEAP_EVENT_FREE (Ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879070"
---
# <a name="etw_heap_event_free-event"></a><span data-ttu-id="4059b-103">\_Evento ETW heap \_ evento \_ gratuito</span><span class="sxs-lookup"><span data-stu-id="4059b-103">ETW\_HEAP\_EVENT\_FREE event</span></span>

<span data-ttu-id="4059b-104">L'evento **ETW \_ heap \_ Event \_ Free** è un evento di traccia di gestione della memoria per un'operazione di heap disponibile.</span><span class="sxs-lookup"><span data-stu-id="4059b-104">The **ETW\_HEAP\_EVENT\_FREE** event is a memory management tracing event for a heap free operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a><span data-ttu-id="4059b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4059b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4059b-106">*HeapHandle*</span><span class="sxs-lookup"><span data-stu-id="4059b-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="4059b-107">Handle dell'heap in cui è stata allocata la memoria.</span><span class="sxs-lookup"><span data-stu-id="4059b-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="4059b-108">Si tratta dell'heap che consente di gestire un'app passata alla funzione [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) quando è stata allocata la memoria.</span><span class="sxs-lookup"><span data-stu-id="4059b-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="4059b-109">*Indirizzo*</span><span class="sxs-lookup"><span data-stu-id="4059b-109">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="4059b-110">Indirizzo della memoria che è stata liberata.</span><span class="sxs-lookup"><span data-stu-id="4059b-110">The address of the memory that was freed.</span></span>

</dd> <dt>

<span data-ttu-id="4059b-111">*Origine*</span><span class="sxs-lookup"><span data-stu-id="4059b-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="4059b-112">Origine della memoria utilizzata dall'allocatore per l'allocazione dell'heap.</span><span class="sxs-lookup"><span data-stu-id="4059b-112">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="4059b-113">Nella tabella seguente sono elencati i valori possibili per il parametro di *origine* , come definito nel file di intestazione *ntetw. h* :</span><span class="sxs-lookup"><span data-stu-id="4059b-113">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="4059b-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4059b-114">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="4059b-115">Significato</span><span class="sxs-lookup"><span data-stu-id="4059b-115">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="4059b-116"><dt>**Memoria \_ di DA \_ LOOKASIDE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4059b-116"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="4059b-117">Memoria dall'elenco lookaside.</span><span class="sxs-lookup"><span data-stu-id="4059b-117">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="4059b-118"><dt>**Memoria \_ di DA \_ LOWFRAG**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4059b-118"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="4059b-119">Memoria dall'heap di frammentazione bassa.</span><span class="sxs-lookup"><span data-stu-id="4059b-119">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="4059b-120"><dt>**Memoria \_ di DA \_ MAINPATH**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4059b-120"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="4059b-121">Memoria dal percorso del codice principale.</span><span class="sxs-lookup"><span data-stu-id="4059b-121">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="4059b-122"><dt> **Memoria \_ da \_ SLOWPATH**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4059b-122"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="4059b-123">Memoria da c lento.</span><span class="sxs-lookup"><span data-stu-id="4059b-123">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="4059b-124"><dt>**Memoria \_ di DA \_ 5 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4059b-124"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="4059b-125">Memoria non valida.</span><span class="sxs-lookup"><span data-stu-id="4059b-125">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="4059b-126"><dt>**Memoria \_ di Dall' \_ \_ heap del segmento**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4059b-126"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="4059b-127">Questo valore è riservato per un utilizzo futuro e non verrà mai restituito.</span><span class="sxs-lookup"><span data-stu-id="4059b-127">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4059b-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="4059b-128">Remarks</span></span>

<span data-ttu-id="4059b-129">L'evento **ETW \_ heap \_ Event \_ Free** viene registrato su tutte le operazioni di heap free.</span><span class="sxs-lookup"><span data-stu-id="4059b-129">The **ETW\_HEAP\_EVENT\_FREE** event is logged on all heap free operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="4059b-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4059b-130">Requirements</span></span>



| <span data-ttu-id="4059b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4059b-131">Requirement</span></span> | <span data-ttu-id="4059b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4059b-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4059b-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4059b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4059b-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4059b-134">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4059b-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4059b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4059b-136">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4059b-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4059b-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4059b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4059b-138"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4059b-138"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4059b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4059b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4059b-140">Eventi di traccia di gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="4059b-140">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
