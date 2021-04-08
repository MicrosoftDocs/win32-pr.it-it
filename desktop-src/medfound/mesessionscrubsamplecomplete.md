---
description: Generato dalla sessione multimediale quando completa una richiesta di ripulitura.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Evento MESessionScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880254"
---
# <a name="mesessionscrubsamplecomplete-event"></a><span data-ttu-id="7a828-103">Evento MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="7a828-103">MESessionScrubSampleComplete event</span></span>

<span data-ttu-id="7a828-104">Generato dalla sessione multimediale quando completa una richiesta di ripulitura.</span><span class="sxs-lookup"><span data-stu-id="7a828-104">Raised by the Media Session when it completes a scrubbing request.</span></span>

<span data-ttu-id="7a828-105">Lo scrubbing si verifica quando la velocità di riproduzione è zero e l'applicazione chiama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="7a828-105">Scrubbing occurs when the playback rate is zero and the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="7a828-106">Questo evento viene generato dopo che ogni sink di flusso ha completato la richiesta di ripulitura.</span><span class="sxs-lookup"><span data-stu-id="7a828-106">This event is raised after every stream sink has completed the scrubbing request.</span></span>

## <a name="event-values"></a><span data-ttu-id="7a828-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="7a828-107">Event values</span></span>

<span data-ttu-id="7a828-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="7a828-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="7a828-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="7a828-109">VARTYPE</span></span>              | <span data-ttu-id="7a828-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a828-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="7a828-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="7a828-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="7a828-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7a828-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="7a828-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a828-113">Requirements</span></span>



| <span data-ttu-id="7a828-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a828-114">Requirement</span></span> | <span data-ttu-id="7a828-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7a828-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a828-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a828-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7a828-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a828-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7a828-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a828-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7a828-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a828-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a828-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a828-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a828-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a828-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a828-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a828-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a828-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7a828-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="7a828-124">MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="7a828-124">MEStreamSinkScrubSampleComplete</span></span>](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




