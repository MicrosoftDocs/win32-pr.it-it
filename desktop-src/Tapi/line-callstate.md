---
description: Il messaggio della linea TAPI \_ CALLSTATE viene inviato quando lo stato della chiamata specificata viene modificato.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Messaggio di LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327500"
---
# <a name="line_callstate-message"></a><span data-ttu-id="40925-103">\_Messaggio linea CALLSTATE</span><span class="sxs-lookup"><span data-stu-id="40925-103">LINE\_CALLSTATE message</span></span>

<span data-ttu-id="40925-104">Il messaggio della **linea TAPI \_ CALLSTATE** viene inviato quando lo stato della chiamata specificata viene modificato.</span><span class="sxs-lookup"><span data-stu-id="40925-104">The TAPI **LINE\_CALLSTATE** message is sent when the status of the specified call has changed.</span></span> <span data-ttu-id="40925-105">In genere, molti di questi messaggi vengono ricevuti durante la durata di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-105">Typically, several such messages are received during the lifetime of a call.</span></span> <span data-ttu-id="40925-106">Le applicazioni ricevono notifiche relative a nuove chiamate in ingresso con questo messaggio. la nuova chiamata è nello stato dell' *offerta* .</span><span class="sxs-lookup"><span data-stu-id="40925-106">Applications are notified of new incoming calls with this message; the new call is in the *offering* state.</span></span> <span data-ttu-id="40925-107">L'applicazione può utilizzare [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) per recuperare informazioni più dettagliate sullo stato corrente della chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-107">The application can use [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) to retrieve more detailed information about the current status of the call.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="40925-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="40925-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40925-109">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="40925-109">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="40925-110">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-110">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="40925-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="40925-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="40925-112">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-112">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="40925-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="40925-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="40925-114">Nuovo stato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-114">The new call state.</span></span> <span data-ttu-id="40925-115">Questo parametro deve essere una sola delle seguenti [**\_ costanti LINECALLSTATE**](linecallstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40925-115">This parameter must be one and only one of the following [**LINECALLSTATE\_ constants**](linecallstate--constants.md).</span></span>



| <span data-ttu-id="40925-116">dwParam1</span><span class="sxs-lookup"><span data-stu-id="40925-116">dwParam1</span></span>                                                                                                                                                                                             | <span data-ttu-id="40925-117">Significato</span><span class="sxs-lookup"><span data-stu-id="40925-117">Meaning</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <span data-ttu-id="40925-118"><dt>**LINECALLSTATE \_ occupato**</dt></span><span class="sxs-lookup"><span data-stu-id="40925-118"><dt>**LINECALLSTATE\_BUSY**</dt></span></span> </dl>                         | <span data-ttu-id="40925-119">*dwParam2* contiene informazioni dettagliate sulla modalità di occupato.</span><span class="sxs-lookup"><span data-stu-id="40925-119">*dwParam2* contains details about the busy mode.</span></span> <span data-ttu-id="40925-120">Questo parametro usa una delle [**\_ costanti LINEBUSYMODE**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40925-120">This parameter uses one of the [**LINEBUSYMODE\_ constants**](linebusymode--constants.md).</span></span><br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <span data-ttu-id="40925-121"><dt>**LINECALLSTATE \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="40925-121"><dt>**LINECALLSTATE\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="40925-122">*dwParam2* contiene informazioni dettagliate sulla modalità connessa.</span><span class="sxs-lookup"><span data-stu-id="40925-122">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="40925-123">Questo parametro usa una delle [**\_ costanti LINECONNECTEDMODE**](lineconnectedmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40925-123">This parameter uses one of the [**LINECONNECTEDMODE\_ constants**](lineconnectedmode--constants.md).</span></span><br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <span data-ttu-id="40925-124"><dt>**LINECALLSTATE \_ DIaltone**</dt></span><span class="sxs-lookup"><span data-stu-id="40925-124"><dt>**LINECALLSTATE\_DIALTONE**</dt></span></span> </dl>             | <span data-ttu-id="40925-125">*dwParam2* contiene informazioni dettagliate sulla modalità di composizione del segnale.</span><span class="sxs-lookup"><span data-stu-id="40925-125">*dwParam2* contains details about the dial tone mode.</span></span> <span data-ttu-id="40925-126">Questo parametro usa una delle [**\_ costanti LINEDIALTONEMODE**](linedialtonemode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40925-126">This parameter uses one of the [**LINEDIALTONEMODE\_ constants**](linedialtonemode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <span data-ttu-id="40925-127"><dt>**\_offerta LINECALLSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="40925-127"><dt>**LINECALLSTATE\_OFFERING**</dt></span></span> </dl>             | <span data-ttu-id="40925-128">*dwParam2* contiene informazioni dettagliate sulla modalità connessa.</span><span class="sxs-lookup"><span data-stu-id="40925-128">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="40925-129">Questo parametro usa una delle [**\_ costanti LINEOFFERINGMODE**](lineofferingmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40925-129">This parameter uses one of the [**LINEOFFERINGMODE\_ constants**](lineofferingmode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <span data-ttu-id="40925-130"><dt>**\_SPECIALINFO LINECALLSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="40925-130"><dt>**LINECALLSTATE\_SPECIALINFO**</dt></span></span> </dl>    | <span data-ttu-id="40925-131">*dwParam2* contiene i dettagli sulla modalità di informazione speciale.</span><span class="sxs-lookup"><span data-stu-id="40925-131">*dwParam2* contains the details about the special information mode.</span></span> <span data-ttu-id="40925-132">Questo parametro usa una delle [**\_ costanti LINESPECIALINFO**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40925-132">This parameter uses one of the [**LINESPECIALINFO\_ constants**](linespecialinfo--constants.md).</span></span><br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <span data-ttu-id="40925-133"><dt>**LINECALLSTATE \_ disconnesso**</dt></span><span class="sxs-lookup"><span data-stu-id="40925-133"><dt>**LINECALLSTATE\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="40925-134">*dwParam2* contiene informazioni dettagliate sulla modalità di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="40925-134">*dwParam2* contains details about the disconnect mode.</span></span> <span data-ttu-id="40925-135">Questo parametro usa una delle [**\_ costanti LINEDISCONNECTMODE**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40925-135">This parameter uses one of the [**LINEDISCONNECTMODE\_ constants**](linedisconnectmode--constants.md).</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="40925-136">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="40925-136">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="40925-137">Informazioni dipendenti dallo stato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-137">Call-state-dependent information.</span></span> <span data-ttu-id="40925-138">Vedere *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="40925-138">See *dwParam1*.</span></span>

> [!Note]  
> <span data-ttu-id="40925-139">Nei casi in cui è appropriata una risposta *ritardata* , usare LINEDISCONNECTMODE \_ TEMPFAILURE.</span><span class="sxs-lookup"><span data-stu-id="40925-139">In circumstances where a *delayed* response is appropriate, use LINEDISCONNECTMODE\_TEMPFAILURE.</span></span> <span data-ttu-id="40925-140">Quando una risposta *Blocklisting* è appropriata, usare LINEDISCONNECT \_ bloccato.</span><span class="sxs-lookup"><span data-stu-id="40925-140">Where a *blocklisted* response is appropriate, use LINEDISCONNECT\_BLOCKED.</span></span> <span data-ttu-id="40925-141">Per ulteriori informazioni, vedere [**\_ costanti LINEDISCONNECTMODE**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40925-141">For further information, see [**LINEDISCONNECTMODE\_ Constants**](linedisconnectmode--constants.md).</span></span>

 

<span data-ttu-id="40925-142">Se *dwParam1* è LINECALLSTATE \_ conferenced, *DwParam2* contiene il parametro *hConfCall* della chiamata padre della conferenza di cui l'oggetto *hCall* è membro.</span><span class="sxs-lookup"><span data-stu-id="40925-142">If *dwParam1* is LINECALLSTATE\_CONFERENCED, *dwParam2* contains the *hConfCall* parameter of the parent call of the conference of which the subject *hCall* is a member.</span></span> <span data-ttu-id="40925-143">Se la chiamata specificata in *dwParam2* non è stata precedentemente considerata come chiamata di conferenza padre da parte dell'applicazione (*hConfCall*, l'applicazione deve eseguire questa operazione in seguito a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="40925-143">If the call specified in *dwParam2* was not previously considered by the application to be a parent conference call (*hConfCall*, the application must do so as a result of this message.</span></span> <span data-ttu-id="40925-144">Se l'applicazione non dispone di un handle per la chiamata padre della conferenza (perché in precedenza è stato chiamato [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) su tale handle) *dwParam2* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="40925-144">If the application does not have a handle to the parent call of the conference (because it has previously called [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) on that handle) *dwParam2* is set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="40925-145">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="40925-145">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="40925-146">Se è zero, questo parametro indica che non sono state apportate modifiche al privilegio dell'applicazione per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-146">If zero, this parameter indicates that there has been no change in the application's privilege for the call.</span></span>

<span data-ttu-id="40925-147">Se diverso da zero, specifica il privilegio dell'applicazione per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-147">If nonzero, it specifies the application's privilege for the call.</span></span> <span data-ttu-id="40925-148">Questo problema si verifica nelle situazioni seguenti: (1) la prima volta che all'applicazione viene assegnato un handle per la chiamata; (2) quando l'applicazione è la destinazione di una chiamata uniforme (anche se l'applicazione è già un proprietario della chiamata).</span><span class="sxs-lookup"><span data-stu-id="40925-148">This occurs in the following situations: (1) The first time that the application is given a handle to this call; (2) When the application is the target of a call handoff (even if the application already was an owner of the call).</span></span> <span data-ttu-id="40925-149">Questo parametro usa una delle [**\_ costanti LINECALLPRIVILEGE**](linecallprivilege--constants.md)seguenti.</span><span class="sxs-lookup"><span data-stu-id="40925-149">This parameter uses one of the following [**LINECALLPRIVILEGE\_ constants**](linecallprivilege--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40925-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40925-150">Return value</span></span>

<span data-ttu-id="40925-151">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="40925-151">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40925-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="40925-152">Remarks</span></span>

<span data-ttu-id="40925-153">Questo messaggio viene inviato a qualsiasi applicazione che dispone di un handle per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="40925-153">This message is sent to any application that has a handle for the call.</span></span> <span data-ttu-id="40925-154">Il messaggio di **riga \_ CALLSTATE** notifica anche alle applicazioni che monitorano le chiamate su una riga sull'esistenza e sullo stato delle chiamate in uscita stabilite da altre applicazioni o manualmente dall'utente (ad esempio, in un dispositivo telefonico collegato).</span><span class="sxs-lookup"><span data-stu-id="40925-154">The **LINE\_CALLSTATE** message also notifies applications that monitor calls on a line about the existence and state of outbound calls established by other applications or manually by the user (for example, on an attached phone device).</span></span> <span data-ttu-id="40925-155">Lo stato di chiamata di tali chiamate riflette lo stato effettivo della chiamata, che non *offre*.</span><span class="sxs-lookup"><span data-stu-id="40925-155">The call state of such calls reflects the actual state of the call, which is not *offering*.</span></span> <span data-ttu-id="40925-156">Esaminando lo stato della chiamata, l'applicazione è in grado di determinare se la chiamata è una chiamata in ingresso a cui è necessario rispondere o meno.</span><span class="sxs-lookup"><span data-stu-id="40925-156">By examining the call state, the application can determine whether the call is an inbound call that needs to be answered or not.</span></span>

<span data-ttu-id="40925-157">Un **messaggio \_ CALLSTATE di riga** con uno stato di chiamata sconosciuto può essere inviato a un'applicazione di monitoraggio come risultato di un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), lineUnpark [**, lineSetupTransfer, linePickup**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer) [**,**](/windows/desktop/api/Tapi/nf-tapi-linepickup) [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)o [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) completato che è stato richiesto da un'altra applicazione. [](/windows/desktop/api/Tapi/nf-tapi-lineunpark)</span><span class="sxs-lookup"><span data-stu-id="40925-157">A **LINE\_CALLSTATE** message with an unknown call state can be sent to a monitoring application as the result of a successful [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference), or [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) that has been requested by another application.</span></span> <span data-ttu-id="40925-158">Nel momento in cui l'applicazione richiedente riceve una risposta di [**riga \_**](line-reply.md) (operazione riuscita) per l'operazione richiesta, tutte le applicazioni di monitoraggio sulla riga riceveranno il messaggio di **riga \_ CALLSTATE** (sconosciuto).</span><span class="sxs-lookup"><span data-stu-id="40925-158">At the same time that the requesting application is sent a [**LINE\_REPLY**](line-reply.md) (success) for the requested operation, any monitoring applications on the line are sent the **LINE\_CALLSTATE** (unknown) message.</span></span> <span data-ttu-id="40925-159">Un messaggio di **riga \_ CALLSTATE** che indica lo stato di chiamata "reale" della chiamata appena generata viene inviato (usando le informazioni fornite dal provider di servizi) per le applicazioni che eseguono la richiesta e il monitoraggio subito dopo.</span><span class="sxs-lookup"><span data-stu-id="40925-159">A **LINE\_CALLSTATE** message indicating the "real" call state of the newly generated call is sent (using information provided by the service provider) to the requesting and monitoring applications shortly thereafter.</span></span>

<span data-ttu-id="40925-160">Un messaggio di **riga \_ CALLSTATE** (sconosciuto) viene inviato al monitoraggio delle applicazioni solo se [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causa la risoluzione delle chiamate in una conferenza a tre vie.</span><span class="sxs-lookup"><span data-stu-id="40925-160">A **LINE\_CALLSTATE** (unknown) message is sent to monitoring applications only if [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causes calls to be resolved into a three-way conference.</span></span>

<span data-ttu-id="40925-161">Per compatibilità con le versioni precedenti, le applicazioni meno recenti non sono in attesa di un valore specifico in *dwParam2* di un \_ messaggio di conferenza LINECALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="40925-161">For backward compatibility, older applications are not expecting any particular value in *dwParam2* of a LINECALLSTATE\_CONFERENCED message.</span></span> <span data-ttu-id="40925-162">TAPI passa quindi la chiamata padre *hConfCall* in *dwParam2* indipendentemente dalla versione API dell'applicazione che riceve il messaggio.</span><span class="sxs-lookup"><span data-stu-id="40925-162">TAPI therefore passes the parent call *hConfCall* in *dwParam2* regardless of the API version of the application receiving the message.</span></span> <span data-ttu-id="40925-163">Nel caso di una chiamata di conferenza iniziata dal provider di servizi, l'applicazione precedente non è consapevole che la chiamata padre è diventata una chiamata di conferenza a meno che non si verifichino spontaneamente altre informazioni (ad esempio, chiamare [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span><span class="sxs-lookup"><span data-stu-id="40925-163">In the case of a conference call initiated by the service provider, the older application is not aware that the parent call has become a conference call unless it happens to spontaneously examine other information (for example, call [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span></span>

<span data-ttu-id="40925-164">Questo messaggio non può essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="40925-164">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="40925-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40925-165">Requirements</span></span>



| <span data-ttu-id="40925-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="40925-166">Requirement</span></span> | <span data-ttu-id="40925-167">Valore</span><span class="sxs-lookup"><span data-stu-id="40925-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="40925-168">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="40925-168">TAPI version</span></span><br/> | <span data-ttu-id="40925-169">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="40925-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="40925-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40925-170">Header</span></span><br/>       | <dl> <span data-ttu-id="40925-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="40925-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40925-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40925-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40925-173">**\_risposta riga**</span><span class="sxs-lookup"><span data-stu-id="40925-173">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="40925-174">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="40925-174">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="40925-175">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="40925-175">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="40925-176">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="40925-176">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[<span data-ttu-id="40925-177">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="40925-177">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="40925-178">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="40925-178">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="40925-179">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="40925-179">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[<span data-ttu-id="40925-180">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="40925-180">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="40925-181">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="40925-181">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="40925-182">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="40925-182">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[<span data-ttu-id="40925-183">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="40925-183">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="40925-184">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="40925-184">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[<span data-ttu-id="40925-185">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="40925-185">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




