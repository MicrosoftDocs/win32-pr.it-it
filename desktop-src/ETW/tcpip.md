---
description: 'Classe TcpIp: questa classe è la classe padre per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.'
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
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105729"
---
# <a name="tcpip-class"></a><span data-ttu-id="5e91e-104">Classe TcpIp</span><span class="sxs-lookup"><span data-stu-id="5e91e-104">TcpIp class</span></span>

<span data-ttu-id="5e91e-105">Questa classe è la classe padre per gli eventi TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="5e91e-105">This class is the parent class for TCP/IP events.</span></span>

<span data-ttu-id="5e91e-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="5e91e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e91e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e91e-107">Syntax</span></span>

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="5e91e-108">Members</span><span class="sxs-lookup"><span data-stu-id="5e91e-108">Members</span></span>

<span data-ttu-id="5e91e-109">La **classe TcpIp** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="5e91e-109">The **TcpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e91e-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e91e-110">Remarks</span></span>

<span data-ttu-id="5e91e-111">Per abilitare gli eventi TCP/IP in una sessione di registrazione del kernel NT, specificare il flag **NETWORK \_ \_ \_ \_ TCPIP EVENT TRACE FLAG nel** membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="5e91e-111">To enable TCP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="5e91e-112">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi TCP/IP chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**TcpIpGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="5e91e-112">Event trace consumers can implement special processing for TCP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**TcpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="5e91e-113">Utilizzare i tipi di evento seguenti per identificare l'evento di rete effettivo (TCP/IP) quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="5e91e-113">Use the following event types to identify the actual network (TCP/IP) event when consuming events.</span></span>



