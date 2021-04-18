---
description: Le \_ costanti del flag di bit LINEDISCONNECTMODE descrivono motivi diversi per una richiesta di disconnessione remota. Una modalità di disconnessione è disponibile come stato della chiamata all'applicazione dopo la transizione dello stato della chiamata a disconnected.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Costanti LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331778"
---
# <a name="linedisconnectmode_-constants"></a><span data-ttu-id="3a23d-104">\_Costanti LINEDISCONNECTMODE</span><span class="sxs-lookup"><span data-stu-id="3a23d-104">LINEDISCONNECTMODE\_ Constants</span></span>

<span data-ttu-id="3a23d-105">Le costanti del flag di bit **LINEDISCONNECTMODE \_** descrivono motivi diversi per una richiesta di disconnessione remota.</span><span class="sxs-lookup"><span data-stu-id="3a23d-105">The **LINEDISCONNECTMODE\_** bit-flag constants describe different reasons for a remote disconnect request.</span></span> <span data-ttu-id="3a23d-106">Una modalità di disconnessione è disponibile come stato della chiamata all'applicazione dopo la transizione dello stato della chiamata a disconnected.</span><span class="sxs-lookup"><span data-stu-id="3a23d-106">A disconnect mode is available as call status to the application after the call state transitions to disconnected.</span></span>

<dl> <dt>

