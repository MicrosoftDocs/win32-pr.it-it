---
description: Le \_ costanti del flag di bit LINECALLINFOSTATE descrivono varie informazioni sulle chiamate per le quali un'applicazione può ricevere una notifica nel messaggio di riga \_ CALLINFO.
ms.assetid: c216d9b7-8e2f-4604-ba93-1d9e1a5d23fc
title: Costanti LINECALLINFOSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f560cfd6ba65929a9f6cf5c9aa6cd8bc2f48b24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324882"
---
# <a name="linecallinfostate_-constants"></a><span data-ttu-id="f3c66-103">\_Costanti LINECALLINFOSTATE</span><span class="sxs-lookup"><span data-stu-id="f3c66-103">LINECALLINFOSTATE\_ Constants</span></span>

<span data-ttu-id="f3c66-104">Le costanti del flag di bit **LINECALLINFOSTATE \_** descrivono varie informazioni sulle chiamate per le quali un'applicazione può ricevere una notifica nel messaggio di [**riga \_ CALLINFO**](line-callinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c66-104">The **LINECALLINFOSTATE\_** bit-flag constants describe various call information items about which an application can be notified in the [**LINE\_CALLINFO**](line-callinfo.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="f3c66-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**\_APPSPECIFIC LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE\_APPSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-106">Campo specifico dell'applicazione del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-106">The application-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**\_BEARERMODE LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE\_BEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-108">Il campo della modalità di porta del record delle informazioni di chiamata.</span><span class="sxs-lookup"><span data-stu-id="f3c66-108">The bearer mode field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**\_CALLDATA LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE\_CALLDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-110">Il membro **CallData** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) è stato aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f3c66-110">The **CallData** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**\_CALLEDID LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE\_CALLEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-112">Uno dei campi correlati a calledID del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-112">One of the calledID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**\_CALLERID LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE\_CALLERID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-114">Uno dei campi correlati a callerID del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-114">One of the callerID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**\_CALLID LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-116">Campo ID chiamata del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-116">The call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**\_CHARGINGINFO LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE\_CHARGINGINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-118">Informazioni di caricamento del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-118">The charging information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**\_COMPLETIONID LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-120">Campo dell'identificatore di completamento del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-120">The completion identifier field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**\_CONNECTEDID LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE\_CONNECTEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-122">Uno dei campi correlati a connectedID del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-122">One of the connectedID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**\_DEVSPECIFIC LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-124">Campo specifico del dispositivo del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-124">The device-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**\_DIALPARAMS LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE\_DIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-126">Parametri di composizione del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-126">The dial parameters of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**\_visualizzazione LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**LINECALLINFOSTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-128">Campo di visualizzazione del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-128">The display field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**\_HIGHLEVELCOMP LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE\_HIGHLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-130">Campo di compatibilità di alto livello del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-130">The high level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**\_LOWLEVELCOMP LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE\_LOWLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-132">Campo di compatibilità di basso livello del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-132">The low level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**\_MEDIAMODE LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE\_MEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-134">Il campo del tipo di supporto del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-134">The media type field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**\_MONITORMODES LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE\_MONITORMODES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-136">Uno o più campi di monitoraggio cifre, tono o supporti nel record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-136">One or more of the digit, tone, or media monitoring fields in the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**\_NUMMONITORS LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE\_NUMMONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-138">Il campo numero di monitoraggi nel record delle informazioni di chiamata è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f3c66-138">The number of monitors field in the call-information record has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**\_NUMOWNERDECR LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE\_NUMOWNERDECR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-140">Il numero di campi del proprietario nel record delle informazioni di chiamata è stato ridotto.</span><span class="sxs-lookup"><span data-stu-id="f3c66-140">The number of owner field in the call-information record was decreased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**\_NUMOWNERINCR LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE\_NUMOWNERINCR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-142">Il numero di campi del proprietario nel record delle informazioni di chiamata è stato aumentato.</span><span class="sxs-lookup"><span data-stu-id="f3c66-142">The number of owner field in the call-information record was increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**\_origine LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE\_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-144">Il campo Origin del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-144">The origin field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE \_ altro**</span><span class="sxs-lookup"><span data-stu-id="f3c66-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-146">Le informazioni relative alla chiamata a elementi diversi da quelli elencati di seguito sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-146">Call information items other than those listed below have changed.</span></span> <span data-ttu-id="f3c66-147">L'applicazione deve controllare le informazioni correnti sulla chiamata per determinare quali elementi sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="f3c66-147">The application should check the current call information to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**\_QoS LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**LINECALLINFOSTATE\_QOS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-149">Uno o più membri **QoS** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) sono stati aggiornati.</span><span class="sxs-lookup"><span data-stu-id="f3c66-149">One or more of the **QOS** members in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**\_frequenza LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**LINECALLINFOSTATE\_RATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-151">Campo della frequenza del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-151">The rate field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**\_motivo LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**LINECALLINFOSTATE\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-153">Campo motivo del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-153">The reason field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**\_REDIRECTINGID LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE\_REDIRECTINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-155">Identificatore dell'indirizzo del percorso che ha reindirizzato una chiamata.</span><span class="sxs-lookup"><span data-stu-id="f3c66-155">The address identifier of the location that redirected a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**\_REDIRECTIONID LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE\_REDIRECTIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-157">Identificatore dell'indirizzo del percorso a cui è stata reindirizzata una chiamata.</span><span class="sxs-lookup"><span data-stu-id="f3c66-157">The address identifier of the location to which a call has been redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**\_RELATEDCALLID LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE\_RELATEDCALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-159">Campo ID chiamata correlato del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-159">The related call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**\_terminale LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**LINECALLINFOSTATE\_TERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-161">Informazioni sulla modalità terminale del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-161">The terminal mode information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**\_trattamento LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**LINECALLINFOSTATE\_TREATMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-163">Il membro **CallTreatment** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) è stato aggiornato.</span><span class="sxs-lookup"><span data-stu-id="f3c66-163">The **CallTreatment** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span> <span data-ttu-id="f3c66-164">Questo problema può verificarsi in risposta a una funzione [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) , una modifica dello stato di chiamata, una chiamata "Vector" o un altro script che controlla la chiamata o al completamento della riproduzione di un messaggio registrato (in genere, che indica una modifica a "Silence" o "Music").</span><span class="sxs-lookup"><span data-stu-id="f3c66-164">This can occur in response to a [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) function, a call state change, a call "vector" or other script controlling the call, or upon completion of playback of a recorded message (ordinarily, indicating a change to "silence" or "music").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**\_trunk LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-166">Campo trunk del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-166">The trunk field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3c66-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**\_USERUSERINFO LINECALLINFOSTATE**</span><span class="sxs-lookup"><span data-stu-id="f3c66-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE\_USERUSERINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f3c66-168">Informazioni utente utente del record di informazioni sulle chiamate.</span><span class="sxs-lookup"><span data-stu-id="f3c66-168">The user-user information of the call-information record.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3c66-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3c66-169">Remarks</span></span>

