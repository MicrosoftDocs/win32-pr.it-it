---
description: 'Thread_V2: questa classe è la classe padre per gli eventi del thread. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Thread_V2 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: b00067af61a55e61f70b0c799a1512edf284f11c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105619"
---
# <a name="thread_v2-class"></a><span data-ttu-id="56a26-104">Classe \_ Thread V2</span><span class="sxs-lookup"><span data-stu-id="56a26-104">Thread\_V2 class</span></span>

<span data-ttu-id="56a26-105">Questa classe è la classe padre per gli eventi del thread.</span><span class="sxs-lookup"><span data-stu-id="56a26-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="56a26-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="56a26-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a26-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56a26-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="56a26-108">Members</span><span class="sxs-lookup"><span data-stu-id="56a26-108">Members</span></span>

<span data-ttu-id="56a26-109">La **classe Thread \_ V2** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="56a26-109">The **Thread\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="56a26-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="56a26-110">Remarks</span></span>

<span data-ttu-id="56a26-111">Per abilitare gli eventi del thread in una sessione di registrazione del kernel NT, specificare il flag **EVENT \_ TRACE FLAG \_ \_ THREAD** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="56a26-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="56a26-112">È anche possibile specificare i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="56a26-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="56a26-113">**CSWITCH \_ DEL FLAG DI TRACCIA \_ \_ EVENTI**</span><span class="sxs-lookup"><span data-stu-id="56a26-113">**EVENT\_TRACE\_FLAG\_CSWITCH**</span></span>
-   <span data-ttu-id="56a26-114">**\_DISPATCHER DEL FLAG DI TRACCIA \_ \_ EVENTI**</span><span class="sxs-lookup"><span data-stu-id="56a26-114">**EVENT\_TRACE\_FLAG\_DISPATCHER**</span></span>

<span data-ttu-id="56a26-115">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del thread chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ThreadGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="56a26-115">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="56a26-116">Usare i tipi di evento seguenti per identificare l'evento del thread effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="56a26-116">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="56a26-117">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="56a26-117">Event type</span></span>                                                      | <span data-ttu-id="56a26-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56a26-118">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56a26-119">**EVENTO \_ TRACE \_ TYPE \_ END**(il valore del tipo di evento è 2)</span><span class="sxs-lookup"><span data-stu-id="56a26-119">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="56a26-120">Evento del thread finale.</span><span class="sxs-lookup"><span data-stu-id="56a26-120">End thread event.</span></span> <span data-ttu-id="56a26-121">La [**classe MOF \_ Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="56a26-121">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="56a26-122">**EVENTO \_ TRACE \_ TYPE \_ START**(il valore del tipo di evento è 1)</span><span class="sxs-lookup"><span data-stu-id="56a26-122">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="56a26-123">Evento del thread di avvio.</span><span class="sxs-lookup"><span data-stu-id="56a26-123">Start thread event.</span></span> <span data-ttu-id="56a26-124">La [**classe MOF \_ Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="56a26-124">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="56a26-125">Valore del tipo di evento, 3</span><span class="sxs-lookup"><span data-stu-id="56a26-125">Event type value, 3</span></span>                                             | <span data-ttu-id="56a26-126">Evento del thread di avvio della raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="56a26-126">Start data collection thread event.</span></span> <span data-ttu-id="56a26-127">Enumera i thread attualmente in esecuzione al momento dell'avvio della sessione del kernel.</span><span class="sxs-lookup"><span data-stu-id="56a26-127">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="56a26-128">La [**classe MOF \_ Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="56a26-128">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="56a26-129">Valore del tipo di evento, 4</span><span class="sxs-lookup"><span data-stu-id="56a26-129">Event type value, 4</span></span>                                             | <span data-ttu-id="56a26-130">Evento del thread di raccolta dati finale.</span><span class="sxs-lookup"><span data-stu-id="56a26-130">End data collection thread event.</span></span> <span data-ttu-id="56a26-131">Enumera i thread attualmente in esecuzione al termine della sessione del kernel.</span><span class="sxs-lookup"><span data-stu-id="56a26-131">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="56a26-132">La [**classe MOF \_ Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="56a26-132">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="56a26-133">Valore del tipo di evento, 36</span><span class="sxs-lookup"><span data-stu-id="56a26-133">Event type value, 36</span></span>                                            | <span data-ttu-id="56a26-134">Evento di cambio di contesto.</span><span class="sxs-lookup"><span data-stu-id="56a26-134">Context switch event.</span></span> <span data-ttu-id="56a26-135">La classe MOF [**CSwitch**](cswitch.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="56a26-135">The [**CSwitch**](cswitch.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="56a26-136">Valore del tipo di evento, 50</span><span class="sxs-lookup"><span data-stu-id="56a26-136">Event type value, 50</span></span>                                            | <span data-ttu-id="56a26-137">Evento del thread pronto.</span><span class="sxs-lookup"><span data-stu-id="56a26-137">Ready thread event.</span></span> <span data-ttu-id="56a26-138">La [**classe MOF ReadyThread**](readythread.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="56a26-138">The [**ReadyThread**](readythread.md) MOF class defines the event data for this event.</span></span>                                                                                                                          |



 

<span data-ttu-id="56a26-139">Gli eventi di avvio di processi e thread possono essere registrati nel contesto del processo o del thread padre.</span><span class="sxs-lookup"><span data-stu-id="56a26-139">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="56a26-140">Di conseguenza, i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread da creare.</span><span class="sxs-lookup"><span data-stu-id="56a26-140">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="56a26-141">Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).</span><span class="sxs-lookup"><span data-stu-id="56a26-141">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="56a26-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56a26-142">Requirements</span></span>



| <span data-ttu-id="56a26-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="56a26-143">Requirement</span></span> | <span data-ttu-id="56a26-144">Valore</span><span class="sxs-lookup"><span data-stu-id="56a26-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56a26-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56a26-145">Minimum supported client</span></span><br/> | <span data-ttu-id="56a26-146">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="56a26-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="56a26-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56a26-147">Minimum supported server</span></span><br/> | <span data-ttu-id="56a26-148">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="56a26-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56a26-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56a26-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a26-150">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="56a26-150">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="56a26-151">**CSwitch**</span><span class="sxs-lookup"><span data-stu-id="56a26-151">**CSwitch**</span></span>](cswitch.md)
</dt> <dt>

[<span data-ttu-id="56a26-152">**Thread**</span><span class="sxs-lookup"><span data-stu-id="56a26-152">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="56a26-153">**Tipo \_ di threadGruppo1**</span><span class="sxs-lookup"><span data-stu-id="56a26-153">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="56a26-154">**Thread \_ V0**</span><span class="sxs-lookup"><span data-stu-id="56a26-154">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="56a26-155">**Thread \_ V1**</span><span class="sxs-lookup"><span data-stu-id="56a26-155">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 
