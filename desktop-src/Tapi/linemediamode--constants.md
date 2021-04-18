---
description: Le \_ costanti LINEMEDIAMODE descrivono i tipi di supporto (o le modalità) di una sessione di comunicazione o di una chiamata.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Costanti LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331026"
---
# <a name="linemediamode_-constants"></a><span data-ttu-id="5d107-103">\_Costanti LINEMEDIAMODE</span><span class="sxs-lookup"><span data-stu-id="5d107-103">LINEMEDIAMODE\_ Constants</span></span>

<span data-ttu-id="5d107-104">Le **costanti \_ LINEMEDIAMODE** descrivono i tipi di supporto (o le modalità) di una sessione di comunicazione o di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-104">The **LINEMEDIAMODE\_** constants describe media types (or modes)of a communications session or call.</span></span>

<dl> <dt>

<span data-ttu-id="5d107-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**\_AUTOMATEDVOICE LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-105"><span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE\_AUTOMATEDVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-106">L'energia vocale è stata rilevata nella chiamata e la voce viene gestita localmente da un'applicazione automatizzata, ad esempio con un'applicazione per la segreteria del computer.</span><span class="sxs-lookup"><span data-stu-id="5d107-106">Voice energy was detected on the call, and the voice is locally handled by an automated application such as with an answering machine application.</span></span> <span data-ttu-id="5d107-107">Quando un provider di servizi non è in grado di distinguere la voce interattiva e automatica di una chiamata in ingresso, la chiamata verrà segnalata come voce interattiva.</span><span class="sxs-lookup"><span data-stu-id="5d107-107">When a service provider cannot distinguish between interactive and automated voice on an incoming call, it will report the call as interactive voice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAmodel**</span><span class="sxs-lookup"><span data-stu-id="5d107-108"><span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE\_DATAMODEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-109">Sessione del modem dati sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-109">A data modem session on the call.</span></span> <span data-ttu-id="5d107-110">Per i protocolli modem correnti è richiesta la stazione chiamata per avviare l'handshake.</span><span class="sxs-lookup"><span data-stu-id="5d107-110">Current modem protocols require the called station to initiate the handshake.</span></span> <span data-ttu-id="5d107-111">Per una chiamata al modem dati in ingresso, l'applicazione in genere non può eseguire alcun rilevamento positivo.</span><span class="sxs-lookup"><span data-stu-id="5d107-111">For an incoming data modem call, the application can typically make no positive detection.</span></span> <span data-ttu-id="5d107-112">Il modo in cui il provider di servizi effettua questa determinazione è la scelta.</span><span class="sxs-lookup"><span data-stu-id="5d107-112">How the service provider makes this determination is its choice.</span></span> <span data-ttu-id="5d107-113">Ad esempio, un periodo di silenzio immediatamente dopo la risposta a una chiamata in ingresso può essere usato come euristica per decidere che potrebbe trattarsi di una chiamata al modem dati.</span><span class="sxs-lookup"><span data-stu-id="5d107-113">For example, a period of silence just after answering an incoming call can be used as a heuristic to decide that this might be a data modem call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**</span><span class="sxs-lookup"><span data-stu-id="5d107-114"><span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE\_ADSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-115">Una sessione ADSI (analogous display Services Interface) nella chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-115">An ADSI (Analog Display Services Interface) session on the call.</span></span> <span data-ttu-id="5d107-116">ADSI migliora le chiamate vocali con le informazioni alfanumeriche scaricate sul telefono e l'uso di pulsanti soft sul telefono.</span><span class="sxs-lookup"><span data-stu-id="5d107-116">ADSI enhances voice calls with alphanumeric information downloaded to the phone and the use of soft buttons on the phone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**\_DIGITALDATA LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-117"><span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE\_DIGITALDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-118">Flusso di dati digitali di formato non specificato.</span><span class="sxs-lookup"><span data-stu-id="5d107-118">A digital data stream of unspecified format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**\_G3FAX LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-119"><span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE\_G3FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-120">È in corso l'invio o la ricezione di un fax del gruppo 3 attraverso la chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-120">A group 3 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**\_G4FAX LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-121"><span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE\_G4FAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-122">È in corso l'invio o la ricezione di un fax del gruppo 4 sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-122">A group 4 fax is being sent or received over the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**\_INTERACTIVEVOICE LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-123"><span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE\_INTERACTIVEVOICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-124">L'energia vocale è stata rilevata nella chiamata e la chiamata viene gestita come chiamata vocale interattiva con gli utenti a entrambe le estremità.</span><span class="sxs-lookup"><span data-stu-id="5d107-124">Voice energy was detected on the call, and the call is handled as an interactive voice call with humans on both ends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ misto**</span><span class="sxs-lookup"><span data-stu-id="5d107-125"><span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE\_MIXED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-126">Sessione mista sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-126">A mixed session on the call.</span></span> <span data-ttu-id="5d107-127">Mixed è uno dei servizi di telematica ISDN.</span><span class="sxs-lookup"><span data-stu-id="5d107-127">Mixed is one of the ISDN telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**</span><span class="sxs-lookup"><span data-stu-id="5d107-128"><span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE\_TDD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-129">Una sessione TDD (dispositivi di telefonia per la sordità) nella chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-129">A TDD (Telephony Devices for the Deaf) session on the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**\_Teletex LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-130"><span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE\_TELETEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-131">Una sessione Teletex sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-131">A teletex session on the call.</span></span> <span data-ttu-id="5d107-132">Teletex è uno dei servizi telematici.</span><span class="sxs-lookup"><span data-stu-id="5d107-132">Teletex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**\_telex LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-133"><span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE\_TELEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-134">Una sessione telex sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-134">A telex session on the call.</span></span> <span data-ttu-id="5d107-135">Telex è uno dei servizi telematici.</span><span class="sxs-lookup"><span data-stu-id="5d107-135">Telex is one of the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**VIDEO di LINEMEDIAMODE \_**</span><span class="sxs-lookup"><span data-stu-id="5d107-136"><span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE\_VIDEO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-137">Il tipo di supporto della chiamata è video.</span><span class="sxs-lookup"><span data-stu-id="5d107-137">The media type of the call is video.</span></span> <span data-ttu-id="5d107-138">(Versioni TAPI 2,1 e successive)</span><span class="sxs-lookup"><span data-stu-id="5d107-138">(TAPI versions 2.1 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**\_VIDEOTEX LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-139"><span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE\_VIDEOTEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-140">Una sessione videotex sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-140">A videotex session on the call.</span></span> <span data-ttu-id="5d107-141">Videotex è uno dei servizi telematici.</span><span class="sxs-lookup"><span data-stu-id="5d107-141">Videotex is one the telematic services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**\_VOICEVIEW LINEMEDIAMODE**</span><span class="sxs-lookup"><span data-stu-id="5d107-142"><span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE\_VOICEVIEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-143">Il tipo di supporto della chiamata è VoiceView.</span><span class="sxs-lookup"><span data-stu-id="5d107-143">The media type of the call is VoiceView.</span></span> <span data-ttu-id="5d107-144">(Versioni TAPI 1,4 e successive)</span><span class="sxs-lookup"><span data-stu-id="5d107-144">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5d107-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="5d107-145"><span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5d107-146">Un flusso multimediale esiste ma la relativa modalità non è attualmente nota e potrebbe essere nota in seguito.</span><span class="sxs-lookup"><span data-stu-id="5d107-146">A media stream exists but its mode is not currently known and may become known later.</span></span> <span data-ttu-id="5d107-147">Corrisponderebbe a una chiamata con un tipo di supporto non classificato.</span><span class="sxs-lookup"><span data-stu-id="5d107-147">This would correspond to a call with an unclassified media type.</span></span> <span data-ttu-id="5d107-148">Nei tipici ambienti di telefonia analogica, il tipo di supporto di una chiamata in ingresso può essere sconosciuto fino a quando non viene ricevuta la risposta alla chiamata e il flusso multimediale è stato filtrato per effettuare una determinazione.</span><span class="sxs-lookup"><span data-stu-id="5d107-148">In typical analog telephony environments, an incoming call's media type may be unknown until after the call has been answered and the media stream has been filtered to make a determination.</span></span>

