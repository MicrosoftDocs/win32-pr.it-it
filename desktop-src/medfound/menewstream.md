---
description: Generato da un'origine multimediale quando avvia un nuovo flusso.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309630"
---
# <a name="menewstream-event"></a><span data-ttu-id="32f2f-103">Evento MENewStream</span><span class="sxs-lookup"><span data-stu-id="32f2f-103">MENewStream event</span></span>

<span data-ttu-id="32f2f-104">Generato da un'origine multimediale quando avvia un nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="32f2f-104">Raised by a media source when it starts a new stream.</span></span>

<span data-ttu-id="32f2f-105">Quando il metodo [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) viene chiamato su un'origine multimediale, l'origine multimediale Invia un evento per ogni flusso selezionato:</span><span class="sxs-lookup"><span data-stu-id="32f2f-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="32f2f-106">L'origine invia l'evento MENewStream se il flusso non è stato selezionato nella precedente chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)oppure si tratta della prima chiamata **iniziale** a questa origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="32f2f-106">The source sends the MENewStream event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="32f2f-107">L'origine invia l'evento [MEUpdatedStream](meupdatedstream.md) se il flusso è già stato selezionato nella precedente chiamata a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="32f2f-107">The source sends the [MEUpdatedStream](meupdatedstream.md) event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="32f2f-108">Non viene inviato alcun evento per i flussi non selezionati.</span><span class="sxs-lookup"><span data-stu-id="32f2f-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="32f2f-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="32f2f-109">Event values</span></span>

<span data-ttu-id="32f2f-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="32f2f-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="32f2f-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="32f2f-111">VARTYPE</span></span>                | <span data-ttu-id="32f2f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32f2f-112">Description</span></span>                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f2f-113">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="32f2f-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="32f2f-114">Contiene un puntatore all'interfaccia [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) del flusso.</span><span class="sxs-lookup"><span data-stu-id="32f2f-114">Contains a pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="32f2f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32f2f-115">Requirements</span></span>



| <span data-ttu-id="32f2f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f2f-116">Requirement</span></span> | <span data-ttu-id="32f2f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="32f2f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f2f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f2f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32f2f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32f2f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="32f2f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f2f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32f2f-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32f2f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32f2f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32f2f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f2f-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32f2f-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32f2f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32f2f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f2f-125">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="32f2f-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




