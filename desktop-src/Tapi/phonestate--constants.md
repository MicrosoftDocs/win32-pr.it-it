---
description: Le \_ costanti del flag di bit PHONESTATE descrivono vari elementi di stato per un dispositivo telefonico.
ms.assetid: 5db53dd4-606a-40b9-9159-b67a0ea1e400
title: Costanti PHONESTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6346251f6947aebb2a5941389843e2abcec77c4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326145"
---
# <a name="phonestate_-constants"></a><span data-ttu-id="f598a-103">\_Costanti PHONESTATE</span><span class="sxs-lookup"><span data-stu-id="f598a-103">PHONESTATE\_ Constants</span></span>

<span data-ttu-id="f598a-104">Le costanti del flag di bit **PHONESTATE \_** descrivono vari elementi di stato per un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="f598a-104">The **PHONESTATE\_** bit-flag constants describe various status items for a phone device.</span></span>

<dl> <dt>

<span data-ttu-id="f598a-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**\_CAPSCHANGE PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-105"><span id="PHONESTATE_CAPSCHANGE"></span><span id="phonestate_capschange"></span>**PHONESTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-106">Indica che, a causa delle modifiche di configurazione apportate dall'utente o altre circostanze, uno o più membri della struttura [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="f598a-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) structure have changed.</span></span> <span data-ttu-id="f598a-107">Per leggere la struttura aggiornata, l'applicazione deve usare [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="f598a-107">The application should use [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) to read the updated structure.</span></span> <span data-ttu-id="f598a-108">Se un provider di servizi invia un messaggio di [**\_ stato telefonico**](phone-state.md) che contiene questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che trattano una versione precedente dell'API riceveranno \_ messaggi di stato del telefono che specificano PHONESTATE \_ reinit, che richiedono l'arresto e la reinizializzazione della connessione a TAPI per ottenere le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="f598a-108">If a service provider sends a [**PHONE\_STATE**](phone-state.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive PHONE\_STATE messages specifying PHONESTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="f598a-109"><span id="PHONESTATE_CONNECTED"></span><span id="phonestate_connected"></span>**PHONESTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-110">La connessione tra il dispositivo telefonico e TAPI è stata appena creata.</span><span class="sxs-lookup"><span data-stu-id="f598a-110">The connection between the phone device and TAPI was just made.</span></span> <span data-ttu-id="f598a-111">Questo errore si verifica quando viene richiamato TAPI o quando il cavo di connessione del telefono al PC viene collegato con TAPI Active.</span><span class="sxs-lookup"><span data-stu-id="f598a-111">This happens when TAPI is first invoked or when the wire connecting the phone to the PC is plugged in with TAPI active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**\_DEVSPECIFIC PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-112"><span id="PHONESTATE_DEVSPECIFIC"></span><span id="phonestate_devspecific"></span>**PHONESTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-113">Le informazioni specifiche del dispositivo del telefono sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="f598a-113">The phone's device-specific information has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="f598a-114"><span id="PHONESTATE_DISCONNECTED"></span><span id="phonestate_disconnected"></span>**PHONESTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-115">La connessione tra il dispositivo telefonico e TAPI è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="f598a-115">The connection between the phone device and TAPI was just broken.</span></span> <span data-ttu-id="f598a-116">Questo problema si verifica quando il cavo collegato al PC viene scollegato quando il dispositivo è attivo.</span><span class="sxs-lookup"><span data-stu-id="f598a-116">This happens when the wire connecting the phone set to the PC is unplugged while TAPI is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**\_visualizzazione PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-117"><span id="PHONESTATE_DISPLAY"></span><span id="phonestate_display"></span>**PHONESTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-118">La visualizzazione del telefono è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f598a-118">The display of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**\_HANDSETGAIN PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-119"><span id="PHONESTATE_HANDSETGAIN"></span><span id="phonestate_handsetgain"></span>**PHONESTATE\_HANDSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-120">L'impostazione del guadagno del microfono del telefono è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f598a-120">The handset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**\_HANDSETHOOKSWITCH PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-121"><span id="PHONESTATE_HANDSETHOOKSWITCH"></span><span id="phonestate_handsethookswitch"></span>**PHONESTATE\_HANDSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-122">Lo stato del hookswitch del portatile è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f598a-122">The handset hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**\_HANDSETVOLUME PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-123"><span id="PHONESTATE_HANDSETVOLUME"></span><span id="phonestate_handsetvolume"></span>**PHONESTATE\_HANDSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-124">L'impostazione del volume altoparlante del ricevitore è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f598a-124">The handset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**\_HEADSETHOOKSWITCH PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-125"><span id="PHONESTATE_HEADSETHOOKSWITCH"></span><span id="phonestate_headsethookswitch"></span>**PHONESTATE\_HEADSETHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-126">Lo stato hookswitch dell'auricolare è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f598a-126">The headset's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**\_HEADSETGAIN PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-127"><span id="PHONESTATE_HEADSETGAIN"></span><span id="phonestate_headsetgain"></span>**PHONESTATE\_HEADSETGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-128">L'impostazione del guadagno del microfono dell'auricolare è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f598a-128">The headset's microphone gain setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**\_HEADSETVOLUME PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-129"><span id="PHONESTATE_HEADSETVOLUME"></span><span id="phonestate_headsetvolume"></span>**PHONESTATE\_HEADSETVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-130">L'impostazione del volume speaker dell'auricolare è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f598a-130">The headset's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**\_lampada PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-131"><span id="PHONESTATE_LAMP"></span><span id="phonestate_lamp"></span>**PHONESTATE\_LAMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-132">Una lampada del telefono è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f598a-132">A lamp of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**\_monitoraggi PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-133"><span id="PHONESTATE_MONITORS"></span><span id="phonestate_monitors"></span>**PHONESTATE\_MONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-134">Numero di monitoraggi per il dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="f598a-134">The number of monitors for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE \_ altro**</span><span class="sxs-lookup"><span data-stu-id="f598a-135"><span id="PHONESTATE_OTHER"></span><span id="phonestate_other"></span>**PHONESTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-136">Gli elementi di stato del telefono diversi da quelli elencati di seguito sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="f598a-136">Phone-status items other than those listed below have changed.</span></span> <span data-ttu-id="f598a-137">L'applicazione deve controllare lo stato corrente del telefono per determinare quali elementi sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="f598a-137">The application should check the current phone status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**\_proprietario PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-138"><span id="PHONESTATE_OWNER"></span><span id="phonestate_owner"></span>**PHONESTATE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-139">Numero di proprietari del dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="f598a-139">The number of owners for the phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="f598a-140"><span id="PHONESTATE_REINIT"></span><span id="phonestate_reinit"></span>**PHONESTATE\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-141">Gli elementi sono stati modificati nella configurazione dei dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="f598a-141">Items have changed in the configuration of phone devices.</span></span> <span data-ttu-id="f598a-142">Per acquisire familiarità con queste modifiche, come per l'aspetto dei nuovi dispositivi telefonici, l'applicazione deve reinizializzare l'uso di TAPI.</span><span class="sxs-lookup"><span data-stu-id="f598a-142">To become aware of these changes (as for the appearance of new phone devices), the application should reinitialize its use of TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="f598a-143"><span id="PHONESTATE_REMOVED"></span><span id="phonestate_removed"></span>**PHONESTATE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-144">Indica che il dispositivo è stato rimosso dal sistema dal provider di servizi (più probabile tramite l'azione dell'utente, tramite un pannello di controllo o un'utilità simile).</span><span class="sxs-lookup"><span data-stu-id="f598a-144">Indicates that the device is being removed from the system by the service provider (most likely through user action, through a control panel or similar utility).</span></span> <span data-ttu-id="f598a-145">Un messaggio di [**\_ stato telefonico**](phone-state.md) con questo valore sarà in genere seguito immediatamente da un messaggio di [**\_ chiusura del telefono**](phone-close.md) sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f598a-145">A [**PHONE\_STATE**](phone-state.md) message with this value will normally be immediately followed by a [**PHONE\_CLOSE**](phone-close.md) message on the device.</span></span> <span data-ttu-id="f598a-146">I tentativi successivi di accesso al dispositivo prima della reinizializzazione di TAPI comporteranno \_ la restituzione di PHONEERR NODEVICE all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f598a-146">Subsequent attempts to access the device prior to TAPI being reinitialized will result in PHONEERR\_NODEVICE being returned to the application.</span></span> <span data-ttu-id="f598a-147">Se un provider di servizi invia un \_ messaggio di stato telefonico che contiene questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.</span><span class="sxs-lookup"><span data-stu-id="f598a-147">If a service provider sends a PHONE\_STATE message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will not receive any notification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**Riprendi PHONESTATE \_**</span><span class="sxs-lookup"><span data-stu-id="f598a-148"><span id="PHONESTATE_RESUME"></span><span id="phonestate_resume"></span>**PHONESTATE\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-149">L'uso dell'applicazione del dispositivo telefonico viene ripreso dopo essere stato sospeso per un certo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="f598a-149">The application's use of the phone device is resumed after having been suspended for some time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**\_RINGMODE PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-150"><span id="PHONESTATE_RINGMODE"></span><span id="phonestate_ringmode"></span>**PHONESTATE\_RINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-151">La modalità suoneria del telefono è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f598a-151">The ring mode of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**\_RINGVOLUME PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-152"><span id="PHONESTATE_RINGVOLUME"></span><span id="phonestate_ringvolume"></span>**PHONESTATE\_RINGVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-153">Il volume dell'anello del telefono è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f598a-153">The ring volume of the phone has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**\_SPEAKERHOOKSWITCH PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-154"><span id="PHONESTATE_SPEAKERHOOKSWITCH"></span><span id="phonestate_speakerhookswitch"></span>**PHONESTATE\_SPEAKERHOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-155">Lo stato hookswitch del dispositivo vivavoce è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f598a-155">The speakerphone's hookswitch state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**\_SPEAKERGAIN PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-156"><span id="PHONESTATE_SPEAKERGAIN"></span><span id="phonestate_speakergain"></span>**PHONESTATE\_SPEAKERGAIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-157">Lo stato dell'impostazione di miglioramento del microfono del dispositivo vivavoce è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f598a-157">The speakerphone's microphone gain setting state has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**\_SPEAKERVOLUME PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-158"><span id="PHONESTATE_SPEAKERVOLUME"></span><span id="phonestate_speakervolume"></span>**PHONESTATE\_SPEAKERVOLUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-159">L'impostazione del volume speaker del dispositivo vivavoce è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f598a-159">The speakerphone's speaker volume setting has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f598a-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**\_sospensione PHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f598a-160"><span id="PHONESTATE_SUSPEND"></span><span id="phonestate_suspend"></span>**PHONESTATE\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f598a-161">L'uso del telefono da parte dell'applicazione è temporaneamente sospeso.</span><span class="sxs-lookup"><span data-stu-id="f598a-161">The application's use of the phone is temporarily suspended.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f598a-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="f598a-162">Remarks</span></span>

<span data-ttu-id="f598a-163">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="f598a-163">No extensibility.</span></span> <span data-ttu-id="f598a-164">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="f598a-164">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="f598a-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f598a-165">Requirements</span></span>



| <span data-ttu-id="f598a-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="f598a-166">Requirement</span></span> | <span data-ttu-id="f598a-167">Valore</span><span class="sxs-lookup"><span data-stu-id="f598a-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f598a-168">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f598a-168">TAPI version</span></span><br/> | <span data-ttu-id="f598a-169">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f598a-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f598a-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f598a-170">Header</span></span><br/>       | <dl> <span data-ttu-id="f598a-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f598a-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f598a-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f598a-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f598a-173">**\_chiusura telefono**</span><span class="sxs-lookup"><span data-stu-id="f598a-173">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="f598a-174">**\_stato telefono**</span><span class="sxs-lookup"><span data-stu-id="f598a-174">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="f598a-175">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="f598a-175">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="f598a-176">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="f598a-176">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




