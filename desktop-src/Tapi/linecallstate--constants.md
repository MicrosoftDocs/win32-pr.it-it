---
description: Le \_ costanti del flag di bit LINECALLSTATE descrivono gli Stati di chiamata in cui può trovarsi una chiamata.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Costanti LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328906"
---
# <a name="linecallstate_-constants"></a><span data-ttu-id="704ef-103">\_Costanti LINECALLSTATE</span><span class="sxs-lookup"><span data-stu-id="704ef-103">LINECALLSTATE\_ Constants</span></span>

<span data-ttu-id="704ef-104">Le costanti del flag di bit **LINECALLSTATE \_** descrivono gli Stati di chiamata in cui può trovarsi una chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-104">The **LINECALLSTATE\_** bit-flag constants describe the call states a call can be in.</span></span>

<dl> <dt>

<span data-ttu-id="704ef-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ accettata**</span><span class="sxs-lookup"><span data-stu-id="704ef-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-106">La chiamata era nello stato dell'offerta ed è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="704ef-106">The call was in the offering state and has been accepted.</span></span> <span data-ttu-id="704ef-107">Ciò indica ad altre applicazioni (monitoraggio) che l'applicazione corrente del proprietario ha richiesto la responsabilità di rispondere alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-107">This indicates to other (monitoring) applications that the current owner application has claimed responsibility for answering the call.</span></span> <span data-ttu-id="704ef-108">In ISDN lo stato accettato viene immesso quando l'apparecchiatura del gruppo chiamato Invia un messaggio all'opzione che indica che è disposto a presentare la chiamata alla persona chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-108">In ISDN, the accepted state is entered when the called-party equipment sends a message to the switch indicating that it is willing to present the call to the called person.</span></span> <span data-ttu-id="704ef-109">Questo ha l'effetto collaterale degli avvisi (squilli) degli utenti a entrambe le estremità della chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-109">This has the side effect of alerting (ringing) the users at both ends of the call.</span></span> <span data-ttu-id="704ef-110">Una chiamata in ingresso può sempre essere immediatamente soddisfatta senza prima essere accettata separatamente.</span><span class="sxs-lookup"><span data-stu-id="704ef-110">An incoming call can always be immediately answered without first being separately accepted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="704ef-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-112">La chiamata sta ricevendo un tono occupato.</span><span class="sxs-lookup"><span data-stu-id="704ef-112">The call is receiving a busy tone.</span></span> <span data-ttu-id="704ef-113">Un tono occupato indica che non è possibile completare la chiamata, ovvero un circuito (trunk) o la stazione della parte remota è in uso.</span><span class="sxs-lookup"><span data-stu-id="704ef-113">A busy tone indicates that the call cannot be completed either a circuit (trunk) or the remote party's station are in use.</span></span> <span data-ttu-id="704ef-114">Vedere [**\_ costanti LINEBUSYMODE**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="704ef-114">See [**LINEBUSYMODE\_ Constants**](linebusymode--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ conferenced**</span><span class="sxs-lookup"><span data-stu-id="704ef-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE\_CONFERENCED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-116">La chiamata è un membro di una chiamata di conferenza ed è logicamente nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="704ef-116">The call is a member of a conference call and is logically in the connected state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="704ef-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-118">La chiamata è stata stabilita e viene effettuata la connessione.</span><span class="sxs-lookup"><span data-stu-id="704ef-118">The call has been established and the connection is made.</span></span> <span data-ttu-id="704ef-119">Le informazioni sono in grado di attraversare la chiamata tra l'indirizzo di origine e l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="704ef-119">Information is able to flow over the call between the originating address and the destination address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**\_composizione LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="704ef-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE\_DIALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-121">Il creatore sta digitando cifre sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-121">The originator is dialing digits on the call.</span></span> <span data-ttu-id="704ef-122">Le cifre componete vengono raccolte dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="704ef-122">The dialed digits are collected by the switch.</span></span> <span data-ttu-id="704ef-123">Si noti che né [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) né [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) la riga viene posizionata nello stato di composizione.</span><span class="sxs-lookup"><span data-stu-id="704ef-123">Note that neither [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nor [**TSPI\_lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) will place the line into the dialing state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_ DIaltone**</span><span class="sxs-lookup"><span data-stu-id="704ef-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-125">La chiamata riceve un tono di connessione dall'opzione, il che significa che l'opzione è pronta a ricevere un numero composto.</span><span class="sxs-lookup"><span data-stu-id="704ef-125">The call is receiving a dial tone from the switch, which means that the switch is ready to receive a dialed number.</span></span> <span data-ttu-id="704ef-126">Vedere [**\_ costanti LINEDIALTONEMODE**](linedialtonemode--constants.md) per gli identificatori dei toni di composizione speciali, ad esempio un tono di balbuzie della posta vocale normale.</span><span class="sxs-lookup"><span data-stu-id="704ef-126">See [**LINEDIALTONEMODE\_ Constants**](linedialtonemode--constants.md) for identifiers of special dial tones, such as a stutter tone of normal voice mail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="704ef-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-128">La parte remota è stata disconnessa dalla chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-128">The remote party has disconnected from the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ inattivo**</span><span class="sxs-lookup"><span data-stu-id="704ef-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-130">La chiamata esiste ma non è stata connessa.</span><span class="sxs-lookup"><span data-stu-id="704ef-130">The call exists but has not been connected.</span></span> <span data-ttu-id="704ef-131">Non esiste alcuna attività nella chiamata, il che significa che nessuna chiamata è attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="704ef-131">No activity exists on the call, which means that no call is currently active.</span></span> <span data-ttu-id="704ef-132">Una chiamata non può mai eseguire la transizione fuori dallo stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="704ef-132">A call can never transition out of the idle state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**\_offerta LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="704ef-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE\_OFFERING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-134">La chiamata viene offerta alla stazione, segnalando l'arrivo di una nuova chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-134">The call is being offered to the station, signaling the arrival of a new call.</span></span> <span data-ttu-id="704ef-135">Lo stato dell'offerta non è uguale a quello di un telefono o un computer a squillare.</span><span class="sxs-lookup"><span data-stu-id="704ef-135">The offering state is not the same as causing a phone or computer to ring.</span></span> <span data-ttu-id="704ef-136">In alcuni ambienti, una chiamata nello stato dell'offerta non squilla l'utente fino a quando l'opzione non indica alla riga di squillare.</span><span class="sxs-lookup"><span data-stu-id="704ef-136">In some environments, a call in the offering state does not ring the user until the switch instructs the line to ring.</span></span> <span data-ttu-id="704ef-137">Un esempio di utilizzo potrebbe essere la posizione in cui viene visualizzata una chiamata in ingresso su diversi set di stazioni, ma solo gli anelli di indirizzi primari.</span><span class="sxs-lookup"><span data-stu-id="704ef-137">An example use might be where an incoming call appears on several station sets but only the primary address rings.</span></span> <span data-ttu-id="704ef-138">L'istruzione da squillare non influisce su alcuno stato di chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-138">The instruction to ring does not affect any call states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ ONholding**</span><span class="sxs-lookup"><span data-stu-id="704ef-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE\_ONHOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-140">La chiamata è in attesa dall'opzione.</span><span class="sxs-lookup"><span data-stu-id="704ef-140">The call is on hold by the switch.</span></span> <span data-ttu-id="704ef-141">In questo modo viene liberata la riga fisica, che consente a un'altra chiamata di utilizzare la riga.</span><span class="sxs-lookup"><span data-stu-id="704ef-141">This frees the physical line, which allows another call to use the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**\_ONHOLDPENDCONF LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="704ef-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE\_ONHOLDPENDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-143">La chiamata è attualmente in attesa mentre viene aggiunta a una conferenza.</span><span class="sxs-lookup"><span data-stu-id="704ef-143">The call is currently on hold while it is being added to a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**\_ONHOLDPENDTRANSFER LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="704ef-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE\_ONHOLDPENDTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-145">La chiamata è attualmente in attesa di trasferimento a un altro numero.</span><span class="sxs-lookup"><span data-stu-id="704ef-145">The call is currently on hold awaiting transfer to another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**proseguimento di LINECALLSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="704ef-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE\_PROCEEDING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-147">La composizione è stata completata e la chiamata sta procedendo attraverso il Commuter o la rete telefonica.</span><span class="sxs-lookup"><span data-stu-id="704ef-147">Dialing has completed and the call is proceeding through the switch or telephone network.</span></span> <span data-ttu-id="704ef-148">Questo errore si verifica dopo il completamento della connessione e prima che la chiamata raggiunga la parte di composizione, come indicato da riponderone, occupato o risposta.</span><span class="sxs-lookup"><span data-stu-id="704ef-148">This occurs after dialing is complete and before the call reaches the dialed party, as indicated by ringback, busy, or answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE \_ risponder**</span><span class="sxs-lookup"><span data-stu-id="704ef-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-150">È stata raggiunta la stazione da chiamare e l'opzione della destinazione sta generando un tono di chiamata all'origine.</span><span class="sxs-lookup"><span data-stu-id="704ef-150">The station to be called has been reached, and the destination's switch is generating a ring tone back to the originator.</span></span> <span data-ttu-id="704ef-151">Una  richiamata indica che l'indirizzo di destinazione viene avvisato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-151">A *ringback* means that the destination address is being alerted to the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**\_SPECIALINFO LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="704ef-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE\_SPECIALINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-153">La chiamata riceve un segnale di informazione speciale, che precede un annuncio preregistrato che indica il motivo per cui non è possibile completare una chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-153">The call is receiving a special information signal, which precedes a prerecorded announcement indicating why a call cannot be completed.</span></span> <span data-ttu-id="704ef-154">Vedere [**\_ costanti LINESPECIALINFO**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="704ef-154">See [**LINESPECIALINFO\_ Constants**](linespecialinfo--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="704ef-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="704ef-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="704ef-156">La chiamata esiste, ma il suo stato è attualmente sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="704ef-156">The call exists, but its state is currently unknown.</span></span> <span data-ttu-id="704ef-157">Questo potrebbe essere il risultato del rilevamento di stato di chiamata scadente da parte del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="704ef-157">This may be the result of poor call progress detection by the service provider.</span></span> <span data-ttu-id="704ef-158">Un messaggio di stato di chiamata con lo stato della chiamata impostato su Unknown può essere generato anche per informare la DLL TAPI su una nuova chiamata in un momento in cui lo stato di chiamata effettivo della chiamata non è esattamente noto.</span><span class="sxs-lookup"><span data-stu-id="704ef-158">A call state message with the call state set to unknown may also be generated to inform the TAPI DLL about a new call at a time when the actual call state of the call is not exactly known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="704ef-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="704ef-159">Remarks</span></span>

