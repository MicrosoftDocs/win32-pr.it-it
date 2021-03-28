---
description: Questa classe è la classe padre per gli eventi di errore di pagina. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: Classe PageFault_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977639"
---
# <a name="pagefault_v2-class"></a><span data-ttu-id="b8a71-104">\_Classe pagefault V2</span><span class="sxs-lookup"><span data-stu-id="b8a71-104">PageFault\_V2 class</span></span>

<span data-ttu-id="b8a71-105">Questa classe è la classe padre per gli eventi di errore di pagina.</span><span class="sxs-lookup"><span data-stu-id="b8a71-105">This class is the parent class for page fault events.</span></span>

<span data-ttu-id="b8a71-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b8a71-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a71-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8a71-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="b8a71-108">Members</span><span class="sxs-lookup"><span data-stu-id="b8a71-108">Members</span></span>

<span data-ttu-id="b8a71-109">La classe **pagefault \_ v2** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="b8a71-109">The **PageFault\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a71-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8a71-110">Remarks</span></span>

<span data-ttu-id="b8a71-111">Per abilitare tutti gli eventi di errore di pagina in una sessione di registrazione del kernel NT, specificare il flag di **\_ \_ \_ \_ \_ errore della pagina memoria del flag di traccia eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="b8a71-111">To enable all page fault events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="b8a71-112">È inoltre possibile specificare i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8a71-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="b8a71-113">**\_flag di traccia eventi \_ \_ \_ errori hardware memoria \_**</span><span class="sxs-lookup"><span data-stu-id="b8a71-113">**EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS**</span></span>
-   <span data-ttu-id="b8a71-114">**FLAG di traccia eventi- \_ \_ \_ \_ Alloc virtuale**</span><span class="sxs-lookup"><span data-stu-id="b8a71-114">**EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC**</span></span>

<span data-ttu-id="b8a71-115">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per tutti gli eventi di errore di pagina chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**PageFaultGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="b8a71-115">Event trace consumers can implement special processing for all page fault events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PageFaultGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="b8a71-116">Usare i tipi di evento seguenti per identificare l'evento di memoria effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="b8a71-116">Use the following event types to identify the actual memory event when consuming events.</span></span>



