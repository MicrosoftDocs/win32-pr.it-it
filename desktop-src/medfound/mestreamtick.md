---
description: Segnala che a un flusso multimediale non sono disponibili dati a un'ora specificata.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307991"
---
# <a name="mestreamtick-event"></a><span data-ttu-id="a4251-103">Evento MEStreamTick</span><span class="sxs-lookup"><span data-stu-id="a4251-103">MEStreamTick event</span></span>

<span data-ttu-id="a4251-104">Segnala che a un flusso multimediale non sono disponibili dati a un'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="a4251-104">Signals that a media stream does not have data available at a specified time.</span></span>

## <a name="event-values"></a><span data-ttu-id="a4251-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="a4251-105">Event values</span></span>

<span data-ttu-id="a4251-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="a4251-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a4251-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a4251-107">VARTYPE</span></span>           | <span data-ttu-id="a4251-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4251-108">Description</span></span>                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="a4251-109">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="a4251-109">VT\_I8</span></span><br/> | <span data-ttu-id="a4251-110">Data e ora in cui si verifica il gap, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="a4251-110">Time at which the gap occurs, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a4251-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4251-111">Remarks</span></span>

<span data-ttu-id="a4251-112">Questo evento segnala un gap nei dati.</span><span class="sxs-lookup"><span data-stu-id="a4251-112">This event signals a gap in the data.</span></span> <span data-ttu-id="a4251-113">L'evento notifica ai componenti downstream di non prevedere i dati all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="a4251-113">The event notifies downstream components not to expect any data at the specified time.</span></span>

<span data-ttu-id="a4251-114">L'evento deve essere inviato da qualsiasi oggetto genera i timestamp per gli esempi di supporti nel flusso.</span><span class="sxs-lookup"><span data-stu-id="a4251-114">The event should be sent by whichever object generates the time stamps for the media samples in the stream.</span></span> <span data-ttu-id="a4251-115">A seconda del formato dei dati, è possibile:</span><span class="sxs-lookup"><span data-stu-id="a4251-115">Depending on the format of the data, this is either:</span></span>

-   <span data-ttu-id="a4251-116">Il flusso multimediale nell'origine supporto (interfaccia [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ) o</span><span class="sxs-lookup"><span data-stu-id="a4251-116">The media stream on the media source ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface), or</span></span>
-   <span data-ttu-id="a4251-117">Trasformazione del decodificatore (interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).</span><span class="sxs-lookup"><span data-stu-id="a4251-117">The decoder transform ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface).</span></span>

<span data-ttu-id="a4251-118">Durante il gap, l'oggetto deve inviare l'evento con la stessa frequenza con cui produrrebbe normalmente esempi.</span><span class="sxs-lookup"><span data-stu-id="a4251-118">During the gap, the object should send the event about as often as it would normally produce samples.</span></span> <span data-ttu-id="a4251-119">Per video, inviare un evento per ogni frame mancante.</span><span class="sxs-lookup"><span data-stu-id="a4251-119">For video, send one event for each missing frame.</span></span> <span data-ttu-id="a4251-120">Per l'audio, inviare l'evento almeno una volta al secondo durante il gap.</span><span class="sxs-lookup"><span data-stu-id="a4251-120">For audio, send the event at least once per second during the gap.</span></span> <span data-ttu-id="a4251-121">Il valore dell'evento è il timestamp dell'esempio mancante.</span><span class="sxs-lookup"><span data-stu-id="a4251-121">The value of the event is the time stamp of the missing sample.</span></span> <span data-ttu-id="a4251-122">Inviare tutti gli eventi MEStreamTick necessari per colmare il gap nei dati.</span><span class="sxs-lookup"><span data-stu-id="a4251-122">Send as many MEStreamTick events as needed to fill the gap in the data.</span></span>

<span data-ttu-id="a4251-123">Se un'origine multimediale presenta diversi flussi e si verifica un gap in più di un flusso, ogni flusso deve inviare eventi MEStreamTick.</span><span class="sxs-lookup"><span data-stu-id="a4251-123">If a media source has several streams and there is a gap in more than one stream, each stream should send MEStreamTick events.</span></span> <span data-ttu-id="a4251-124">Se, ad esempio, è presente un gap nei dati audio e video, entrambi i flussi inviano l'evento.</span><span class="sxs-lookup"><span data-stu-id="a4251-124">For example, if there is a gap in both audio and video data, then both streams send the event.</span></span>

<span data-ttu-id="a4251-125">L'evento MEStreamTick non completa una richiesta [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="a4251-125">The MEStreamTick event does not complete an [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) request.</span></span> <span data-ttu-id="a4251-126">L'origine multimediale deve comunque inviare un evento [MEMediaSample](memediasample.md) per ogni chiamata a **RequestSample**.</span><span class="sxs-lookup"><span data-stu-id="a4251-126">The media source must still send an [MEMediaSample](memediasample.md) event for each call to **RequestSample**.</span></span>

<span data-ttu-id="a4251-127">I sink di supporto non possono utilizzare direttamente questo evento.</span><span class="sxs-lookup"><span data-stu-id="a4251-127">Media sinks cannot consume this event directly.</span></span> <span data-ttu-id="a4251-128">Per segnalare un gap nel flusso a un sink multimediale, chiamare [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) con un marcatore di segno di **MFSTREAMSINK \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="a4251-128">To signal a gap in the stream to a media sink, call [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) with an **MFSTREAMSINK\_MARKER\_TICK** marker.</span></span> <span data-ttu-id="a4251-129">Quando necessario, la pipeline Media Foundation Converte gli eventi MEStreamTick in marcatori di segno di **MFSTREAMSINK \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="a4251-129">The Media Foundation pipeline converts MEStreamTick events to **MFSTREAMSINK\_MARKER\_TICK** markers when needed.</span></span>

<span data-ttu-id="a4251-130">Non impostare l'attributo [**di \_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) nel successivo esempio di supporto dopo un evento MEStreamTick.</span><span class="sxs-lookup"><span data-stu-id="a4251-130">Do not set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the next media sample after an MEStreamTick event.</span></span> <span data-ttu-id="a4251-131">L'attributo di **\_ discontinuità MFSampleExtension** implica che il timestamp è discontinuo con i timestamp precedenti, mentre MEStreamTick implica che i timestamp sono continui ma alcuni dati risultano mancanti.</span><span class="sxs-lookup"><span data-stu-id="a4251-131">The **MFSampleExtension\_Discontinuity** attribute implies that the time stamp is discontinuous with previous time stamps, whereas MEStreamTick implies that time stamps are continuous but some data is missing.</span></span>

> [!Note]  
> <span data-ttu-id="a4251-132">Una versione precedente della documentazione ha erroneamente dichiarato che l'esempio dopo un evento MEStreamTick deve avere l'attributo [**di \_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a4251-132">An earlier version of the documentation incorrectly stated that the sample after an MEStreamTick event should have the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a4251-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4251-133">Requirements</span></span>



| <span data-ttu-id="a4251-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4251-134">Requirement</span></span> | <span data-ttu-id="a4251-135">Valore</span><span class="sxs-lookup"><span data-stu-id="a4251-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4251-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4251-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a4251-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4251-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a4251-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4251-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a4251-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4251-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a4251-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4251-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4251-141"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4251-141"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4251-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4251-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4251-143">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4251-143">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