<span data-ttu-id="5d107-149">Se è impostato il flag della modalità media sconosciuta, è possibile impostare anche altri flag di supporto.</span><span class="sxs-lookup"><span data-stu-id="5d107-149">If the unknown media-mode flag is set, other media flags can also be set.</span></span> <span data-ttu-id="5d107-150">Viene utilizzato per indicare che il supporto è sconosciuto, ma che probabilmente è uno degli altri tipi di supporti selezionati.</span><span class="sxs-lookup"><span data-stu-id="5d107-150">This is used to signify that the media is unknown but that it is likely to be one of the other selected media types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d107-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d107-151">Remarks</span></span>

<span data-ttu-id="5d107-152">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="5d107-152">All 32 bits are reserved.</span></span>

<span data-ttu-id="5d107-153">Si noti che la modalità di porta e il tipo di supporto sono nozioni differenti.</span><span class="sxs-lookup"><span data-stu-id="5d107-153">Note that bearer mode and media type are different notions.</span></span> <span data-ttu-id="5d107-154">La modalità di connessione di una chiamata indica la qualità della connessione telefonica fornita principalmente dalla rete.</span><span class="sxs-lookup"><span data-stu-id="5d107-154">The bearer mode of a call is an indication of the quality of the telephone connection as provided primarily by the network.</span></span> <span data-ttu-id="5d107-155">Il tipo di supporto di una chiamata indica il tipo di flusso di informazioni scambiato tramite la chiamata.</span><span class="sxs-lookup"><span data-stu-id="5d107-155">The media type of a call is an indication of the type of information stream that is exchanged over that call.</span></span> <span data-ttu-id="5d107-156">Il fax del gruppo 3 o il modem dati sono tipi di supporti che usano una chiamata con la modalità di connessione vocale a 3,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="5d107-156">Group 3 fax or data modem are media types that use a call with a 3.1 kHz voice bearer mode.</span></span>

<span data-ttu-id="5d107-157">Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare questo \_ valore LINEMEDIAMODE se non è supportato nella versione negoziata.</span><span class="sxs-lookup"><span data-stu-id="5d107-157">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEMEDIAMODE\_ value if not supported on the negotiated version.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d107-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d107-158">Requirements</span></span>



| <span data-ttu-id="5d107-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d107-159">Requirement</span></span> | <span data-ttu-id="5d107-160">Valore</span><span class="sxs-lookup"><span data-stu-id="5d107-160">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5d107-161">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="5d107-161">TAPI version</span></span><br/> | <span data-ttu-id="5d107-162">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5d107-162">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5d107-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d107-163">Header</span></span><br/>       | <dl> <span data-ttu-id="5d107-164"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d107-164"><dt>Tapi.h</dt></span></span> </dl> |



 

 




