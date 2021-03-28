---
description: Questa classe è la classe padre per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Classe Process_V2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: c055dc1f78da13c0dfa29bea948a8f0c94363ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968241"
---
# <a name="process_v2-class"></a><span data-ttu-id="f6370-104">\_Classe processo V2</span><span class="sxs-lookup"><span data-stu-id="f6370-104">Process\_V2 class</span></span>

<span data-ttu-id="f6370-105">Questa classe è la classe padre per gli eventi di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f6370-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="f6370-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f6370-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6370-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6370-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="f6370-108">Members</span><span class="sxs-lookup"><span data-stu-id="f6370-108">Members</span></span>

<span data-ttu-id="f6370-109">La classe **Process** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="f6370-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6370-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6370-110">Remarks</span></span>

<span data-ttu-id="f6370-111">Per abilitare gli eventi di elaborazione in una sessione di registrazione del kernel NT, specificare il flag di **processo del \_ flag di traccia \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="f6370-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="f6370-112">È anche possibile specificare il flag seguente:</span><span class="sxs-lookup"><span data-stu-id="f6370-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="f6370-113">**\_ \_ \_ contatori processo flag di traccia eventi \_**</span><span class="sxs-lookup"><span data-stu-id="f6370-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="f6370-114">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di elaborazione chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ProcessGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="f6370-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="f6370-115">Usare i tipi di evento seguenti per identificare l'evento del processo effettivo durante l'utilizzo di eventi.</span><span class="sxs-lookup"><span data-stu-id="f6370-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="f6370-116">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="f6370-116">Event type</span></span>                                                      | <span data-ttu-id="f6370-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6370-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6370-118">**Evento \_ \_ \_ Fine tipo di traccia**(il valore del tipo di evento è 2)</span><span class="sxs-lookup"><span data-stu-id="f6370-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="f6370-119">Evento del processo finale.</span><span class="sxs-lookup"><span data-stu-id="f6370-119">End process event.</span></span> <span data-ttu-id="f6370-120">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f6370-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="f6370-121">**Evento \_ \_ \_ Inizio tipo di traccia**(il valore del tipo di evento è 1)</span><span class="sxs-lookup"><span data-stu-id="f6370-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="f6370-122">Evento di avvio processo.</span><span class="sxs-lookup"><span data-stu-id="f6370-122">Start process event.</span></span> <span data-ttu-id="f6370-123">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f6370-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="f6370-124">Valore del tipo di evento, 3</span><span class="sxs-lookup"><span data-stu-id="f6370-124">Event type value, 3</span></span>                                             | <span data-ttu-id="f6370-125">Avviare l'evento del processo di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="f6370-125">Start data collection process event.</span></span> <span data-ttu-id="f6370-126">Enumera i processi attualmente in esecuzione al momento dell'avvio della sessione kernel.</span><span class="sxs-lookup"><span data-stu-id="f6370-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="f6370-127">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f6370-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="f6370-128">Valore del tipo di evento, 4</span><span class="sxs-lookup"><span data-stu-id="f6370-128">Event type value, 4</span></span>                                             | <span data-ttu-id="f6370-129">Fine evento di elaborazione raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="f6370-129">End data collection process event.</span></span> <span data-ttu-id="f6370-130">Enumera i processi attualmente in esecuzione al termine della sessione kernel.</span><span class="sxs-lookup"><span data-stu-id="f6370-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="f6370-131">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f6370-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="f6370-132">Valore del tipo di evento, 32</span><span class="sxs-lookup"><span data-stu-id="f6370-132">Event type value, 32</span></span>                                            | <span data-ttu-id="f6370-133">Evento dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f6370-133">Performance counters event.</span></span> <span data-ttu-id="f6370-134">La classe MOF [**Process \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f6370-134">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="f6370-135">Valore del tipo di evento, 33</span><span class="sxs-lookup"><span data-stu-id="f6370-135">Event type value, 33</span></span>                                            | <span data-ttu-id="f6370-136">Riepilogo dei contatori delle prestazioni all'inizio della sessione.</span><span class="sxs-lookup"><span data-stu-id="f6370-136">Rundown of the performance counters at the start of the session.</span></span> <span data-ttu-id="f6370-137">La classe MOF [**Process \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f6370-137">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                     |
| <span data-ttu-id="f6370-138">Valore del tipo di evento, 39</span><span class="sxs-lookup"><span data-stu-id="f6370-138">Event type value, 39</span></span>                                            | <span data-ttu-id="f6370-139">Evento del processo inattivo.</span><span class="sxs-lookup"><span data-stu-id="f6370-139">Defunct process event.</span></span> <span data-ttu-id="f6370-140">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="f6370-140">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |



 

<span data-ttu-id="f6370-141">Gli eventi di avvio del processo e del thread possono essere registrati nel contesto del processo o del thread padre.</span><span class="sxs-lookup"><span data-stu-id="f6370-141">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="f6370-142">Di conseguenza, i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="f6370-142">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="f6370-143">Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).</span><span class="sxs-lookup"><span data-stu-id="f6370-143">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6370-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6370-144">Requirements</span></span>



| <span data-ttu-id="f6370-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6370-145">Requirement</span></span> | <span data-ttu-id="f6370-146">Valore</span><span class="sxs-lookup"><span data-stu-id="f6370-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f6370-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6370-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f6370-148">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f6370-148">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="f6370-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6370-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f6370-150">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f6370-150">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6370-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6370-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6370-152">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="f6370-152">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="f6370-153">**Processo**</span><span class="sxs-lookup"><span data-stu-id="f6370-153">**Process**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="f6370-154">**Elabora \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="f6370-154">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="f6370-155">**Processo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="f6370-155">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="f6370-156">**Processo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="f6370-156">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 