<span data-ttu-id="704ef-160">Gli 8 bit più significativi possono definire uno stato sottostato specifico del dispositivo di uno degli stati predefiniti, a condizione che \_ venga impostato anche uno dei bit LINECALLSTATE definiti sopra.</span><span class="sxs-lookup"><span data-stu-id="704ef-160">The high-order 8 bits can define a device-specific substate of any of the predefined states, provided that one of the LINECALLSTATE\_ bits defined above is also set.</span></span> <span data-ttu-id="704ef-161">I 24 bit di ordine inferiore sono riservati per gli stati predefiniti.</span><span class="sxs-lookup"><span data-stu-id="704ef-161">The low-order 24 bits are reserved for predefined states.</span></span>

<span data-ttu-id="704ef-162">Le **\_ costanti LINECALLSTATE** vengono utilizzate come parametri dal messaggio di [**riga \_ CALLSTATE**](line-callstate.md) inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="704ef-162">The **LINECALLSTATE\_constants** are used as parameters by the [**LINE\_CALLSTATE**](line-callstate.md) message sent to the application.</span></span> <span data-ttu-id="704ef-163">Il messaggio contiene il nuovo stato di chiamata a cui è stata effettuata la transizione della chiamata.</span><span class="sxs-lookup"><span data-stu-id="704ef-163">The message carries the new call state that the call transitioned to.</span></span> <span data-ttu-id="704ef-164">Queste costanti vengono usate anche come membri nella struttura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) restituita dalla funzione [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .</span><span class="sxs-lookup"><span data-stu-id="704ef-164">These constants are also used as members in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure returned by the [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="704ef-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="704ef-165">Requirements</span></span>



| <span data-ttu-id="704ef-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="704ef-166">Requirement</span></span> | <span data-ttu-id="704ef-167">Valore</span><span class="sxs-lookup"><span data-stu-id="704ef-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="704ef-168">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="704ef-168">TAPI version</span></span><br/> | <span data-ttu-id="704ef-169">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="704ef-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="704ef-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="704ef-170">Header</span></span><br/>       | <dl> <span data-ttu-id="704ef-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="704ef-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="704ef-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="704ef-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="704ef-173">**LINEA \_ CALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="704ef-173">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="704ef-174">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="704ef-174">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="704ef-175">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="704ef-175">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="704ef-176">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="704ef-176">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

