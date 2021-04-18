---
description: Questo è l'elenco dei codici di errore che l'implementazione può restituire quando si richiamano le operazioni sui dispositivi telefonici. Consultare le descrizioni delle singole funzioni per determinare quali di questi codici di errore possono essere restituiti da ogni funzione.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: Costanti PHONEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333951"
---
# <a name="phoneerr_-constants"></a><span data-ttu-id="6949e-104">\_Costanti PHONEERR</span><span class="sxs-lookup"><span data-stu-id="6949e-104">PHONEERR\_ Constants</span></span>

<span data-ttu-id="6949e-105">Questo è l'elenco dei codici di errore che l'implementazione può restituire quando si richiamano le operazioni sui dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="6949e-105">This is the list of error codes that the implementation can return when invoking operations on phone devices.</span></span> <span data-ttu-id="6949e-106">Consultare le descrizioni delle singole funzioni per determinare quali di questi codici di errore possono essere restituiti da ogni funzione.</span><span class="sxs-lookup"><span data-stu-id="6949e-106">Consult the individual function descriptions to determine which of these error codes each function can return.</span></span>

<dl> <dt>

<span data-ttu-id="6949e-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ allocato**</span><span class="sxs-lookup"><span data-stu-id="6949e-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-108">La risorsa specificata è già allocata.</span><span class="sxs-lookup"><span data-stu-id="6949e-108">The specified resource is already allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**\_BADDEVICEID PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-110">L'identificatore di dispositivo specificato non è valido o non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="6949e-110">The specified device identifier is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="6949e-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-112">La chiamata è stata disconnessa.</span><span class="sxs-lookup"><span data-stu-id="6949e-112">The call was disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**\_INCOMPATIBLEAPIVERSION PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-114">L'applicazione ha richiesto una versione o un intervallo di versioni dell'API che non può essere supportato dall'implementazione dell'API di telefonia o dal provider di servizi corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6949e-114">The application requested an API version or version range that cannot be supported by the Telephony API implementation or the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**\_INCOMPATIBLEEXTVERSION PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-116">L'applicazione ha richiesto una versione dell'estensione o un intervallo di versioni che non può essere supportato dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="6949e-116">The application requested an extension version or version range that cannot be supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**\_INIFILECORRUPT PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-118">A causa di incoerenze interne o problemi di formattazione nel file di Telephon.ini, non può essere letto e compreso correttamente da TAPI.</span><span class="sxs-lookup"><span data-stu-id="6949e-118">Because of internal inconsistencies or formatting problems in the Telephon.ini file, it cannot be read and understood properly by TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**\_InUse PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-120">Il dispositivo è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="6949e-120">The device is currently in use.</span></span> <span data-ttu-id="6949e-121">Non è possibile configurare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6949e-121">The device cannot be configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**\_INVALAPPHANDLE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-123">Il punto di controllo di utilizzo o l'handle di registrazione specificato dall'applicazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-123">The application's specified usage handle or registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**\_INVALAPPNAME PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-125">Il nome dell'applicazione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-125">The specified application name is invalid.</span></span> <span data-ttu-id="6949e-126">Se l'applicazione specifica un nome di applicazione, si presuppone che la stringa non contenga caratteri non visualizzabili e con terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="6949e-126">If an application name is specified by the application, it is assumed that the string does not contain any nondisplayable characters and is **NULL**-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**\_INVALBUTTONLAMPID PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR\_INVALBUTTONLAMPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-128">L'identificatore del pulsante o della lampada specificato non è compreso nell'intervallo o non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-128">The specified button/lamp identifier is out of range or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**\_INVALBUTTONMODE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR\_INVALBUTTONMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-130">Il parametro della modalità pulsante non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-130">The button mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**\_INVALBUTTONSTATE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR\_INVALBUTTONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-132">Il parametro degli Stati dei pulsanti non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-132">The button states parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**\_INVALDATAID PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR\_INVALDATAID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-134">L'identificatore di dati specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-134">The specified data identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**\_INVALDEVICECLASS PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-136">Il telefono specificato non supporta la classe di dispositivi indicata.</span><span class="sxs-lookup"><span data-stu-id="6949e-136">The specified phone does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**\_INVALEXTVERSION PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-138">Il numero di versione dell'estensione del provider di servizi non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-138">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**\_INVALHOOKSWITCHDEV PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR\_INVALHOOKSWITCHDEV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-140">Il parametro del dispositivo hookswitch non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-140">The hookswitch device parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**\_INVALHOOKSWITCHMODE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR\_INVALHOOKSWITCHMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-142">Il parametro della modalità hookswitch non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-142">The hookswitch mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**\_INVALLAMPMODE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR\_INVALLAMPMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-144">Il parametro della modalità lampada specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-144">The specified lamp mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**\_INVALPARAM PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-146">Un parametro, ad esempio un valore di riga o di colonna o un handle di finestra, non è valido o non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="6949e-146">A parameter, such as a row or column value or a window handle, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**\_INVALPHONEHANDLE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR\_INVALPHONEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-148">L'handle di dispositivo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-148">The specified device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**\_INVALPHONESTATE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR\_INVALPHONESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-150">Il dispositivo telefonico non è in uno stato valido per l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="6949e-150">The phone device is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**\_INVALPOINTER PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-152">Uno o più parametri del puntatore specificati non sono validi.</span><span class="sxs-lookup"><span data-stu-id="6949e-152">One or more of the specified pointer parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**\_INVALPRIVILEGE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR\_INVALPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-154">Il parametro *dwPrivilege* non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-154">The *dwPrivilege* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**\_INVALRINGMODE PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR\_INVALRINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-156">Il parametro della modalità anello non è valido.</span><span class="sxs-lookup"><span data-stu-id="6949e-156">The ring mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ NOdevice**</span><span class="sxs-lookup"><span data-stu-id="6949e-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-158">L'identificatore di dispositivo specificato, che in precedenza era valido, non viene più accettato perché il dispositivo associato è stato rimosso dal sistema perché TAPI è stato inizializzato per l'ultima volta o è danneggiato in modo non rilevato durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="6949e-158">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized or is corrupt in a way that was not detected at initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NOdriver**</span><span class="sxs-lookup"><span data-stu-id="6949e-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-160">Il provider del servizio telefonico per il dispositivo specificato ha rilevato che uno dei suoi componenti è mancante o danneggiato in modo che non sia stato rilevato al momento dell'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="6949e-160">The telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="6949e-161">Per risolvere il problema, è consigliabile usare il pannello di controllo telefonia.</span><span class="sxs-lookup"><span data-stu-id="6949e-161">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**nome del PHONEERR \_**</span><span class="sxs-lookup"><span data-stu-id="6949e-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-163">Memoria insufficiente per completare l'operazione richiesta oppure non è possibile allocare o bloccare la memoria.</span><span class="sxs-lookup"><span data-stu-id="6949e-163">Insufficient memory to complete the requested operation, or unable to allocate or lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**\_NOtowner PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-165">L'applicazione non dispone del privilegio proprietario per il dispositivo telefonico specificato.</span><span class="sxs-lookup"><span data-stu-id="6949e-165">The application does not have owner privilege to the specified phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**\_OPERATIONFAILED PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-167">L'operazione non è riuscita per un motivo non specificato.</span><span class="sxs-lookup"><span data-stu-id="6949e-167">The operation failed for an unspecified reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**\_OPERATIONUNAVAIL PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-169">Operazione non disponibile.</span><span class="sxs-lookup"><span data-stu-id="6949e-169">The operation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR \_ REinit**</span><span class="sxs-lookup"><span data-stu-id="6949e-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-171">Se è stata richiesta la reinizializzazione di TAPI, ad esempio in seguito all'aggiunta o alla rimozione di un provider di servizi di telefonia, le richieste [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) o [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) vengono rifiutate con questo errore fino a quando l'ultima applicazione non arresta l'utilizzo dell'API (usando [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), a quel punto la nuova configurazione diventa effettiva e le applicazioni sono nuovamente autorizzate a chiamare **phoneInitialize** o **phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="6949e-171">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) or [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **phoneInitialize** or **phoneInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**\_REQUESTOVERRUN PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-173">È stato superato il numero massimo di richieste telefoniche in attesa.</span><span class="sxs-lookup"><span data-stu-id="6949e-173">The maximum number of outstanding phone requests has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**\_RESOURCEUNAVAIL PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-175">Non è possibile completare l'operazione a causa di un overcommit delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6949e-175">The operation cannot be completed because of resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**\_STRUCTURETOOSMALL PHONEERR**</span><span class="sxs-lookup"><span data-stu-id="6949e-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-177">La struttura dei tappi telefonici specificata è troppo piccola.</span><span class="sxs-lookup"><span data-stu-id="6949e-177">The specified phone caps structure is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6949e-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR non \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="6949e-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6949e-179">L'operazione è stata richiamata prima di qualsiasi applicazione denominata [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="6949e-179">The operation was invoked before any application called [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6949e-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="6949e-180">Remarks</span></span>

<span data-ttu-id="6949e-181">I valori da 0xC0000000 a 0xFFFFFFFF sono disponibili per le estensioni specifiche del dispositivo. i valori 0x80000000 tramite 0xBFFFFFFF sono riservati. e 0x00000000 tramite 0x7FFFFFFF vengono usati come identificatori di richiesta.</span><span class="sxs-lookup"><span data-stu-id="6949e-181">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions; the values 0x80000000 through 0xBFFFFFFF are reserved; and 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="6949e-182">Se un'applicazione restituisce un errore che non gestisce in modo specifico (ad esempio un errore definito da un'estensione specifica del dispositivo), deve considerare l'errore come un \_ OPERATIONFAILED PHONEERR (per un motivo non specificato).</span><span class="sxs-lookup"><span data-stu-id="6949e-182">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a PHONEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

## <a name="requirements"></a><span data-ttu-id="6949e-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6949e-183">Requirements</span></span>



| <span data-ttu-id="6949e-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="6949e-184">Requirement</span></span> | <span data-ttu-id="6949e-185">Valore</span><span class="sxs-lookup"><span data-stu-id="6949e-185">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6949e-186">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="6949e-186">TAPI version</span></span><br/> | <span data-ttu-id="6949e-187">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6949e-187">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6949e-188">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6949e-188">Header</span></span><br/>       | <dl> <span data-ttu-id="6949e-189"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6949e-189"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6949e-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6949e-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6949e-191">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="6949e-191">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="6949e-192">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="6949e-192">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="6949e-193">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="6949e-193">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="6949e-194">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="6949e-194">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




