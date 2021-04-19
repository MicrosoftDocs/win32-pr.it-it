---
description: Generato da un sink del flusso quando completa una richiesta di ripulitura.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Evento MEStreamSinkScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318069"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a><span data-ttu-id="b871c-103">Evento MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="b871c-103">MEStreamSinkScrubSampleComplete event</span></span>

<span data-ttu-id="b871c-104">Generato da un sink del flusso quando completa una richiesta di ripulitura.</span><span class="sxs-lookup"><span data-stu-id="b871c-104">Raised by a stream sink when it completes a scrubbing request.</span></span>

<span data-ttu-id="b871c-105">Lo scrubbing si verifica quando la velocità di riproduzione è zero e il clock di presentazione viene avviato con un tempo di srubbing specificato.</span><span class="sxs-lookup"><span data-stu-id="b871c-105">Scrubbing occurs when the playback rate is zero and the presentation clock is started with a specified srubbing time.</span></span> <span data-ttu-id="b871c-106">Se un sink multimediale supporta lo scrubbing, ogni flusso del sink genera questo evento ogni volta che viene chiamato il metodo [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) mentre la velocità di riproduzione è zero.</span><span class="sxs-lookup"><span data-stu-id="b871c-106">If a media sink supports scrubbing, every stream on the sink raises this event whenever the [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) method is called while the playback rate is zero.</span></span>

<span data-ttu-id="b871c-107">Se il flusso esegue il rendering dei dati durante lo scrubbing, invia l'evento non appena viene eseguito il rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="b871c-107">If the stream renders data while scrubbing, it sends the event as soon as the data is rendered.</span></span> <span data-ttu-id="b871c-108">Se il flusso non esegue il rendering dei dati, invia l'evento immediatamente dopo la chiamata a [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .</span><span class="sxs-lookup"><span data-stu-id="b871c-108">If the stream does not render data, it sends the event immediately after [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="b871c-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="b871c-109">Event values</span></span>

<span data-ttu-id="b871c-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="b871c-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b871c-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b871c-111">VARTYPE</span></span>              | <span data-ttu-id="b871c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b871c-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b871c-113">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="b871c-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b871c-114">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b871c-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="b871c-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="b871c-115">Attributes</span></span>

<span data-ttu-id="b871c-116">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b871c-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="b871c-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="b871c-117">Attribute</span></span>                                                                              | <span data-ttu-id="b871c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b871c-118">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b871c-119">**\_tempo di \_ SCRUBSAMPLE \_ evento MF**</span><span class="sxs-lookup"><span data-stu-id="b871c-119">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)<br/> | <span data-ttu-id="b871c-120">Tempo di presentazione per cui è stato eseguito il rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="b871c-120">Presentation time for which data was rendered.</span></span> <span data-ttu-id="b871c-121">Se il sink multimediale non esegue il rendering dei dati durante lo scrubbing, questo attributo non viene impostato.</span><span class="sxs-lookup"><span data-stu-id="b871c-121">If the media sink does not render data while scrubbing, it does not set this attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b871c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b871c-122">Requirements</span></span>



| <span data-ttu-id="b871c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b871c-123">Requirement</span></span> | <span data-ttu-id="b871c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b871c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b871c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b871c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b871c-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b871c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b871c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b871c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b871c-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b871c-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b871c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b871c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b871c-130"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b871c-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b871c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b871c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b871c-132">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b871c-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="b871c-133">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="b871c-133">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="b871c-134">MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="b871c-134">MESessionScrubSampleComplete</span></span>](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




