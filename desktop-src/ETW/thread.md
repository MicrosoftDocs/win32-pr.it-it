---
description: 'Classe di thread: questa classe è la classe padre per gli eventi di thread. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105529"
---
# <a name="thread-class"></a><span data-ttu-id="1bb67-104">Thread (classe)</span><span class="sxs-lookup"><span data-stu-id="1bb67-104">Thread class</span></span>

<span data-ttu-id="1bb67-105">Questa classe è la classe padre per gli eventi del thread.</span><span class="sxs-lookup"><span data-stu-id="1bb67-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="1bb67-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="1bb67-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bb67-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1bb67-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1bb67-108">Members</span><span class="sxs-lookup"><span data-stu-id="1bb67-108">Members</span></span>

<span data-ttu-id="1bb67-109">La **classe Thread** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="1bb67-109">The **Thread** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bb67-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bb67-110">Remarks</span></span>

<span data-ttu-id="1bb67-111">Per abilitare gli eventi del thread in una sessione di registrazione del kernel NT, specificare il flag **EVENT \_ TRACE FLAG \_ \_ THREAD** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="1bb67-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="1bb67-112">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi del thread chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ThreadGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="1bb67-112">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="1bb67-113">Usare i tipi di evento seguenti per identificare l'evento del thread effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="1bb67-113">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="1bb67-114">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="1bb67-114">Event type</span></span>                                                      | <span data-ttu-id="1bb67-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bb67-115">Description</span></span>                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb67-116">**EVENTO \_ TRACE \_ TYPE \_ END**(il valore del tipo di evento è 2)</span><span class="sxs-lookup"><span data-stu-id="1bb67-116">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="1bb67-117">Evento del thread finale.</span><span class="sxs-lookup"><span data-stu-id="1bb67-117">End thread event.</span></span> <span data-ttu-id="1bb67-118">La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="1bb67-118">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="1bb67-119">**EVENTO \_ TRACE \_ TYPE \_ START**(il valore del tipo di evento è 1)</span><span class="sxs-lookup"><span data-stu-id="1bb67-119">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="1bb67-120">Evento del thread di avvio.</span><span class="sxs-lookup"><span data-stu-id="1bb67-120">Start thread event.</span></span> <span data-ttu-id="1bb67-121">La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="1bb67-121">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="1bb67-122">Valore del tipo di evento, 3</span><span class="sxs-lookup"><span data-stu-id="1bb67-122">Event type value, 3</span></span>                                             | <span data-ttu-id="1bb67-123">Avviare l'evento del thread di raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="1bb67-123">Start data collection thread event.</span></span> <span data-ttu-id="1bb67-124">Enumera i thread attualmente in esecuzione al momento dell'avvio della sessione del kernel.</span><span class="sxs-lookup"><span data-stu-id="1bb67-124">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="1bb67-125">La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="1bb67-125">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="1bb67-126">Valore del tipo di evento, 4</span><span class="sxs-lookup"><span data-stu-id="1bb67-126">Event type value, 4</span></span>                                             | <span data-ttu-id="1bb67-127">Evento del thread di raccolta dati finale.</span><span class="sxs-lookup"><span data-stu-id="1bb67-127">End data collection thread event.</span></span> <span data-ttu-id="1bb67-128">Enumera i thread attualmente in esecuzione al termine della sessione del kernel.</span><span class="sxs-lookup"><span data-stu-id="1bb67-128">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="1bb67-129">La [**classe \_ MOF Thread TypeGroup1**](thread-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="1bb67-129">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="1bb67-130">Gli eventi di avvio di processi e thread possono essere registrati nel contesto del processo o del thread padre.</span><span class="sxs-lookup"><span data-stu-id="1bb67-130">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="1bb67-131">Di conseguenza, i **membri ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) potrebbero non corrispondere al processo e al thread da creare.</span><span class="sxs-lookup"><span data-stu-id="1bb67-131">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="1bb67-132">Questo è il motivo per cui questi eventi contengono gli identificatori di processo e thread nei dati dell'evento (oltre a quelli nell'intestazione dell'evento).</span><span class="sxs-lookup"><span data-stu-id="1bb67-132">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bb67-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bb67-133">Requirements</span></span>



| <span data-ttu-id="1bb67-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bb67-134">Requirement</span></span> | <span data-ttu-id="1bb67-135">Valore</span><span class="sxs-lookup"><span data-stu-id="1bb67-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1bb67-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bb67-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1bb67-137">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1bb67-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1bb67-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bb67-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1bb67-139">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1bb67-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1bb67-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bb67-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bb67-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="1bb67-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="1bb67-142">**Thread \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="1bb67-142">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="1bb67-143">**Thread \_ V0**</span><span class="sxs-lookup"><span data-stu-id="1bb67-143">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="1bb67-144">**Thread \_ V1**</span><span class="sxs-lookup"><span data-stu-id="1bb67-144">**Thread\_V1**</span></span>](thread-v1.md)
</dt> <dt>

[<span data-ttu-id="1bb67-145">**Thread \_ V2**</span><span class="sxs-lookup"><span data-stu-id="1bb67-145">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 
