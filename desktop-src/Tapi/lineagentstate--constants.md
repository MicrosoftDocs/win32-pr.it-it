---
description: Le \_ costanti LINEAGENTSTATE descrivono lo stato di un agente in un indirizzo.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Costanti LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332914"
---
# <a name="lineagentstate_-constants"></a><span data-ttu-id="b215b-103">\_Costanti LINEAGENTSTATE</span><span class="sxs-lookup"><span data-stu-id="b215b-103">LINEAGENTSTATE\_ Constants</span></span>

<span data-ttu-id="b215b-104">Le **\_ costanti LINEAGENTSTATE** descrivono lo stato di un agente in un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="b215b-104">The **LINEAGENTSTATE\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="b215b-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**\_BUSYACD LINEAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="b215b-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-106">L'agente è occupato a gestire una chiamata instradata da una coda ACD.</span><span class="sxs-lookup"><span data-stu-id="b215b-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**\_BUSYINCOMING LINEAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="b215b-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-108">L'agente è occupato a gestire una chiamata in ingresso che non è stata trasferita all'agente da una coda ACD in cui è connesso l'agente.</span><span class="sxs-lookup"><span data-stu-id="b215b-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**\_BUSYOTHER LINEAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="b215b-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE\_BUSYOTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-110">L'agente occupa la gestione di un altro tipo di chiamata, ad esempio una chiamata personale in uscita non trasferita all'agente da un dialer predittivo.</span><span class="sxs-lookup"><span data-stu-id="b215b-110">The agent is busy handling another type of call, such as an outgoing personal call not transferred to the agent by a predictive dialer.</span></span> <span data-ttu-id="b215b-111">Questo valore può essere utilizzato anche quando l'agente è noto come occupato in una chiamata, ma il tipo di chiamata è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b215b-111">This value can also be used when the agent is known to be busy on a call but the type of call is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**\_BUSYOUTBOUND LINEAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="b215b-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE\_BUSYOUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-113">L'agente è occupato a gestire una chiamata in uscita, ad esempio una instradata da una coda di composizione predittiva.</span><span class="sxs-lookup"><span data-stu-id="b215b-113">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**\_LOGGEDOFF LINEAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="b215b-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE\_LOGGEDOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-115">Nessun agente è connesso all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="b215b-115">No agent is logged in on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ NObattistrada**</span><span class="sxs-lookup"><span data-stu-id="b215b-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-117">L'agente è connesso, ma è occupato da un'attività diversa da quella di una chiamata (ad esempio, in pausa).</span><span class="sxs-lookup"><span data-stu-id="b215b-117">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="b215b-118">Nessuna chiamata aggiuntiva deve essere indirizzata all'agente.</span><span class="sxs-lookup"><span data-stu-id="b215b-118">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="b215b-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-120">L'agente è pronto per accettare le chiamate.</span><span class="sxs-lookup"><span data-stu-id="b215b-120">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="b215b-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-122">Lo stato dell'agente è sconosciuto e non verrà mai reso noto.</span><span class="sxs-lookup"><span data-stu-id="b215b-122">The agent state is unknown and will never become known.</span></span> <span data-ttu-id="b215b-123">In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)questa condizione può essere rappresentata anche dal membro **dwAgentState** impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="b215b-123">In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), this condition can also be represented by the **dwAgentState** member being set to 0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="b215b-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-125">Lo stato dell'agente è attualmente sconosciuto, ma può diventare noto in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="b215b-125">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="b215b-126">Questo può essere uno stato di transizione quando una linea o un indirizzo viene aperto per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="b215b-126">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b215b-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**\_WORKINGAFTERCALL LINEAGENTSTATE**</span><span class="sxs-lookup"><span data-stu-id="b215b-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE\_WORKINGAFTERCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b215b-128">L'agente ha completato la chiamata precedente, ma è ancora occupato con il lavoro correlato alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="b215b-128">The agent has completed the preceding call, but is still occupied with work related to that call.</span></span> <span data-ttu-id="b215b-129">L'agente non deve ricevere chiamate aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="b215b-129">The agent should not receive additional calls.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b215b-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b215b-130">Remarks</span></span>

<span data-ttu-id="b215b-131">I 16 bit superiori di questo set di costanti sono riservati per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b215b-131">The upper 16 bits of this set of constants are reserved for device-specific extensions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b215b-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b215b-132">Requirements</span></span>



| <span data-ttu-id="b215b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b215b-133">Requirement</span></span> | <span data-ttu-id="b215b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b215b-134">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b215b-135">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="b215b-135">TAPI version</span></span><br/> | <span data-ttu-id="b215b-136">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b215b-136">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b215b-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b215b-137">Header</span></span><br/>       | <dl> <span data-ttu-id="b215b-138"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b215b-138"><dt>Tapi.h</dt></span></span> </dl> |



 

 




