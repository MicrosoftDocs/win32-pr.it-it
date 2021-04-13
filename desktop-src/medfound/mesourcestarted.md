---
description: Generato quando un'origine multimediale viene avviata senza cercare.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Evento MESourceStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528261"
---
# <a name="mesourcestarted-event"></a><span data-ttu-id="4b3f1-103">Evento MESourceStarted</span><span class="sxs-lookup"><span data-stu-id="4b3f1-103">MESourceStarted event</span></span>

<span data-ttu-id="4b3f1-104">Generato quando un'origine multimediale viene avviata senza cercare.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-104">Raised when a media source starts without seeking.</span></span>

## <a name="event-values"></a><span data-ttu-id="4b3f1-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="4b3f1-105">Event values</span></span>

<span data-ttu-id="4b3f1-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4b3f1-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4b3f1-107">VARTYPE</span></span>              | <span data-ttu-id="4b3f1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b3f1-108">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3f1-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="4b3f1-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4b3f1-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-110">No event data.</span></span> <span data-ttu-id="4b3f1-111">L'ora di inizio è stata dalla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-111">The start time was from the current position.</span></span><br/> <br/>                            |
| <span data-ttu-id="4b3f1-112">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="4b3f1-112">VT\_I8</span></span><br/>    | <span data-ttu-id="4b3f1-113">Ora di inizio, in unità di 100 nanosecondi, relativa ai timestamp degli esempi.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-113">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="4b3f1-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="4b3f1-114">Attributes</span></span>

<span data-ttu-id="4b3f1-115">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="4b3f1-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="4b3f1-116">Attribute</span></span>                                                                                     | <span data-ttu-id="4b3f1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b3f1-117">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b3f1-118">**\_ \_ \_ inizio effettivo origine evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="4b3f1-118">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)<br/> | <span data-ttu-id="4b3f1-119">Ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-119">Start time.</span></span> <span data-ttu-id="4b3f1-120">L'origine multimediale imposta questo attributo se viene riavviato dalla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-120">The media source sets this attribute if it restarts from its current position.</span></span><br/> <br/>                     |
| [<span data-ttu-id="4b3f1-121">**\_ \_ \_ inizio Fake origine evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="4b3f1-121">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)<br/>     | <span data-ttu-id="4b3f1-122">Specifica se la topologia del segmento corrente è vuota.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-122">Specifies whether the current segment topology is empty.</span></span> <span data-ttu-id="4b3f1-123">L'origine di Sequencer imposta questo attributo.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-123">The sequencer source sets this attribute.</span></span><br/> <br/>             |
| [<span data-ttu-id="4b3f1-124">**\_origine evento \_ MF \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="4b3f1-124">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)<br/>  | <span data-ttu-id="4b3f1-125">Ora di inizio per un segmento rispetto all'inizio della presentazione.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-125">Start time for a segment, relative to the start of the presentation.</span></span> <span data-ttu-id="4b3f1-126">L'origine di Sequencer imposta questo attributo.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-126">The sequencer source sets this attribute.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4b3f1-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b3f1-127">Remarks</span></span>

<span data-ttu-id="4b3f1-128">Un'origine multimediale genera questo evento quando inizia da uno stato interrotto o inizia da uno stato di sospensione nella stessa posizione dell'origine.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-128">A media source raises this event when it starts from a stopped state, or starts from a paused state at the same position in the source.</span></span> <span data-ttu-id="4b3f1-129">L'evento viene generato se il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-129">The event is raised if the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method returns S\_OK.</span></span>

<span data-ttu-id="4b3f1-130">Se l'origine multimediale inizia dalla posizione corrente e lo stato precedente dell'origine è in esecuzione o in pausa, i dati dell'evento possono essere vuoti (VT \_ vuoto).</span><span class="sxs-lookup"><span data-stu-id="4b3f1-130">If the media source starts from the current position and the source's previous state was running or paused, the event data can empty (VT\_EMPTY).</span></span> <span data-ttu-id="4b3f1-131">Se i dati dell'evento sono VT \_ vuoti, l'origine del supporto potrebbe impostare l'attributo [**\_ \_ \_ \_ Start effettivo dell'origine eventi MF**](mf-event-source-actual-start-attribute.md) con l'ora di inizio effettiva.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-131">If the event data is VT\_EMPTY, the media source might set the [**MF\_EVENT\_SOURCE\_ACTUAL\_START**](mf-event-source-actual-start-attribute.md) attribute with the actual starting time.</span></span>

<span data-ttu-id="4b3f1-132">Se l'origine multimediale viene avviata da una nuova posizione o lo stato precedente dell'origine è stato arrestato, i dati dell'evento devono essere l'ora di inizio (VT \_ I8).</span><span class="sxs-lookup"><span data-stu-id="4b3f1-132">If the media source starts from a new position, or the source's previous state was stopped, the event data must be the starting time (VT\_I8).</span></span>

<span data-ttu-id="4b3f1-133">Se il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa una ricerca, l'origine multimediale invia l'evento [MESourceSeeked](mesourceseeked.md) anziché MESourceStarted.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-133">If the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method causes a seek, the media source sends the [MESourceSeeked](mesourceseeked.md) event instead of MESourceStarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b3f1-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b3f1-134">Requirements</span></span>



| <span data-ttu-id="4b3f1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b3f1-135">Requirement</span></span> | <span data-ttu-id="4b3f1-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4b3f1-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3f1-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b3f1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4b3f1-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b3f1-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4b3f1-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b3f1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4b3f1-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b3f1-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b3f1-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b3f1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b3f1-142"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b3f1-142"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b3f1-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b3f1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3f1-144">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b3f1-144">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




