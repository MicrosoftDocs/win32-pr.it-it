---
description: Questa classe è la classe padre per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Classe UdpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527288"
---
# <a name="udpip-class"></a><span data-ttu-id="7ebe2-104">Classe UdpIp</span><span class="sxs-lookup"><span data-stu-id="7ebe2-104">UdpIp class</span></span>

<span data-ttu-id="7ebe2-105">Questa classe è la classe padre per gli eventi UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="7ebe2-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebe2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ebe2-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="7ebe2-108">Members</span><span class="sxs-lookup"><span data-stu-id="7ebe2-108">Members</span></span>

<span data-ttu-id="7ebe2-109">La classe **UdpIp** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ebe2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ebe2-110">Remarks</span></span>

<span data-ttu-id="7ebe2-111">Per abilitare gli eventi UDP/IP in una sessione di registrazione del kernel NT, specificare il flag **tcpip di rete del flag di \_ traccia \_ \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="7ebe2-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="7ebe2-112">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi UDP/IP chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**UdpIpGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="7ebe2-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="7ebe2-113">Usare i tipi di eventi seguenti per identificare l'evento di rete (UDP/IP) effettivo quando si utilizzano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="7ebe2-114">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="7ebe2-114">Event type</span></span>                                                         | <span data-ttu-id="7ebe2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ebe2-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ebe2-116">**Evento \_ Tipo di traccia \_ \_ Receive**(il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="7ebe2-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="7ebe2-117">Evento di ricezione per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="7ebe2-118">La classe MOF [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="7ebe2-119">**Evento \_ Tipo di traccia \_ \_ Send**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="7ebe2-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="7ebe2-120">Inviare un evento per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="7ebe2-121">La classe MOF [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="7ebe2-122">Valore del tipo di evento, 17</span><span class="sxs-lookup"><span data-stu-id="7ebe2-122">Event type value, 17</span></span>                                               | <span data-ttu-id="7ebe2-123">Evento fail.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-123">Fail event.</span></span> <span data-ttu-id="7ebe2-124">La classe MOF [**UdpIp \_ Fail**](udpip-fail.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="7ebe2-125">Valore del tipo di evento, 26</span><span class="sxs-lookup"><span data-stu-id="7ebe2-125">Event type value, 26</span></span>                                               | <span data-ttu-id="7ebe2-126">Inviare un evento per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="7ebe2-127">La classe MOF [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="7ebe2-128">Valore del tipo di evento, 27</span><span class="sxs-lookup"><span data-stu-id="7ebe2-128">Event type value, 27</span></span>                                               | <span data-ttu-id="7ebe2-129">Evento di ricezione per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="7ebe2-130">La classe MOF [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="7ebe2-131">È possibile tracciare gli eventi di rete in un processo di origine e di destinazione usando la proprietà **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="7ebe2-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="7ebe2-132">Poiché alcuni eventi di rete vengono registrati da thread distinti, potrebbe non essere possibile usare i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha originato le attività di rete.</span><span class="sxs-lookup"><span data-stu-id="7ebe2-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ebe2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ebe2-133">Requirements</span></span>



| <span data-ttu-id="7ebe2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ebe2-134">Requirement</span></span> | <span data-ttu-id="7ebe2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="7ebe2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ebe2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ebe2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7ebe2-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ebe2-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ebe2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ebe2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7ebe2-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ebe2-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ebe2-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ebe2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ebe2-141">**\_SYSTEMTRACE MSNT**</span><span class="sxs-lookup"><span data-stu-id="7ebe2-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="7ebe2-142">**UdpIp \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="7ebe2-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="7ebe2-143">**\_TypeGroup1 UdpIp**</span><span class="sxs-lookup"><span data-stu-id="7ebe2-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="7ebe2-144">**\_TypeGroup2 UdpIp**</span><span class="sxs-lookup"><span data-stu-id="7ebe2-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="7ebe2-145">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="7ebe2-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="7ebe2-146">**UdpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="7ebe2-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