| <span data-ttu-id="5e91e-114">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="5e91e-114">Event type</span></span>                                                            | <span data-ttu-id="5e91e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e91e-115">Description</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e91e-116">**EVENTO \_ TRACE \_ TYPE \_ ACCEPT**(il valore del tipo di evento è 15)</span><span class="sxs-lookup"><span data-stu-id="5e91e-116">**EVENT\_TRACE\_TYPE\_ACCEPT**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="5e91e-117">Accettare l'evento per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e91e-117">Accept event for IPv4 protocol.</span></span> <span data-ttu-id="5e91e-118">La [**classe \_ MOF TypeGroup2 TcpIp**](tcpip-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-118">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="5e91e-119">**EVENTO \_ TRACE \_ TYPE \_ CONNECT**(il valore del tipo di evento è 12)</span><span class="sxs-lookup"><span data-stu-id="5e91e-119">**EVENT\_TRACE\_TYPE\_CONNECT**(Event type value is 12)</span></span><br/>    | <span data-ttu-id="5e91e-120">Evento Connect per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e91e-120">Connect event for IPv4 protocol.</span></span> <span data-ttu-id="5e91e-121">La [**classe \_ MOF TypeGroup2 TcpIp**](tcpip-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-121">The [**TcpIp\_TypeGroup2**](tcpip-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="5e91e-122">**EVENTO \_ TRACE \_ TYPE \_ DISCONNECT**(il valore del tipo di evento è 13)</span><span class="sxs-lookup"><span data-stu-id="5e91e-122">**EVENT\_TRACE\_TYPE\_DISCONNECT**(Event type value is 13)</span></span><br/> | <span data-ttu-id="5e91e-123">Evento di disconnessione per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e91e-123">Disconnect event for IPv4 protocol.</span></span> <span data-ttu-id="5e91e-124">La [**classe MOF \_ TypeGroup1 TcpIp**](tcpip-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-124">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="5e91e-125">**EVENTO \_ TRACE \_ TYPE \_ RECEIVE**(il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="5e91e-125">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/>    | <span data-ttu-id="5e91e-126">Evento di ricezione per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e91e-126">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="5e91e-127">La [**classe MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-127">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="5e91e-128">**EVENTO \_ TRACE \_ TYPE \_ RECONNECT**(il valore del tipo di evento è 16)</span><span class="sxs-lookup"><span data-stu-id="5e91e-128">**EVENT\_TRACE\_TYPE\_RECONNECT**(Event type value is 16)</span></span><br/>  | <span data-ttu-id="5e91e-129">Evento di riconnessione per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e91e-129">Reconnect event for IPv4 protocol.</span></span> <span data-ttu-id="5e91e-130">Un tentativo di connessione non è riuscito e viene eseguito un altro tentativo. La [**classe MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-130">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="5e91e-131">**EVENTO \_ TRACE \_ TYPE \_ RETRANSMIT**(il valore del tipo di evento è 14)</span><span class="sxs-lookup"><span data-stu-id="5e91e-131">**EVENT\_TRACE\_TYPE\_RETRANSMIT**(Event type value is 14)</span></span><br/> | <span data-ttu-id="5e91e-132">Evento di ritrasmissione per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e91e-132">Retransmit event for IPv4 protocol.</span></span> <span data-ttu-id="5e91e-133">La [**classe MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-133">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="5e91e-134">**EVENTO \_ TRACE \_ TYPE \_ SEND**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="5e91e-134">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>       | <span data-ttu-id="5e91e-135">Evento di invio per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e91e-135">Send event for IPv4 protocol.</span></span> <span data-ttu-id="5e91e-136">La [**classe MOF TcpIp \_ SendIPV4**](tcpip-sendipv4.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-136">The [**TcpIp\_SendIPV4**](tcpip-sendipv4.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="5e91e-137">Valore del tipo di evento, 17</span><span class="sxs-lookup"><span data-stu-id="5e91e-137">Event type value, 17</span></span>                                                  | <span data-ttu-id="5e91e-138">Evento Fail.</span><span class="sxs-lookup"><span data-stu-id="5e91e-138">Fail event.</span></span> <span data-ttu-id="5e91e-139">La [**classe MOF TcpIp \_ Fail**](tcpip-fail.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-139">The [**TcpIp\_Fail**](tcpip-fail.md) MOF class defines the event data for this event.</span></span>                                                                                            |
| <span data-ttu-id="5e91e-140">Valore del tipo di evento, 18</span><span class="sxs-lookup"><span data-stu-id="5e91e-140">Event type value, 18</span></span>                                                  | <span data-ttu-id="5e91e-141">Evento di copia TCP per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="5e91e-141">TCP copy event for IPv4 protocol.</span></span> <span data-ttu-id="5e91e-142">La [**classe MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-142">The [**TcpIp\_TypeGroup1**](tcpip-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                          |
| <span data-ttu-id="5e91e-143">Valore del tipo di evento, 26</span><span class="sxs-lookup"><span data-stu-id="5e91e-143">Event type value, 26</span></span>                                                  | <span data-ttu-id="5e91e-144">Evento di invio per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5e91e-144">Send event for IPv6 protocol.</span></span> <span data-ttu-id="5e91e-145">La [**classe MOF TcpIp \_ SendIPV6**](tcpip-sendipv6.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-145">The [**TcpIp\_SendIPV6**](tcpip-sendipv6.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="5e91e-146">Valore del tipo di evento, 27</span><span class="sxs-lookup"><span data-stu-id="5e91e-146">Event type value, 27</span></span>                                                  | <span data-ttu-id="5e91e-147">Evento di ricezione per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5e91e-147">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="5e91e-148">La [**classe \_ MOF TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-148">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="5e91e-149">Valore del tipo di evento, 28</span><span class="sxs-lookup"><span data-stu-id="5e91e-149">Event type value, 28</span></span>                                                  | <span data-ttu-id="5e91e-150">Evento Connect per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5e91e-150">Connect event for IPv6 protocol.</span></span> <span data-ttu-id="5e91e-151">La [**classe \_ MOF TypeGroup4 TcpIp**](tcpip-typegroup4.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-151">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                           |
| <span data-ttu-id="5e91e-152">Valore del tipo di evento, 29</span><span class="sxs-lookup"><span data-stu-id="5e91e-152">Event type value, 29</span></span>                                                  | <span data-ttu-id="5e91e-153">Evento di disconnessione per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5e91e-153">Disconnect event for IPv6 protocol.</span></span> <span data-ttu-id="5e91e-154">La [**classe \_ MOF TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-154">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="5e91e-155">Valore del tipo di evento, 30</span><span class="sxs-lookup"><span data-stu-id="5e91e-155">Event type value, 30</span></span>                                                  | <span data-ttu-id="5e91e-156">Evento di ritrasmissione per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5e91e-156">Retransmit event for IPv6 protocol.</span></span> <span data-ttu-id="5e91e-157">La [**classe \_ MOF TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-157">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                        |
| <span data-ttu-id="5e91e-158">Valore del tipo di evento, 31</span><span class="sxs-lookup"><span data-stu-id="5e91e-158">Event type value, 31</span></span>                                                  | <span data-ttu-id="5e91e-159">Accettare l'evento per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5e91e-159">Accept event for IPv6 protocol.</span></span> <span data-ttu-id="5e91e-160">La [**classe \_ MOF TypeGroup4 TcpIp**](tcpip-typegroup4.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-160">The [**TcpIp\_TypeGroup4**](tcpip-typegroup4.md) MOF class defines the event data for this event.</span></span>                                                            |
| <span data-ttu-id="5e91e-161">Valore del tipo di evento, 32</span><span class="sxs-lookup"><span data-stu-id="5e91e-161">Event type value, 32</span></span>                                                  | <span data-ttu-id="5e91e-162">Evento di riconnessione per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5e91e-162">Reconnect event for IPv6 protocol.</span></span> <span data-ttu-id="5e91e-163">Un tentativo di connessione non è riuscito e viene eseguito un altro tentativo. La [**classe \_ MOF TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-163">(A connect attempt failed and another attempt is made.) The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="5e91e-164">Valore del tipo di evento, 34</span><span class="sxs-lookup"><span data-stu-id="5e91e-164">Event type value, 34</span></span>                                                  | <span data-ttu-id="5e91e-165">Evento di copia TCP per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5e91e-165">TCP copy event for IPv6 protocol.</span></span> <span data-ttu-id="5e91e-166">La [**classe MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5e91e-166">The [**TcpIp\_TypeGroup3**](tcpip-typegroup3.md) MOF class defines the event data for this event.</span></span>                                                          |



 

<span data-ttu-id="5e91e-167">È possibile tracciare gli eventi di rete in un processo di origine e di destinazione usando la **proprietà ProcessId.**</span><span class="sxs-lookup"><span data-stu-id="5e91e-167">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="5e91e-168">Poiché alcuni eventi di rete vengono registrati da thread separati, potrebbe non essere possibile usare i membri **ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha originato le attività di rete.</span><span class="sxs-lookup"><span data-stu-id="5e91e-168">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e91e-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e91e-169">Requirements</span></span>



| <span data-ttu-id="5e91e-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e91e-170">Requirement</span></span> | <span data-ttu-id="5e91e-171">Valore</span><span class="sxs-lookup"><span data-stu-id="5e91e-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e91e-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e91e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="5e91e-173">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e91e-173">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e91e-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e91e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="5e91e-175">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e91e-175">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e91e-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e91e-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e91e-177">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="5e91e-177">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="5e91e-178">**TcpIp \_ Fail**</span><span class="sxs-lookup"><span data-stu-id="5e91e-178">**TcpIp\_Fail**</span></span>](tcpip-fail.md)
</dt> <dt>

[<span data-ttu-id="5e91e-179">**TcpIp \_ SendIPV4**</span><span class="sxs-lookup"><span data-stu-id="5e91e-179">**TcpIp\_SendIPV4**</span></span>](tcpip-sendipv4.md)
</dt> <dt>

[<span data-ttu-id="5e91e-180">**TcpIp \_ SendIPV6**</span><span class="sxs-lookup"><span data-stu-id="5e91e-180">**TcpIp\_SendIPV6**</span></span>](tcpip-sendipv6.md)
</dt> <dt>

[<span data-ttu-id="5e91e-181">**TcpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="5e91e-181">**TcpIp\_TypeGroup1**</span></span>](tcpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="5e91e-182">**TcpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="5e91e-182">**TcpIp\_TypeGroup2**</span></span>](tcpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="5e91e-183">**TcpIp \_ TypeGroup3**</span><span class="sxs-lookup"><span data-stu-id="5e91e-183">**TcpIp\_TypeGroup3**</span></span>](tcpip-typegroup3.md)
</dt> <dt>

[<span data-ttu-id="5e91e-184">**TypeGroup \_ TcpIp4**</span><span class="sxs-lookup"><span data-stu-id="5e91e-184">**TcpIp\_TypeGroup4**</span></span>](tcpip-typegroup4.md)
</dt> <dt>

[<span data-ttu-id="5e91e-185">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="5e91e-185">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> <dt>

[<span data-ttu-id="5e91e-186">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="5e91e-186">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 
