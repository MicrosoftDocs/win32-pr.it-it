---
description: Le \_ costanti del flag di bit LINEDEVSTATE descrivono vari eventi dello stato della riga.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: Costanti LINEDEVSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333650"
---
# <a name="linedevstate_-constants"></a><span data-ttu-id="3f906-103">\_Costanti LINEDEVSTATE</span><span class="sxs-lookup"><span data-stu-id="3f906-103">LINEDEVSTATE\_ Constants</span></span>

<span data-ttu-id="3f906-104">Le costanti del flag di bit **LINEDEVSTATE \_** descrivono vari eventi dello stato della riga.</span><span class="sxs-lookup"><span data-stu-id="3f906-104">The **LINEDEVSTATE\_** bit-flag constants describe various line status events.</span></span>

<dl> <dt>

<span data-ttu-id="3f906-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_batteria LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-105"><span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**LINEDEVSTATE\_BATTERY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-106">Il livello della batteria è stato modificato in modo significativo (cellulare).</span><span class="sxs-lookup"><span data-stu-id="3f906-106">The battery level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**\_CAPSCHANGE LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-107"><span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-108">Indica che, a causa delle modifiche di configurazione apportate dall'utente o altre circostanze, uno o più membri della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per l'indirizzo sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="3f906-108">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the address have changed.</span></span> <span data-ttu-id="3f906-109">Per leggere la struttura aggiornata, l'applicazione deve usare [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="3f906-109">The application should use [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="3f906-110">Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni che hanno negoziato la versione di TAPI 1,4 o versioni successive. le applicazioni che trattano una versione precedente di TAPI riceveranno i messaggi di **riga \_ LINEDEVSTATE** specificando LINEDEVSTATE \_ reinit, richiedendo di arrestare e reinizializzare la connessione a TAPI per ottenere le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="3f906-110">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**chiusura di LINEDEVSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="3f906-111"><span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-112">La riga è stata chiusa da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f906-112">The line has been closed by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**\_CONFIGCHANGE LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-113"><span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE\_CONFIGCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-114">Indica che sono state apportate modifiche alla configurazione a uno o più dispositivi multimediali associati al dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="3f906-114">Indicates that configuration changes have been made to one or more of the media devices associated with the line device.</span></span> <span data-ttu-id="3f906-115">L'applicazione, se desidera, può utilizzare [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) per leggere le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="3f906-115">The application, if it desires, can use [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) to read the updated information.</span></span> <span data-ttu-id="3f906-116">Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.</span><span class="sxs-lookup"><span data-stu-id="3f906-116">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**\_COMPLCANCEL LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-117"><span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE\_COMPLCANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-118">Indica che il completamento della chiamata identificato dall'identificatore di completamento contenuto nel parametro *dwParam2* del messaggio [**line \_ LINEDEVSTATE**](line-linedevstate.md) è stato annullato esternamente e non è più considerato valido (se tale valore deve essere passato in una chiamata successiva a [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), la funzione avrà esito negativo con LINEERR \_ INVALCOMPLETIONID).</span><span class="sxs-lookup"><span data-stu-id="3f906-118">Indicates that the call completion identified by the completion identifier contained in the *dwParam2* parameter of the [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message has been externally canceled and is no longer considered valid (if that value were to be passed in a subsequent call to [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), the function would fail with LINEERR\_INVALCOMPLETIONID).</span></span> <span data-ttu-id="3f906-119">Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.</span><span class="sxs-lookup"><span data-stu-id="3f906-119">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="3f906-120"><span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-121">La riga è stata precedentemente disconnessa ed è ora connessa a TAPI.</span><span class="sxs-lookup"><span data-stu-id="3f906-121">The line was previously disconnected and is now connected to TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**\_DEVSPECIFIC LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-122"><span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-123">Le informazioni specifiche del dispositivo della riga sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="3f906-123">The line's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="3f906-124"><span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-125">Questa riga è stata connessa in precedenza ed è ora disconnessa da TAPI.</span><span class="sxs-lookup"><span data-stu-id="3f906-125">This line was previously connected and is now disconnected from TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INservice**</span><span class="sxs-lookup"><span data-stu-id="3f906-126"><span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-127">La linea è connessa a TAPI.</span><span class="sxs-lookup"><span data-stu-id="3f906-127">The line is connected to TAPI.</span></span> <span data-ttu-id="3f906-128">Questo errore si verifica quando TAPI viene attivato per la prima volta o quando il cavo di linea è fisicamente collegato al compartmento e in-Service quando TAPI è attivo.</span><span class="sxs-lookup"><span data-stu-id="3f906-128">This happens when TAPI is first activated or when the line wire is physically plugged in and in-service at the switch while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**\_blocco LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-129"><span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**LINEDEVSTATE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-130">Lo stato bloccato del dispositivo a linee è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3f906-130">The locked status of the line device has changed.</span></span> <span data-ttu-id="3f906-131">Per ulteriori informazioni, vedere LINEDEVSTATUSFLAGS \_ BLOCCATO nelle [**\_ costanti LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md).)</span><span class="sxs-lookup"><span data-stu-id="3f906-131">(For more information, see LINEDEVSTATUSFLAGS\_LOCKED in [**LINEDEVSTATUSFLAGS\_ Constants**](linedevstatusflags--constants.md).)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**\_manutenzione LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-132"><span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**LINEDEVSTATE\_MAINTENANCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-133">È in corso l'esecuzione della manutenzione sulla riga del Commuter.</span><span class="sxs-lookup"><span data-stu-id="3f906-133">Maintenance is being performed on the line at the switch.</span></span> <span data-ttu-id="3f906-134">Non è possibile usare TAPI per operare sul dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="3f906-134">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**\_MSGWAITOFF LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-135"><span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE\_MSGWAITOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-136">L'indicatore di attesa dei messaggi è disattivato.</span><span class="sxs-lookup"><span data-stu-id="3f906-136">The message waiting indicator is turned off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**\_MSGWAITON LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-137"><span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE\_MSGWAITON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-138">L'indicatore di attesa dei messaggi è attivato.</span><span class="sxs-lookup"><span data-stu-id="3f906-138">The message waiting indicator is turned on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**\_NUMCALLS LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-139"><span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-140">Il numero di chiamate sul dispositivo a linee è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3f906-140">The number of calls on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**\_NUMCOMPLETIONS LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-141"><span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE\_NUMCOMPLETIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-142">Il numero di completamenti di chiamate in attesa sul dispositivo a linee è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3f906-142">The number of outstanding call completions on the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="3f906-143"><span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-144">La riga è stata aperta da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f906-144">The line has been opened by another application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ altro**</span><span class="sxs-lookup"><span data-stu-id="3f906-145"><span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-146">Gli elementi di stato del dispositivo diversi da quelli elencati di seguito sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="3f906-146">Device-status items other than those listed below have changed.</span></span> <span data-ttu-id="3f906-147">L'applicazione deve controllare lo stato corrente del dispositivo per determinare quali elementi sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="3f906-147">The application should check the current device status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**\_OUTOFSERVICE LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-148"><span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE\_OUTOFSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-149">La riga non è più in servizio al passaggio o fisicamente disconnessa.</span><span class="sxs-lookup"><span data-stu-id="3f906-149">The line is out of service at the switch or physically disconnected.</span></span> <span data-ttu-id="3f906-150">Non è possibile usare TAPI per operare sul dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="3f906-150">TAPI cannot be used to operate on the line device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="3f906-151"><span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-152">Gli elementi sono stati modificati nella configurazione dei dispositivi line.</span><span class="sxs-lookup"><span data-stu-id="3f906-152">Items have changed in the configuration of line devices.</span></span> <span data-ttu-id="3f906-153">Per acquisire familiarità con queste modifiche (per quanto riguarda l'aspetto dei nuovi dispositivi linea), l'applicazione deve reinizializzare l'uso di TAPI.</span><span class="sxs-lookup"><span data-stu-id="3f906-153">To become aware of these changes (as for the appearance of new line devices) the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="3f906-154"><span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-155">Indica che il dispositivo è stato rimosso dal sistema dal provider di servizi (più probabile tramite l'azione dell'utente, tramite un pannello di controllo o un'utilità simile).</span><span class="sxs-lookup"><span data-stu-id="3f906-155">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="3f906-156">Un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) con questo valore sarà in genere seguito immediatamente da un messaggio di [**\_ chiusura riga**](line-close.md) sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3f906-156">A [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message with this value will normally be immediately followed by a [**LINE\_CLOSE**](line-close.md) message on the device.</span></span> <span data-ttu-id="3f906-157">I tentativi successivi di accesso al dispositivo prima della reinizializzazione di TAPI comporteranno \_ la restituzione di LINEERR NODEVICE all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f906-157">Subsequent attempts to access the device prior to TAPI being reinitialized will result in LINEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="3f906-158">Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.</span><span class="sxs-lookup"><span data-stu-id="3f906-158">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**\_suoneria LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-159"><span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE\_RINGING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-160">L'opzione indica alla riga di avvisare l'utente.</span><span class="sxs-lookup"><span data-stu-id="3f906-160">The switch tells the line to alert the user.</span></span>

