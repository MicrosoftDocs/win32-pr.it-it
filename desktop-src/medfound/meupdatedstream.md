---
description: Generato da un'origine multimediale quando viene riavviato o Cerca un flusso già attivo.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529604"
---
# <a name="meupdatedstream-event"></a><span data-ttu-id="86077-103">Evento MEUpdatedStream</span><span class="sxs-lookup"><span data-stu-id="86077-103">MEUpdatedStream event</span></span>

<span data-ttu-id="86077-104">Generato da un'origine multimediale quando viene riavviato o Cerca un flusso già attivo.</span><span class="sxs-lookup"><span data-stu-id="86077-104">Raised by a media source when it restarts or seeks a stream that is already active.</span></span>

<span data-ttu-id="86077-105">Quando il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) viene chiamato su un'origine multimediale, l'origine multimediale Invia un evento per ogni flusso selezionato:</span><span class="sxs-lookup"><span data-stu-id="86077-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="86077-106">L'origine invia l'evento [MENewStream](menewstream.md) se il flusso non è stato selezionato nella precedente chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)oppure si tratta della prima chiamata **iniziale** a questa origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="86077-106">The source sends the [MENewStream](menewstream.md) event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="86077-107">L'origine invia l'evento MEUpdatedStream se il flusso è già stato selezionato nella precedente chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="86077-107">The source sends the MEUpdatedStream event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="86077-108">Non viene inviato alcun evento per i flussi non selezionati.</span><span class="sxs-lookup"><span data-stu-id="86077-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="86077-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="86077-109">Event values</span></span>

<span data-ttu-id="86077-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="86077-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="86077-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="86077-111">VARTYPE</span></span>                | <span data-ttu-id="86077-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86077-112">Description</span></span>                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86077-113">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="86077-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="86077-114">Puntatore all'interfaccia [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) del flusso.</span><span class="sxs-lookup"><span data-stu-id="86077-114">Pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="86077-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="86077-115">Remarks</span></span>

<span data-ttu-id="86077-116">Alla prima chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in cui un flusso diventa attivo, l'origine multimediale Invia un evento [MENewStream](menewstream.md) per il flusso.</span><span class="sxs-lookup"><span data-stu-id="86077-116">On the first call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in which a stream becomes active, the media source sends an [MENewStream](menewstream.md) event for the stream.</span></span> <span data-ttu-id="86077-117">Nelle chiamate successive a **Start**, l'origine multimediale Invia un evento MEUpdatedStream, finché il flusso non viene deselezionato.</span><span class="sxs-lookup"><span data-stu-id="86077-117">On subsequent calls to **Start**, the media source sends an MEUpdatedStream event, until the stream is deselected.</span></span>

## <a name="requirements"></a><span data-ttu-id="86077-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86077-118">Requirements</span></span>



| <span data-ttu-id="86077-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86077-119">Requirement</span></span> | <span data-ttu-id="86077-120">Valore</span><span class="sxs-lookup"><span data-stu-id="86077-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86077-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86077-121">Minimum supported client</span></span><br/> | <span data-ttu-id="86077-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86077-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="86077-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86077-123">Minimum supported server</span></span><br/> | <span data-ttu-id="86077-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86077-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86077-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86077-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="86077-126"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86077-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86077-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86077-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86077-128">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86077-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




