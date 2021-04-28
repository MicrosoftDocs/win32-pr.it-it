---
description: 'Classe UdpIp: questa classe è la classe padre per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.'
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
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105389"
---
# <a name="udpip-class"></a><span data-ttu-id="d0eff-104">Classe UdpIp</span><span class="sxs-lookup"><span data-stu-id="d0eff-104">UdpIp class</span></span>

<span data-ttu-id="d0eff-105">Questa classe è la classe padre per gli eventi UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="d0eff-105">This class is the parent class for UDP/IP events.</span></span>

<span data-ttu-id="d0eff-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="d0eff-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0eff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0eff-107">Syntax</span></span>

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="d0eff-108">Members</span><span class="sxs-lookup"><span data-stu-id="d0eff-108">Members</span></span>

<span data-ttu-id="d0eff-109">La **classe UdpIp** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="d0eff-109">The **UdpIp** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0eff-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0eff-110">Remarks</span></span>

<span data-ttu-id="d0eff-111">Per abilitare gli eventi UDP/IP in una sessione di registrazione del kernel NT, specificare il flag **EVENT TRACE FLAG NETWORK \_ \_ \_ \_ TCPIP** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)</span><span class="sxs-lookup"><span data-stu-id="d0eff-111">To enable UDP/IP events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="d0eff-112">I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi UDP/IP chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**UdpIpGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.*</span><span class="sxs-lookup"><span data-stu-id="d0eff-112">Event trace consumers can implement special processing for UDP/IP events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**UdpIpGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="d0eff-113">Usare i tipi di evento seguenti per identificare l'evento di rete effettivo (UDP/IP) quando si usano gli eventi.</span><span class="sxs-lookup"><span data-stu-id="d0eff-113">Use the following event types to identify the actual network (UDP/IP) event when consuming events.</span></span>



| <span data-ttu-id="d0eff-114">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="d0eff-114">Event type</span></span>                                                         | <span data-ttu-id="d0eff-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0eff-115">Description</span></span>                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0eff-116">**EVENTO \_ TRACE \_ TYPE \_ RECEIVE**(il valore del tipo di evento è 11)</span><span class="sxs-lookup"><span data-stu-id="d0eff-116">**EVENT\_TRACE\_TYPE\_RECEIVE**(Event type value is 11)</span></span><br/> | <span data-ttu-id="d0eff-117">Evento di ricezione per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="d0eff-117">Receive event for IPv4 protocol.</span></span> <span data-ttu-id="d0eff-118">La [**classe MOF \_ UdpIp TypeGroup1**](udpip-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="d0eff-118">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="d0eff-119">**EVENTO \_ TRACE \_ TYPE \_ SEND**(il valore del tipo di evento è 10)</span><span class="sxs-lookup"><span data-stu-id="d0eff-119">**EVENT\_TRACE\_TYPE\_SEND**(Event type value is 10)</span></span><br/>    | <span data-ttu-id="d0eff-120">Evento di invio per il protocollo IPv4.</span><span class="sxs-lookup"><span data-stu-id="d0eff-120">Send event for IPv4 protocol.</span></span> <span data-ttu-id="d0eff-121">La [**classe MOF \_ UdpIp TypeGroup1**](udpip-typegroup1.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="d0eff-121">The [**UdpIp\_TypeGroup1**](udpip-typegroup1.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="d0eff-122">Valore del tipo di evento, 17</span><span class="sxs-lookup"><span data-stu-id="d0eff-122">Event type value, 17</span></span>                                               | <span data-ttu-id="d0eff-123">Evento Fail.</span><span class="sxs-lookup"><span data-stu-id="d0eff-123">Fail event.</span></span> <span data-ttu-id="d0eff-124">La [**classe MOF UdpIp \_ Fail**](udpip-fail.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="d0eff-124">The [**UdpIp\_Fail**](udpip-fail.md) MOF class defines the event data for this event.</span></span>                                  |
| <span data-ttu-id="d0eff-125">Valore del tipo di evento, 26</span><span class="sxs-lookup"><span data-stu-id="d0eff-125">Event type value, 26</span></span>                                               | <span data-ttu-id="d0eff-126">Evento di invio per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="d0eff-126">Send event for IPv6 protocol.</span></span> <span data-ttu-id="d0eff-127">La [**classe \_ MOF UdpIp TypeGroup2**](udpip-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="d0eff-127">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span>    |
| <span data-ttu-id="d0eff-128">Valore del tipo di evento, 27</span><span class="sxs-lookup"><span data-stu-id="d0eff-128">Event type value, 27</span></span>                                               | <span data-ttu-id="d0eff-129">Evento di ricezione per il protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="d0eff-129">Receive event for IPv6 protocol.</span></span> <span data-ttu-id="d0eff-130">La [**classe \_ MOF UdpIp TypeGroup2**](udpip-typegroup2.md) definisce i dati dell'evento per questo evento.</span><span class="sxs-lookup"><span data-stu-id="d0eff-130">The [**UdpIp\_TypeGroup2**](udpip-typegroup2.md) MOF class defines the event data for this event.</span></span> |



 

<span data-ttu-id="d0eff-131">È possibile tracciare gli eventi di rete in un processo di origine e di destinazione usando la **proprietà ProcessId.**</span><span class="sxs-lookup"><span data-stu-id="d0eff-131">You can trace network events to a source and destination process using the **ProcessId** property.</span></span> <span data-ttu-id="d0eff-132">Poiché alcuni eventi di rete vengono registrati da thread separati, potrebbe non essere possibile usare i membri **ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha originato le attività di rete.</span><span class="sxs-lookup"><span data-stu-id="d0eff-132">Because some network events are logged by separate threads, you may not be able to use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the process or thread that originated the network activities.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0eff-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0eff-133">Requirements</span></span>



| <span data-ttu-id="d0eff-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0eff-134">Requirement</span></span> | <span data-ttu-id="d0eff-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d0eff-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d0eff-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0eff-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d0eff-137">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d0eff-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d0eff-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0eff-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d0eff-139">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0eff-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0eff-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0eff-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0eff-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="d0eff-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="d0eff-142">**UdpIp \_ Fail**</span><span class="sxs-lookup"><span data-stu-id="d0eff-142">**UdpIp\_Fail**</span></span>](udpip-fail.md)
</dt> <dt>

[<span data-ttu-id="d0eff-143">**UdpIp \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="d0eff-143">**UdpIp\_TypeGroup1**</span></span>](udpip-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="d0eff-144">**UdpIp \_ TypeGroup2**</span><span class="sxs-lookup"><span data-stu-id="d0eff-144">**UdpIp\_TypeGroup2**</span></span>](udpip-typegroup2.md)
</dt> <dt>

[<span data-ttu-id="d0eff-145">**UdpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="d0eff-145">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> <dt>

[<span data-ttu-id="d0eff-146">**UdpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="d0eff-146">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> </dl>

 

 
