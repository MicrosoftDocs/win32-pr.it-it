---
description: "Generato da un flusso multimediale dopo una chiamata a IMFMediaSource:: Start causa una ricerca nel flusso. Un flusso multimediale genera questo evento quando l'origine multimediale genera l'evento MESourceSeeked."
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Evento MEStreamSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226653"
---
# <a name="mestreamseeked-event"></a><span data-ttu-id="000c1-104">Evento MEStreamSeeked</span><span class="sxs-lookup"><span data-stu-id="000c1-104">MEStreamSeeked event</span></span>

<span data-ttu-id="000c1-105">Generato da un flusso multimediale dopo una chiamata a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa una ricerca nel flusso.</span><span class="sxs-lookup"><span data-stu-id="000c1-105">Raised by a media stream after a call to [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causes a seek in the stream.</span></span> <span data-ttu-id="000c1-106">Un flusso multimediale genera questo evento quando l'origine multimediale genera l'evento [MESourceSeeked](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="000c1-106">A media stream raises this event when the media source raises the [MESourceSeeked](mesourceseeked.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="000c1-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="000c1-107">Event values</span></span>

<span data-ttu-id="000c1-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="000c1-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="000c1-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="000c1-109">VARTYPE</span></span>           | <span data-ttu-id="000c1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="000c1-110">Description</span></span>                                                        |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="000c1-111">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="000c1-111">VT\_I8</span></span><br/> | <span data-ttu-id="000c1-112">Nuova ora di inizio, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="000c1-112">New starting time, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="000c1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="000c1-113">Requirements</span></span>



| <span data-ttu-id="000c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="000c1-114">Requirement</span></span> | <span data-ttu-id="000c1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="000c1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="000c1-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="000c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="000c1-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="000c1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="000c1-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="000c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="000c1-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="000c1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="000c1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="000c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="000c1-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="000c1-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000c1-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="000c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000c1-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="000c1-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