| <span data-ttu-id="b8a71-117">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="b8a71-117">Event type</span></span>                                                     | <span data-ttu-id="b8a71-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8a71-118">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a71-119">\_Tipo di traccia evento \_ \_ mm \_ mucca (il valore del tipo di evento è 12)</span><span class="sxs-lookup"><span data-stu-id="b8a71-119">EVENT\_TRACE\_TYPE\_MM\_COW(Event type value is 12)</span></span><br/> | <span data-ttu-id="b8a71-120">Evento copy-on-Write.</span><span class="sxs-lookup"><span data-stu-id="b8a71-120">Copy-on-write event.</span></span> <span data-ttu-id="b8a71-121">La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-121">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="b8a71-122">Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-122">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>     |
| <span data-ttu-id="b8a71-123">\_Tipo traccia \_ evento \_ mm \_ DZF (il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="b8a71-123">EVENT\_TRACE\_TYPE\_MM\_DZF(Event type value is 11)</span></span><br/> | <span data-ttu-id="b8a71-124">Evento di errore di richiesta zero.</span><span class="sxs-lookup"><span data-stu-id="b8a71-124">Demand zero fault event.</span></span> <span data-ttu-id="b8a71-125">La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-125">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="b8a71-126">Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-126">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span> |
| <span data-ttu-id="b8a71-127">\_Tipo traccia \_ evento \_ mm \_ GPF (il valore del tipo di evento è 13)</span><span class="sxs-lookup"><span data-stu-id="b8a71-127">EVENT\_TRACE\_TYPE\_MM\_GPF(Event type value is 13)</span></span><br/> | <span data-ttu-id="b8a71-128">Evento di errore di pagina Guard.</span><span class="sxs-lookup"><span data-stu-id="b8a71-128">Guard page fault event.</span></span> <span data-ttu-id="b8a71-129">La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-129">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="b8a71-130">Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-130">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="b8a71-131">\_Tipo traccia \_ evento \_ mm \_ HPF (il valore del tipo di evento è 14)</span><span class="sxs-lookup"><span data-stu-id="b8a71-131">EVENT\_TRACE\_TYPE\_MM\_HPF(Event type value is 14)</span></span><br/> | <span data-ttu-id="b8a71-132">Evento di errore di pagina hardware.</span><span class="sxs-lookup"><span data-stu-id="b8a71-132">Hard page fault event.</span></span> <span data-ttu-id="b8a71-133">La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-133">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="b8a71-134">Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-134">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>   |
| <span data-ttu-id="b8a71-135">\_Tipo di traccia eventi \_ \_ mm \_ tf (il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="b8a71-135">EVENT\_TRACE\_TYPE\_MM\_TF(Event type value is 10)</span></span><br/>  | <span data-ttu-id="b8a71-136">Evento di errore di transizione.</span><span class="sxs-lookup"><span data-stu-id="b8a71-136">Transition fault event.</span></span> <span data-ttu-id="b8a71-137">La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-137">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="b8a71-138">Prima di Windows Vista, la classe MOF [**pagefault \_ TransitionFault**](pagefault-transitionfault.md) definisce l'evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-138">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="b8a71-139">\_Tipo di traccia eventi \_ \_ mm \_ AV (il valore del tipo di evento è 15)</span><span class="sxs-lookup"><span data-stu-id="b8a71-139">EVENT\_TRACE\_TYPE\_MM\_AV(Event type value is 15)</span></span><br/>  | <span data-ttu-id="b8a71-140">Evento di violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="b8a71-140">Access violation event.</span></span> <span data-ttu-id="b8a71-141">La classe MOF [**pagefault \_ TypeGroup1**](pagefault-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-141">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                           |
| <span data-ttu-id="b8a71-142">Valore del tipo di evento, 32</span><span class="sxs-lookup"><span data-stu-id="b8a71-142">Event type value, 32</span></span>                                           | <span data-ttu-id="b8a71-143">Evento di errore di pagina hardware. La classe MOF [**pagefault \_ HardFault**](pagefault-hardfault.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-143">Hard page fault event.The [**PageFault\_HardFault**](pagefault-hardfault.md) MOF class defines the event data for this event.</span></span>                                                                                                                               |
| <span data-ttu-id="b8a71-144">Valore del tipo di evento, 105</span><span class="sxs-lookup"><span data-stu-id="b8a71-144">Event type value, 105</span></span>                                          | <span data-ttu-id="b8a71-145">Caricamento dell'immagine nell'evento del file di paging.</span><span class="sxs-lookup"><span data-stu-id="b8a71-145">Image load in page file event.</span></span> <span data-ttu-id="b8a71-146">La classe MOF [**pagefault \_ ImageLoadBacked**](pagefault-imageloadbacked.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-146">The [**PageFault\_ImageLoadBacked**](pagefault-imageloadbacked.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="b8a71-147">Valore del tipo di evento, 98</span><span class="sxs-lookup"><span data-stu-id="b8a71-147">Event type value, 98</span></span>                                           | <span data-ttu-id="b8a71-148">Evento di allocazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="b8a71-148">Virtual allocation event.</span></span> <span data-ttu-id="b8a71-149">La classe MOF [**VirtualAlloc**](pagefault-virtualalloc.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-149">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="b8a71-150">Valore del tipo di evento, 99</span><span class="sxs-lookup"><span data-stu-id="b8a71-150">Event type value, 99</span></span>                                           | <span data-ttu-id="b8a71-151">Evento virtuale gratuito.</span><span class="sxs-lookup"><span data-stu-id="b8a71-151">Virtual free event.</span></span> <span data-ttu-id="b8a71-152">La classe MOF [**VirtualAlloc**](pagefault-virtualalloc.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8a71-152">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                      |



 

<span data-ttu-id="b8a71-153">È possibile utilizzare i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="b8a71-153">You can use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the faulting process or thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a71-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8a71-154">Requirements</span></span>



| <span data-ttu-id="b8a71-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a71-155">Requirement</span></span> | <span data-ttu-id="b8a71-156">Valore</span><span class="sxs-lookup"><span data-stu-id="b8a71-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8a71-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8a71-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a71-158">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b8a71-158">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b8a71-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8a71-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a71-160">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8a71-160">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