<span data-ttu-id="3f906-161">**TAPI:** I provider di servizi inviano notifiche alle applicazioni in ogni ciclo circolare inviando ripetutamente messaggi di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenenti questa costante.</span><span class="sxs-lookup"><span data-stu-id="3f906-161">**TAPI:** Service providers notify applications on each ring cycle by repeatedly sending [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages containing this constant.</span></span> <span data-ttu-id="3f906-162">Nel Stati Uniti, ad esempio, i provider di servizi inviano un messaggio con questa costante ogni sei secondi.</span><span class="sxs-lookup"><span data-stu-id="3f906-162">For example, in the United States, service providers send a message with this constant every six seconds.</span></span>

<span data-ttu-id="3f906-163">**TSPI:** In un dispositivo POTS, il provider di servizi può inviare il messaggio ogni volta che l'ufficio centrale Invia la tensione di anello.</span><span class="sxs-lookup"><span data-stu-id="3f906-163">**TSPI:** On a POTS device, the service provider can send the message whenever the central office sends ring voltage.</span></span> <span data-ttu-id="3f906-164">Nei dispositivi digitali, ad esempio ISDN, il provider di servizi potrebbe dover sintetizzare la ripetizione del messaggio se il Commuter genera una sola richiesta ring.</span><span class="sxs-lookup"><span data-stu-id="3f906-164">On digital devices such as ISDN, the service provider may need to synthesize the repetition of the message if the switch generates only one ring request.</span></span> <span data-ttu-id="3f906-165">Ogni ripetizione del messaggio dovrebbe mostrare il numero di squilli in aumento, in modo che le funzioni di salvataggio a pedaggio funzionino correttamente.</span><span class="sxs-lookup"><span data-stu-id="3f906-165">Each repetition of the message should show the ring count increasing, so that toll save functions work properly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**\_ROAMMODE LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-166"><span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE\_ROAMMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-167">La modalità roaming del dispositivo a linee è cambiata.</span><span class="sxs-lookup"><span data-stu-id="3f906-167">The roam mode of the line device has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**\_segnale LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-168"><span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**LINEDEVSTATE\_SIGNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-169">Il livello del segnale è stato modificato significativamente (cellulare).</span><span class="sxs-lookup"><span data-stu-id="3f906-169">The signal level has changed significantly (cellular).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_terminali LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-170"><span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**LINEDEVSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-171">Le impostazioni del terminale sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="3f906-171">The terminal settings have changed.</span></span> <span data-ttu-id="3f906-172">Questo può accadere, ad esempio, se più dispositivi linea condividono terminali tra di essi, ad esempio due righe che condividono un terminale telefonico.</span><span class="sxs-lookup"><span data-stu-id="3f906-172">This can happen, for example, if multiple line devices share terminals among them (for example, two lines sharing a phone terminal).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3f906-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**\_TRANSLATECHANGE LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-173"><span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE\_TRANSLATECHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3f906-174">Indica che, a causa delle modifiche di configurazione apportate dall'utente o altre circostanze, uno o più membri della struttura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="3f906-174">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure have changed.</span></span> <span data-ttu-id="3f906-175">Per leggere la struttura aggiornata, l'applicazione deve usare [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) .</span><span class="sxs-lookup"><span data-stu-id="3f906-175">The application should use [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) to read the updated structure.</span></span> <span data-ttu-id="3f906-176">Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni che hanno negoziato la versione di TAPI 1,4 o versioni successive. le applicazioni che trattano una versione precedente di TAPI riceveranno i messaggi di **riga \_ LINEDEVSTATE** specificando LINEDEVSTATE \_ reinit, richiedendo di arrestare e reinizializzare la connessione a TAPI per ottenere le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="3f906-176">If a service provider sends a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous TAPI version will receive **LINE\_LINEDEVSTATE** messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f906-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f906-177">Remarks</span></span>

<span data-ttu-id="3f906-178">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="3f906-178">No extensibility.</span></span> <span data-ttu-id="3f906-179">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="3f906-179">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f906-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f906-180">Requirements</span></span>



| <span data-ttu-id="3f906-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f906-181">Requirement</span></span> | <span data-ttu-id="3f906-182">Valore</span><span class="sxs-lookup"><span data-stu-id="3f906-182">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3f906-183">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="3f906-183">TAPI version</span></span><br/> | <span data-ttu-id="3f906-184">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3f906-184">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3f906-185">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f906-185">Header</span></span><br/>       | <dl> <span data-ttu-id="3f906-186"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f906-186"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f906-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f906-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f906-188">**\_chiusura riga**</span><span class="sxs-lookup"><span data-stu-id="3f906-188">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="3f906-189">**LINEA \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="3f906-189">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="3f906-190">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="3f906-190">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="3f906-191">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="3f906-191">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="3f906-192">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="3f906-192">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="3f906-193">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="3f906-193">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="3f906-194">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="3f906-194">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="3f906-195">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="3f906-195">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




