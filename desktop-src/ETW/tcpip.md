---
description: Questa classe è la classe padre per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: Classe TcpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6488ece2fd8df0670455ceea25560835c352b83e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978226"
---
# <a name="tcpip-class"></a><span data-ttu-id="2d216-104">Classe TcpIp</span><span class="sxs-lookup"><span data-stu-id="2d216-104">TcpIp class</span></span>

<span data-ttu-id="2d216-105">Questa classe è la classe padre per gli eventi TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2d216-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="2d216-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="2d216-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d216-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d216-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="2d216-108">Members</span><span class="sxs-lookup"><span data-stu-id="2d216-108">Members</span></span>

<span data-ttu-id="2d216-109">La classe **Tcpip** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="2d216-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d216-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d216-110">Remarks</span></span>

<span data-ttu-id="2d216-111">Per abilitare gli eventi TCP/IP in una sessione di registrazione del kernel NT, specificare il flag **tcpip di rete del flag di \_ traccia \_ \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="2d216-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="2d216-112">I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi TCP/IP chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**TcpIpGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="2d216-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="2d216-113">Usare i tipi di eventi seguenti per identificare l'evento di rete (TCP/IP) effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="2d216-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="2d216-114">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="2d216-114">Event type</span></span>                                                            | <span data-ttu-id="2d216-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d216-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d216-116">**Evento \_ Tipo di traccia \_ \_ Accept**(il valore del tipo di evento è 15)</span><span class="sxs-lookup"><span data-stu-id="2d216-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="2d216-117">Evento Accept per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="2d216-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="2d216-118">La classe [**TCPIP \_ TypeGroup2**](tcpip-typegroup2.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="2d216-119">**Evento \_ Tipo di traccia \_ \_ Connect**(il valore del tipo di evento è 12)</span><span class="sxs-lookup"><span data-stu-id="2d216-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="2d216-120">Evento Connect per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="2d216-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="2d216-121">La classe [**TCPIP \_ TypeGroup2**](tcpip-typegroup2.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="2d216-122">**Evento \_ \_Disconnessione \_ tipo di traccia**(il valore del tipo di evento è 13)</span><span class="sxs-lookup"><span data-stu-id="2d216-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="2d216-123">Evento di disconnessione per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="2d216-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="2d216-124">La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="2d216-125">**Evento \_ Tipo di traccia \_ \_ Receive**(il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="2d216-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="2d216-126">Evento di ricezione per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="2d216-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="2d216-127">La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="2d216-128">**Evento \_ Tipo di traccia \_ \_ riconnessione**(il valore del tipo di evento è 16)</span><span class="sxs-lookup"><span data-stu-id="2d216-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="2d216-129">Riconnetti l'evento per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="2d216-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="2d216-130">Un tentativo di connessione non è riuscito e viene effettuato un altro tentativo. La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="2d216-131">**Evento \_ \_RItrasmissione \_ del tipo di traccia**(il valore del tipo di evento è 14)</span><span class="sxs-lookup"><span data-stu-id="2d216-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="2d216-132">Ritrasmissione dell'evento per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="2d216-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="2d216-133">La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="2d216-134">**Evento \_ Tipo di traccia \_ \_ Send**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="2d216-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="2d216-135">Inviare un evento per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="2d216-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="2d216-136">La classe [**TCPIP \_ SendIPV4**](tcpip-sendipv4.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="2d216-137">Valore del tipo di evento, 17</span><span class="sxs-lookup"><span data-stu-id="2d216-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="2d216-138">Evento fail.</span><span class="sxs-lookup"><span data-stu-id="2d216-138">Fail event.</span></span> <span data-ttu-id="2d216-139">La classe MOF [**\_ Fail di Tcpip**](tcpip-fail.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="2d216-140">Valore del tipo di evento, 18</span><span class="sxs-lookup"><span data-stu-id="2d216-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="2d216-141">Evento di copia TCP per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="2d216-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="2d216-142">La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="2d216-143">Valore del tipo di evento, 26</span><span class="sxs-lookup"><span data-stu-id="2d216-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="2d216-144">Inviare un evento per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d216-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="2d216-145">La classe [**TCPIP \_ SendIPV6**](tcpip-sendipv6.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="2d216-146">Valore del tipo di evento, 27</span><span class="sxs-lookup"><span data-stu-id="2d216-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="2d216-147">Evento di ricezione per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d216-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="2d216-148">La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="2d216-149">Valore del tipo di evento, 28</span><span class="sxs-lookup"><span data-stu-id="2d216-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="2d216-150">Evento Connect per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d216-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="2d216-151">La classe [**TCPIP \_ TypeGroup4**](tcpip-typegroup4.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="2d216-152">Valore del tipo di evento, 29</span><span class="sxs-lookup"><span data-stu-id="2d216-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="2d216-153">Evento Disconnect per protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d216-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="2d216-154">La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="2d216-155">Valore del tipo di evento, 30</span><span class="sxs-lookup"><span data-stu-id="2d216-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="2d216-156">Ritrasmissione dell'evento per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d216-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="2d216-157">La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="2d216-158">Valore del tipo di evento, 31</span><span class="sxs-lookup"><span data-stu-id="2d216-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="2d216-159">Evento Accept per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d216-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="2d216-160">La classe [**TCPIP \_ TypeGroup4**](tcpip-typegroup4.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="2d216-161">Valore del tipo di evento, 32</span><span class="sxs-lookup"><span data-stu-id="2d216-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="2d216-162">Riconnetti evento per protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d216-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="2d216-163">Un tentativo di connessione non è riuscito e viene effettuato un altro tentativo. La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="2d216-164">Valore del tipo di evento, 34</span><span class="sxs-lookup"><span data-stu-id="2d216-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="2d216-165">Evento di copia TCP per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d216-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="2d216-166">La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="2d216-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="2d216-167">È possibile tracciare gli eventi di rete in un processo di origine e di destinazione usando la proprietà **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="2d216-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="2d216-168">Poiché alcuni eventi di rete vengono registrati da thread distinti, potrebbe non essere possibile usare i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha originato le attività di rete.</span><span class="sxs-lookup"><span data-stu-id="2d216-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d216-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d216-169">Requirements</span></span>



| <span data-ttu-id="2d216-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d216-170">Requirement</span></span> | <span data-ttu-id="2d216-171">Valore</span><span class="sxs-lookup"><span data-stu-id="2d216-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2d216-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d216-172">Minimum supported client</span></span><br/> | <span data-ttu-id="2d216-173">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d216-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2d216-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d216-174">Minimum supported server</span></span><br/> | <span data-ttu-id="2d216-175">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d216-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d216-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d216-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d216-177">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="2d216-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="2d216-178">**\_Errore Tcpip**</span><span class="sxs-lookup"><span data-stu-id="2d216-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="2d216-179">**\_SendIPV4 Tcpip**</span><span class="sxs-lookup"><span data-stu-id="2d216-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="2d216-180">**\_SendIPV6 Tcpip**</span><span class="sxs-lookup"><span data-stu-id="2d216-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="2d216-181">**\_TypeGroup1 Tcpip**</span><span class="sxs-lookup"><span data-stu-id="2d216-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="2d216-182">**\_TypeGroup2 Tcpip**</span><span class="sxs-lookup"><span data-stu-id="2d216-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="2d216-183">**\_TypeGroup3 Tcpip**</span><span class="sxs-lookup"><span data-stu-id="2d216-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="2d216-184">**\_TypeGroup4 Tcpip**</span><span class="sxs-lookup"><span data-stu-id="2d216-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="2d216-185">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="2d216-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="2d216-186">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="2d216-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