<span data-ttu-id="3a23d-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**\_BADADDRESS LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="3a23d-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE\_BADADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-108">L'indirizzo di destinazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="3a23d-108">The destination address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ bloccati**</span><span class="sxs-lookup"><span data-stu-id="3a23d-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-110">Impossibile connettere la chiamata poiché le chiamate dall'indirizzo di origine non vengono accettate nell'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3a23d-110">The call could not be connected because calls from the origination address are not being accepted at the destination address.</span></span> <span data-ttu-id="3a23d-111">Questo comportamento è diverso da quello di LINEDISCONNECTMODE, \_ in quanto il blocco viene implementato nella rete (un rifiuto passivo), mentre un rifiuto viene implementato nell'attrezzatura di destinazione (rifiuto attivo).</span><span class="sxs-lookup"><span data-stu-id="3a23d-111">This differs from LINEDISCONNECTMODE\_REJECT in that blocking is implemented in the network (a passive reject) while a rejection is implemented in the destination equipment (an active reject).</span></span> <span data-ttu-id="3a23d-112">Il blocco può essere causato da un'esclusione specifica dell'indirizzo di origine o dal fatto che la destinazione accetta chiamate solo da un set di indirizzi di origine (gruppo di utenti chiusi) selezionato.</span><span class="sxs-lookup"><span data-stu-id="3a23d-112">The blocking can be due to a specific exclusion of the origination address, or because the destination accepts calls from only a selected set of origination address (closed user group).</span></span> <span data-ttu-id="3a23d-113">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="3a23d-113">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="3a23d-114">Il \_ blocco LINEDISCONNECTMODE è appropriato come risposta Blocklisting.</span><span class="sxs-lookup"><span data-stu-id="3a23d-114">LINEDISCONNECTMODE\_BLOCKED is appropriate as a blocklisted response.</span></span> <span data-ttu-id="3a23d-115">Ad esempio, un modem ha ricevuto una risposta, più di sei secondi senza rilevare la rilevanza, non è stato possibile connettere un numero definito di volte, determina che il numero di telefono non è valido per la chiamata ed emette una risposta "Blocklisting".</span><span class="sxs-lookup"><span data-stu-id="3a23d-115">For example, a modem has received an answer, gone more than six seconds without detecting Ringback, failed to connect a defined number of times, determines that the phone number is not valid to call, and issues a 'blocklisted' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="3a23d-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-117">La stazione dell'utente remoto è occupata.</span><span class="sxs-lookup"><span data-stu-id="3a23d-117">The remote user's station is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="3a23d-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-119">La chiamata è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="3a23d-119">The call was cancelled.</span></span> <span data-ttu-id="3a23d-120">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="3a23d-120">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**congestione LINEDISCONNECTMODE \_**</span><span class="sxs-lookup"><span data-stu-id="3a23d-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE\_CONGESTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-122">La rete è congestionata.</span><span class="sxs-lookup"><span data-stu-id="3a23d-122">The network is congested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**\_DONOTDISTURB LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="3a23d-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE\_DONOTDISTURB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-124">Impossibile connettere la chiamata perché la destinazione ha richiamato la funzionalità non disturbare.</span><span class="sxs-lookup"><span data-stu-id="3a23d-124">The call could not be connected because the destination has invoked the Do Not Disturb feature.</span></span> <span data-ttu-id="3a23d-125">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="3a23d-125">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE di \_ trasmissione**</span><span class="sxs-lookup"><span data-stu-id="3a23d-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-127">La chiamata è stata trasmessa dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="3a23d-127">The call was forwarded by the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INcompatibile**</span><span class="sxs-lookup"><span data-stu-id="3a23d-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-129">L'apparecchiatura della stazione dell'utente remoto non è compatibile con il tipo di chiamata richiesta.</span><span class="sxs-lookup"><span data-stu-id="3a23d-129">The remote user's station equipment is incompatible with the type of call requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOanswer**</span><span class="sxs-lookup"><span data-stu-id="3a23d-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE\_NOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-131">La stazione dell'utente remoto non risponde.</span><span class="sxs-lookup"><span data-stu-id="3a23d-131">The remote user's station does not answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**\_NODIALTONE LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="3a23d-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE\_NODIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-133">Un tono di composizione non è stato rilevato all'interno di un timeout definito dal provider di servizi, in un determinato momento durante la composizione quando ne era previsto uno (ad esempio, "W" nella stringa di connessione remota).</span><span class="sxs-lookup"><span data-stu-id="3a23d-133">A dial tone was not detected within a service-provider defined timeout, at a point during dialing when one was expected (such as at a "W" in the dialable string).</span></span> <span data-ttu-id="3a23d-134">Questo può verificarsi anche senza un periodo di timeout definito dal provider di servizi o senza un valore specificato nel membro **dwWaitForDialTone** della struttura [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) .</span><span class="sxs-lookup"><span data-stu-id="3a23d-134">This can also occur without a service-provider-defined timeout period or without a value specified in the **dwWaitForDialTone** member of the [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) structure.</span></span> <span data-ttu-id="3a23d-135">(Versioni TAPI 1,4 e successive)</span><span class="sxs-lookup"><span data-stu-id="3a23d-135">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ normale**</span><span class="sxs-lookup"><span data-stu-id="3a23d-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-137">Si tratta di una normale richiesta di disconnessione da parte della parte remota.</span><span class="sxs-lookup"><span data-stu-id="3a23d-137">This is a normal disconnect request by the remote party.</span></span> <span data-ttu-id="3a23d-138">La chiamata è stata terminata normalmente.</span><span class="sxs-lookup"><span data-stu-id="3a23d-138">The call was terminated normally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**\_NUMBERCHANGED LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="3a23d-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE\_NUMBERCHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-140">Non è stato possibile connettere la chiamata perché il numero di destinazione è stato modificato, ma non è stato specificato il reindirizzamento automatico al nuovo numero.</span><span class="sxs-lookup"><span data-stu-id="3a23d-140">The call could not be connected because the destination number has been changed, but automatic redirection to the new number is not provided.</span></span> <span data-ttu-id="3a23d-141">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="3a23d-141">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**\_OUTOFORDER LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="3a23d-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE\_OUTOFORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-143">La chiamata non è stata connessa o è stata disconnessa perché il dispositivo di destinazione non è in ordine (errore hardware).</span><span class="sxs-lookup"><span data-stu-id="3a23d-143">The call could not be connected or was disconnected because the destination device is out of order (hardware failure).</span></span> <span data-ttu-id="3a23d-144">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="3a23d-144">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE \_ pickup**</span><span class="sxs-lookup"><span data-stu-id="3a23d-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-146">La chiamata è stata prelevata da un'altra posizione.</span><span class="sxs-lookup"><span data-stu-id="3a23d-146">The call was picked up from elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**\_QOSUNAVAIL LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="3a23d-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE\_QOSUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-148">Non è stato possibile connettere la chiamata o è stata disconnessa perché non è stato possibile ottenere o sostenere la qualità del servizio minima.</span><span class="sxs-lookup"><span data-stu-id="3a23d-148">The call could not be connected or was disconnected because the minimum quality of service could not be obtained or sustained.</span></span> <span data-ttu-id="3a23d-149">Questo comportamento è diverso da LINEDISCONNECTMODE \_ incompatibile perché la mancanza di risorse può essere una condizione temporanea nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="3a23d-149">This differs from LINEDISCONNECTMODE\_INCOMPATIBLE in that the lack of resources may be a temporary condition at the destination.</span></span> <span data-ttu-id="3a23d-150">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="3a23d-150">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ rifiuta**</span><span class="sxs-lookup"><span data-stu-id="3a23d-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE\_REJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-152">La chiamata è stata rifiutata dall'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="3a23d-152">The remote user has rejected the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**\_TEMPFAILURE LINEDISCONNECTMODE**</span><span class="sxs-lookup"><span data-stu-id="3a23d-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE\_TEMPFAILURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-154">Non è stato possibile connettere la chiamata o è stata disconnessa a causa di un errore temporaneo nella rete. la chiamata può essere ritentata in un secondo momento ed è prevista la fine del completamento.</span><span class="sxs-lookup"><span data-stu-id="3a23d-154">The call could not be connected or was disconnected because of a temporary failure in the network; the call can be reattempted later and is expected to eventually complete.</span></span> <span data-ttu-id="3a23d-155">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="3a23d-155">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="3a23d-156">LINEDISCONNECTMODE \_ TEMPFAILURE è appropriato come risposta ritardata.</span><span class="sxs-lookup"><span data-stu-id="3a23d-156">LINEDISCONNECTMODE\_TEMPFAILURE is appropriate as a delayed response.</span></span> <span data-ttu-id="3a23d-157">Ad esempio, un modem che riceve un segnale occupato o equivalente troppe volte in un determinato periodo di tempo conclude che il numero non deve essere chiamato di nuovo fino a quando non è trascorso un periodo definito e genera una risposta "ritardata".</span><span class="sxs-lookup"><span data-stu-id="3a23d-157">For example, a modem getting a busy signal or equivalent too many times in a particular time period concludes that the number should not be called again until a defined time has elapsed and issues a 'delayed' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="3a23d-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-159">Il motivo della disconnessione non è disponibile e non verrà più noto in seguito.</span><span class="sxs-lookup"><span data-stu-id="3a23d-159">The reason for the disconnect is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="3a23d-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-161">Il motivo della richiesta di disconnessione è sconosciuto, ma potrebbe essere noto in seguito.</span><span class="sxs-lookup"><span data-stu-id="3a23d-161">The reason for the disconnect request is unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a23d-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ irraggiungibile**</span><span class="sxs-lookup"><span data-stu-id="3a23d-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3a23d-163">Non è stato possibile raggiungere l'utente remoto.</span><span class="sxs-lookup"><span data-stu-id="3a23d-163">The remote user could not be reached.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a23d-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a23d-164">Remarks</span></span>

