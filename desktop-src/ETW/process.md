---
description: Questa classe è la classe padre per gli eventi di elaborazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Classe Process
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
ms.openlocfilehash: b014262044db9e227bec5af2b351d1392c243c23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980391"
---
# <a name="process-class"></a><span data-ttu-id="c8f39-104">Classe Process</span><span class="sxs-lookup"><span data-stu-id="c8f39-104">Process class</span></span>

<span data-ttu-id="c8f39-105">Questa classe è la classe padre per gli eventi di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="c8f39-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="c8f39-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="c8f39-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f39-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8f39-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="c8f39-108">Members</span><span class="sxs-lookup"><span data-stu-id="c8f39-108">Members</span></span>

<span data-ttu-id="c8f39-109">La classe **Process** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="c8f39-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f39-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8f39-110">Remarks</span></span>

<span data-ttu-id="c8f39-111">Per abilitare gli eventi di elaborazione in una sessione di registrazione del kernel NT, specificare il flag di **processo del \_ flag di traccia \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="c8f39-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="c8f39-112">È anche possibile specificare il flag seguente:</span><span class="sxs-lookup"><span data-stu-id="c8f39-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="c8f39-113">**\_ \_ \_ contatori processo flag di traccia eventi \_**</span><span class="sxs-lookup"><span data-stu-id="c8f39-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="c8f39-114">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi di elaborazione chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ProcessGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="c8f39-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="c8f39-115">Usare i tipi di evento seguenti per identificare l'evento del processo effettivo durante l'utilizzo di eventi.</span><span class="sxs-lookup"><span data-stu-id="c8f39-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="c8f39-116">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="c8f39-116">Event type</span></span>                                                      | <span data-ttu-id="c8f39-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8f39-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f39-118">**Evento \_ \_ \_ Fine tipo di traccia**(il valore del tipo di evento è 2)</span><span class="sxs-lookup"><span data-stu-id="c8f39-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="c8f39-119">Evento del processo finale.</span><span class="sxs-lookup"><span data-stu-id="c8f39-119">End process event.</span></span> <span data-ttu-id="c8f39-120">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c8f39-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="c8f39-121">**Evento \_ \_ \_ Inizio tipo di traccia**(il valore del tipo di evento è 1)</span><span class="sxs-lookup"><span data-stu-id="c8f39-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="c8f39-122">Evento di avvio processo.</span><span class="sxs-lookup"><span data-stu-id="c8f39-122">Start process event.</span></span> <span data-ttu-id="c8f39-123">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c8f39-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="c8f39-124">Valore del tipo di evento, 3</span><span class="sxs-lookup"><span data-stu-id="c8f39-124">Event type value, 3</span></span>                                             | <span data-ttu-id="c8f39-125">Avviare l'evento del processo di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="c8f39-125">Start data collection process event.</span></span> <span data-ttu-id="c8f39-126">Enumera i processi attualmente in esecuzione al momento dell'avvio della sessione kernel.</span><span class="sxs-lookup"><span data-stu-id="c8f39-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="c8f39-127">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c8f39-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="c8f39-128">Valore del tipo di evento, 4</span><span class="sxs-lookup"><span data-stu-id="c8f39-128">Event type value, 4</span></span>                                             | <span data-ttu-id="c8f39-129">Fine evento di elaborazione raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="c8f39-129">End data collection process event.</span></span> <span data-ttu-id="c8f39-130">Enumera i processi attualmente in esecuzione al termine della sessione kernel.</span><span class="sxs-lookup"><span data-stu-id="c8f39-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="c8f39-131">La classe MOF [**Process \_ TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c8f39-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="c8f39-132">Gli eventi di avvio del processo e del thread possono essere registrati nel contesto del processo o del thread padre.</span><span class="sxs-lookup"><span data-stu-id="c8f39-132">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="c8f39-133">Di conseguenza, i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="c8f39-133">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="c8f39-134">Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).</span><span class="sxs-lookup"><span data-stu-id="c8f39-134">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f39-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8f39-135">Requirements</span></span>



| <span data-ttu-id="c8f39-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8f39-136">Requirement</span></span> | <span data-ttu-id="c8f39-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c8f39-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="c8f39-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8f39-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f39-139">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c8f39-139">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="c8f39-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8f39-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f39-141">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c8f39-141">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8f39-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8f39-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f39-143">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="c8f39-143">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="c8f39-144">**Elabora \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="c8f39-144">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="c8f39-145">**Processo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c8f39-145">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="c8f39-146">**Processo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="c8f39-146">**Process\_V1**</span></span>](process-v1.md)
</dt> <dt>

[<span data-ttu-id="c8f39-147">**Processo \_ v2**</span><span class="sxs-lookup"><span data-stu-id="c8f39-147">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 
