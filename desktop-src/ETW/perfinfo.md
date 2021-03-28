---
description: Questa classe è la classe padre per gli eventi del contatore delle prestazioni. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Classe PerfInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977706"
---
# <a name="perfinfo-class"></a><span data-ttu-id="c01f6-104">Classe PerfInfo</span><span class="sxs-lookup"><span data-stu-id="c01f6-104">PerfInfo class</span></span>

<span data-ttu-id="c01f6-105">Questa classe è la classe padre per gli eventi del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="c01f6-105">This class is the parent class for performance counter events.</span></span>

<span data-ttu-id="c01f6-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="c01f6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01f6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c01f6-107">Syntax</span></span>

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="c01f6-108">Members</span><span class="sxs-lookup"><span data-stu-id="c01f6-108">Members</span></span>

<span data-ttu-id="c01f6-109">La classe **PerfInfo** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="c01f6-109">The **PerfInfo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c01f6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c01f6-110">Remarks</span></span>

<span data-ttu-id="c01f6-111">Per abilitare gli eventi di chiamata di procedura posticipata in una sessione di registrazione del kernel NT, specificare il flag **DPC del \_ flag di traccia \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="c01f6-111">To enable deferred procedure call (DPC) events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="c01f6-112">È anche possibile specificare uno o più dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="c01f6-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="c01f6-113">**\_interrupt del \_ flag di traccia eventi \_**</span><span class="sxs-lookup"><span data-stu-id="c01f6-113">**EVENT\_TRACE\_FLAG\_INTERRUPT**</span></span>
-   <span data-ttu-id="c01f6-114">**\_ \_ profilo contrassegno di traccia eventi \_**</span><span class="sxs-lookup"><span data-stu-id="c01f6-114">**EVENT\_TRACE\_FLAG\_PROFILE**</span></span>
-   <span data-ttu-id="c01f6-115">**\_flag di traccia evento \_ \_ SYSTEMCALL**</span><span class="sxs-lookup"><span data-stu-id="c01f6-115">**EVENT\_TRACE\_FLAG\_SYSTEMCALL**</span></span>

<span data-ttu-id="c01f6-116">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi DPC chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**PerfInfoGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="c01f6-116">Event trace consumers can implement special processing for DPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PerfInfoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="c01f6-117">Usare i tipi di evento seguenti per identificare l'evento effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="c01f6-117">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="c01f6-118">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="c01f6-118">Event type</span></span>           | <span data-ttu-id="c01f6-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c01f6-119">Description</span></span>                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c01f6-120">Valore del tipo di evento, 46</span><span class="sxs-lookup"><span data-stu-id="c01f6-120">Event type value, 46</span></span> | <span data-ttu-id="c01f6-121">Evento del profilo campionato.</span><span class="sxs-lookup"><span data-stu-id="c01f6-121">Sampled profile event.</span></span> <span data-ttu-id="c01f6-122">La classe MOF [**SampledProfile**](sampledprofile.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c01f6-122">The [**SampledProfile**](sampledprofile.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="c01f6-123">Valore del tipo di evento, 51</span><span class="sxs-lookup"><span data-stu-id="c01f6-123">Event type value, 51</span></span> | <span data-ttu-id="c01f6-124">Evento di chiamata di sistema Enter.</span><span class="sxs-lookup"><span data-stu-id="c01f6-124">System call enter event.</span></span> <span data-ttu-id="c01f6-125">La classe MOF [**SysCallEnter**](syscallenter.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c01f6-125">The [**SysCallEnter**](syscallenter.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="c01f6-126">Valore del tipo di evento, 52</span><span class="sxs-lookup"><span data-stu-id="c01f6-126">Event type value, 52</span></span> | <span data-ttu-id="c01f6-127">Evento di uscita chiamata di sistema.</span><span class="sxs-lookup"><span data-stu-id="c01f6-127">System call exit event.</span></span> <span data-ttu-id="c01f6-128">La classe MOF [**SysCallExit**](syscallexit.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c01f6-128">The [**SysCallExit**](syscallexit.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="c01f6-129">Valore del tipo di evento, 66</span><span class="sxs-lookup"><span data-stu-id="c01f6-129">Event type value, 66</span></span> | <span data-ttu-id="c01f6-130">Evento DPC a thread.</span><span class="sxs-lookup"><span data-stu-id="c01f6-130">Threaded DPC event.</span></span> <span data-ttu-id="c01f6-131">La classe [**DPC**](dpc.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c01f6-131">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                          |
| <span data-ttu-id="c01f6-132">Valore del tipo di evento, 67</span><span class="sxs-lookup"><span data-stu-id="c01f6-132">Event type value, 67</span></span> | <span data-ttu-id="c01f6-133">Evento di interrupt service routine (ISR).</span><span class="sxs-lookup"><span data-stu-id="c01f6-133">Interrupt service routine (ISR) event.</span></span> <span data-ttu-id="c01f6-134">La classe MOF [**ISR**](isr.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c01f6-134">The [**ISR**](isr.md) MOF class defines the event data for this event.</span></span>       |
| <span data-ttu-id="c01f6-135">Valore del tipo di evento, 68</span><span class="sxs-lookup"><span data-stu-id="c01f6-135">Event type value, 68</span></span> | <span data-ttu-id="c01f6-136">Evento DPC.</span><span class="sxs-lookup"><span data-stu-id="c01f6-136">DPC event.</span></span> <span data-ttu-id="c01f6-137">La classe [**DPC**](dpc.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c01f6-137">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="c01f6-138">Valore del tipo di evento, 69</span><span class="sxs-lookup"><span data-stu-id="c01f6-138">Event type value, 69</span></span> | <span data-ttu-id="c01f6-139">Evento timer DPC.</span><span class="sxs-lookup"><span data-stu-id="c01f6-139">DPC timer event.</span></span> <span data-ttu-id="c01f6-140">La classe [**DPC**](dpc.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c01f6-140">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="c01f6-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c01f6-141">Requirements</span></span>



| <span data-ttu-id="c01f6-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="c01f6-142">Requirement</span></span> | <span data-ttu-id="c01f6-143">Valore</span><span class="sxs-lookup"><span data-stu-id="c01f6-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c01f6-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c01f6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="c01f6-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c01f6-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c01f6-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c01f6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="c01f6-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c01f6-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