<span data-ttu-id="f3c66-170">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="f3c66-170">No extensibility.</span></span> <span data-ttu-id="f3c66-171">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="f3c66-171">All 32 bits are reserved.</span></span>

<span data-ttu-id="f3c66-172">Quando si verificano modifiche in questa struttura di dati, all'applicazione viene inviato un messaggio di [**riga \_ CALLINFO**](line-callinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c66-172">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="f3c66-173">I parametri di questo messaggio sono un handle per la chiamata e un'indicazione dell'elemento informazioni che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f3c66-173">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="f3c66-174">La struttura dei dati [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) indica anche quali elementi di informazioni sulle chiamate sono validi per ogni chiamata all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="f3c66-174">The [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure also indicates which of these call information elements are valid for every call on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c66-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3c66-175">Requirements</span></span>



| <span data-ttu-id="f3c66-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3c66-176">Requirement</span></span> | <span data-ttu-id="f3c66-177">Valore</span><span class="sxs-lookup"><span data-stu-id="f3c66-177">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f3c66-178">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f3c66-178">TAPI version</span></span><br/> | <span data-ttu-id="f3c66-179">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f3c66-179">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f3c66-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3c66-180">Header</span></span><br/>       | <dl> <span data-ttu-id="f3c66-181"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c66-181"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3c66-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3c66-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c66-183">**LINEA \_ CALLINFO**</span><span class="sxs-lookup"><span data-stu-id="f3c66-183">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="f3c66-184">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="f3c66-184">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="f3c66-185">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="f3c66-185">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="f3c66-186">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="f3c66-186">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)
</dt> </dl>

 

 




