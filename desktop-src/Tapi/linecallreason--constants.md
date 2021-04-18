---
description: Le \_ costanti del flag di bit LINECALLREASON descrivono il motivo di una chiamata.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Costanti LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324879"
---
# <a name="linecallreason_-constants"></a><span data-ttu-id="a8dfa-103">\_Costanti LINECALLREASON</span><span class="sxs-lookup"><span data-stu-id="a8dfa-103">LINECALLREASON\_ Constants</span></span>

<span data-ttu-id="a8dfa-104">Le costanti del flag di bit **LINECALLREASON \_** descrivono il motivo di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-104">The **LINECALLREASON\_** bit-flag constants describe the reason for a call.</span></span>

<dl> <dt>

<span data-ttu-id="a8dfa-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**\_CALLCOMPLETION LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON\_CALLCOMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-106">La chiamata è stata il risultato di una richiesta di completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-106">The call was the result of a call completion request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**\_CAMPEDON LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON\_CAMPEDON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-108">La chiamata è stata campata sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-108">The call was camped on the address.</span></span> <span data-ttu-id="a8dfa-109">Generalmente, viene visualizzato inizialmente nello stato onHolding e può essere passato all'uso di [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span><span class="sxs-lookup"><span data-stu-id="a8dfa-109">Usually, it appears initially in the onhold state, and can be switched to using [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span></span> <span data-ttu-id="a8dfa-110">Se una chiamata attiva diventa inattiva, la chiamata camped-on può variare in base allo stato dell'offerta e il dispositivo inizia a squillare.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-110">If an active call becomes idle, the camped-on call may change to the offering state and the device start ringing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-112">Si tratta di una chiamata diretta in ingresso o in uscita.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-112">This is a direct incoming or outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**\_FWDBUSY LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON\_FWDBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-114">Questa chiamata è stata trasmessa da un'altra estensione occupata al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-114">This call was forwarded from another extension that was busy at the time of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**\_FWDNOANSWER LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON\_FWDNOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-116">La chiamata è stata trasmessa da un'altra estensione che non ha risposto alla chiamata dopo un certo numero di anelli.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-116">The call was forwarded from another extension that didn't answer the call after some number of rings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**\_FWDUNCOND LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON\_FWDUNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-118">La chiamata è stata trasmessa in modo incondizionato da un altro numero.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-118">The call was forwarded unconditionally from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ intrusione**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-120">Chiamata interstata sulla riga, da un'azione di completamento della chiamata richiamata da un'altra stazione o da un'azione dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-120">The call intruded onto the line, either by a call completion action invoked by another station or by operator action.</span></span> <span data-ttu-id="a8dfa-121">A seconda dell'implementazione del Commuter, è possibile che la chiamata venga visualizzata nello stato connesso o in conferenza con una chiamata attiva esistente sulla riga.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-121">Depending on switch implementation, the call may appear either in the connected state, or conferenced with an existing active call on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ parcheggiata**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON\_PARKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-123">La chiamata è stata parcheggiata sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-123">The call was parked on the address.</span></span> <span data-ttu-id="a8dfa-124">Viene in genere visualizzato inizialmente nello stato onHolding.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-124">Usually, it appears initially in the onhold state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON \_ pickup**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-126">La chiamata è stata rilevata da un'altra estensione.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-126">The call was picked up from another extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**\_Reindirizzamento LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-128">La chiamata è stata reindirizzata a questa stazione.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-128">The call was redirected to this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**promemoria LINECALLREASON \_**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON\_REMINDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-130">La chiamata è un promemoria (o "richiamo") per cui l'utente ha una chiamata parcheggiata o in attesa (potenzialmente) per un lungo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-130">The call is a reminder (or "recall") that the user has a call parked or on hold for (potentially) a long time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**\_ROUTEREQUEST LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON\_ROUTEREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-132">La chiamata viene visualizzata sull'indirizzo perché per il commute sono necessarie istruzioni di routing dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-132">The call appears on the address because the switch needs routing instructions from the application.</span></span> <span data-ttu-id="a8dfa-133">L'applicazione deve esaminare il membro **CalledID** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)e utilizzare la funzione [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) per fornire un nuovo indirizzo di connessione per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-133">The application should examine the **CalledID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo), and use the [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) function to provide a new dialable address for the call.</span></span> <span data-ttu-id="a8dfa-134">Se invece la chiamata deve essere bloccata, l'applicazione può chiamare [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="a8dfa-134">If the call is to be blocked instead, the application may call [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span></span> <span data-ttu-id="a8dfa-135">Se l'applicazione non riesce a eseguire un'azione all'interno di un periodo di timeout definito dallo switch, viene eseguita un'azione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-135">If the application fails to take action within a switch-defined timeout period, a default action will be taken.</span></span> <span data-ttu-id="a8dfa-136">Un provider di servizi può usare questa costante solo se la versione negoziata nella riga è 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-136">A service provider can use this constant only if the negotiated version on the line is 2.0 or higher.</span></span> <span data-ttu-id="a8dfa-137">In caso contrario, il provider di servizi deve sostituire LINECALLREASON \_ undisp.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-137">Otherwise the service provider should substitute LINECALLREASON\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**\_trasferimento LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-139">La chiamata è stata trasferita da un altro numero.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-139">The call has been transferred from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-141">Il motivo della chiamata non è disponibile e non verrà più noto in seguito.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-141">The reason for the call is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-143">Il motivo della chiamata è attualmente sconosciuto, ma può diventare noto in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-143">The reason for the call is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8dfa-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON \_ UNpark**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a8dfa-145">La chiamata è stata recuperata come chiamata parcheggiata.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-145">The call was retrieved as a parked call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8dfa-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8dfa-146">Remarks</span></span>

<span data-ttu-id="a8dfa-147">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-147">No extensibility.</span></span> <span data-ttu-id="a8dfa-148">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="a8dfa-148">All 32 bits are reserved.</span></span>

<span data-ttu-id="a8dfa-149">Le \_ costanti LINECALLREASON vengono usate nel membro **dwReason** della struttura di dati [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="a8dfa-149">The LINECALLREASON\_ constants are used in the **dwReason** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8dfa-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8dfa-150">Requirements</span></span>



| <span data-ttu-id="a8dfa-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8dfa-151">Requirement</span></span> | <span data-ttu-id="a8dfa-152">Valore</span><span class="sxs-lookup"><span data-stu-id="a8dfa-152">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a8dfa-153">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a8dfa-153">TAPI version</span></span><br/> | <span data-ttu-id="a8dfa-154">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a8dfa-154">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a8dfa-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8dfa-155">Header</span></span><br/>       | <dl> <span data-ttu-id="a8dfa-156"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8dfa-156"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8dfa-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8dfa-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8dfa-158">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-158">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="a8dfa-159">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-159">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="a8dfa-160">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-160">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[<span data-ttu-id="a8dfa-161">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="a8dfa-161">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