<span data-ttu-id="3a23d-165">È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a23d-165">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="3a23d-166">I 16 bit di ordine inferiore sono riservati.</span><span class="sxs-lookup"><span data-stu-id="3a23d-166">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="3a23d-167">Una richiesta di disconnessione remota per una determinata chiamata determina la transizione dello stato della chiamata allo stato disconnesso e all'applicazione viene inviato un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) .</span><span class="sxs-lookup"><span data-stu-id="3a23d-167">A remote disconnect request for a given call results in the call state transitioning to the disconnected state and a [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="3a23d-168">Le \_ informazioni LINEDISCONNECTMODE forniscono informazioni dettagliate sulla richiesta di disconnessione remota.</span><span class="sxs-lookup"><span data-stu-id="3a23d-168">The LINEDISCONNECTMODE\_ information provides details about the remote disconnect request.</span></span> <span data-ttu-id="3a23d-169">È disponibile nella struttura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) della chiamata quando la chiamata è nello stato disconnected.</span><span class="sxs-lookup"><span data-stu-id="3a23d-169">It is available in the call's [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure when the call is in the disconnected state.</span></span> <span data-ttu-id="3a23d-170">Mentre una chiamata si trova in questo stato, l'applicazione può comunque eseguire query sulle informazioni e sullo stato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="3a23d-170">While a call is in this state, the application is still allowed to query the call's information and status.</span></span> <span data-ttu-id="3a23d-171">Ad esempio, le informazioni utente utente ricevute come parte della disconnessione remota sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="3a23d-171">For example, user-user information that is received as part of the remote disconnect is available then.</span></span> <span data-ttu-id="3a23d-172">L'applicazione può cancellare una chiamata disconnessa eliminando la chiamata.</span><span class="sxs-lookup"><span data-stu-id="3a23d-172">The application can clear a disconnected call by dropping the call.</span></span>

<span data-ttu-id="3a23d-173">Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare questo \_ valore LINEDISCONNECTMODE se non è supportato nella versione negoziata (in alternativa, è possibile usare LINEDISCONNECTMODE \_ Normal o \_ Unknown).</span><span class="sxs-lookup"><span data-stu-id="3a23d-173">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEDISCONNECTMODE\_ value if it is not supported on the negotiated version (LINEDISCONNECTMODE\_NORMAL or \_UNKNOWN could be used instead).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a23d-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a23d-174">Requirements</span></span>



| <span data-ttu-id="3a23d-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a23d-175">Requirement</span></span> | <span data-ttu-id="3a23d-176">Valore</span><span class="sxs-lookup"><span data-stu-id="3a23d-176">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3a23d-177">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="3a23d-177">TAPI version</span></span><br/> | <span data-ttu-id="3a23d-178">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3a23d-178">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3a23d-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a23d-179">Header</span></span><br/>       | <dl> <span data-ttu-id="3a23d-180"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a23d-180"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a23d-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a23d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a23d-182">**LINEA \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="3a23d-182">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="3a23d-183">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="3a23d-183">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="3a23d-184">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="3a23d-184">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




