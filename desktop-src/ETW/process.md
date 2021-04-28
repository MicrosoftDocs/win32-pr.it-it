---
description: 'Classe di processo: questa classe è la classe padre per gli eventi del processo. La sintassi seguente è semplificata dal codice MOF.'
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
ms.openlocfilehash: 8085bae0d00ebe830efff420744f6b7e9b4bf23c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106269"
---
# <a name="process-class"></a><span data-ttu-id="c25fd-104">Classe Process</span><span class="sxs-lookup"><span data-stu-id="c25fd-104">Process class</span></span>

<span data-ttu-id="c25fd-105">Questa classe è la classe padre per gli eventi del processo.</span><span class="sxs-lookup"><span data-stu-id="c25fd-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="c25fd-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="c25fd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c25fd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c25fd-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="c25fd-108">Members</span><span class="sxs-lookup"><span data-stu-id="c25fd-108">Members</span></span>

<span data-ttu-id="c25fd-109">La **classe Process** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="c25fd-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="c25fd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c25fd-110">Remarks</span></span>

<span data-ttu-id="c25fd-111">Per abilitare gli eventi di elaborazione in una sessione di registrazione del kernel NT, specificare il flag **EVENT \_ TRACE FLAG \_ \_ PROCESS** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="c25fd-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="c25fd-112">È anche possibile specificare il flag seguente:</span><span class="sxs-lookup"><span data-stu-id="c25fd-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="c25fd-113">**CONTATORI \_ DEI PROCESSI DEI FLAG DI TRACCIA \_ \_ \_ EVENTI**</span><span class="sxs-lookup"><span data-stu-id="c25fd-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="c25fd-114">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del processo chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ProcessGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="c25fd-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="c25fd-115">Usare i tipi di evento seguenti per identificare l'evento di processo effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="c25fd-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="c25fd-116">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="c25fd-116">Event type</span></span>                                                      | <span data-ttu-id="c25fd-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c25fd-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c25fd-118">**EVENTO \_ TRACE \_ TYPE \_ END**(il valore del tipo di evento è 2)</span><span class="sxs-lookup"><span data-stu-id="c25fd-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="c25fd-119">Evento di fine processo.</span><span class="sxs-lookup"><span data-stu-id="c25fd-119">End process event.</span></span> <span data-ttu-id="c25fd-120">La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c25fd-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="c25fd-121">**EVENTO \_ TRACE \_ TYPE \_ START**(il valore del tipo di evento è 1)</span><span class="sxs-lookup"><span data-stu-id="c25fd-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="c25fd-122">Evento di avvio del processo.</span><span class="sxs-lookup"><span data-stu-id="c25fd-122">Start process event.</span></span> <span data-ttu-id="c25fd-123">La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c25fd-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="c25fd-124">Valore del tipo di evento, 3</span><span class="sxs-lookup"><span data-stu-id="c25fd-124">Event type value, 3</span></span>                                             | <span data-ttu-id="c25fd-125">Evento di avvio del processo di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="c25fd-125">Start data collection process event.</span></span> <span data-ttu-id="c25fd-126">Enumera i processi attualmente in esecuzione al momento dell'avvio della sessione del kernel.</span><span class="sxs-lookup"><span data-stu-id="c25fd-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="c25fd-127">La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c25fd-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="c25fd-128">Valore del tipo di evento, 4</span><span class="sxs-lookup"><span data-stu-id="c25fd-128">Event type value, 4</span></span>                                             | <span data-ttu-id="c25fd-129">Evento del processo di raccolta dati finale.</span><span class="sxs-lookup"><span data-stu-id="c25fd-129">End data collection process event.</span></span> <span data-ttu-id="c25fd-130">Enumera i processi attualmente in esecuzione al termine della sessione del kernel.</span><span class="sxs-lookup"><span data-stu-id="c25fd-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="c25fd-131">La [**classe \_ MOF Process TypeGroup1**](process-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="c25fd-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="c25fd-132">Gli eventi di avvio di processi e thread possono essere registrati nel contesto del processo o del thread padre.</span><span class="sxs-lookup"><span data-stu-id="c25fd-132">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="c25fd-133">Di conseguenza, i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread da creare.</span><span class="sxs-lookup"><span data-stu-id="c25fd-133">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="c25fd-134">Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).</span><span class="sxs-lookup"><span data-stu-id="c25fd-134">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="c25fd-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c25fd-135">Requirements</span></span>



| <span data-ttu-id="c25fd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c25fd-136">Requirement</span></span> | <span data-ttu-id="c25fd-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c25fd-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="c25fd-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c25fd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c25fd-139">App desktop di Windows Vista \[ \| app UWP\]</span><span class="sxs-lookup"><span data-stu-id="c25fd-139">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="c25fd-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c25fd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c25fd-141">App UWP per app desktop di Windows Server 2008 \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="c25fd-141">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c25fd-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c25fd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c25fd-143">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="c25fd-143">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="c25fd-144">**Tipo \_ di processoGruppo1**</span><span class="sxs-lookup"><span data-stu-id="c25fd-144">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="c25fd-145">**Processo \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c25fd-145">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="c25fd-146">**Processo \_ V1**</span><span class="sxs-lookup"><span data-stu-id="c25fd-146">**Process\_V1**</span></span>](process-v1.md)
</dt> <dt>

[<span data-ttu-id="c25fd-147">**Processo \_ V2**</span><span class="sxs-lookup"><span data-stu-id="c25fd-147">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 
