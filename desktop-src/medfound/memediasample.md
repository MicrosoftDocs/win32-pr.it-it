---
description: 'Inviato quando un flusso multimediale fornisce un nuovo esempio in risposta a una chiamata a IMFMediaStream:: RequestSample.'
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: Evento MEMediaSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320581"
---
# <a name="memediasample-event"></a><span data-ttu-id="41c1a-103">Evento MEMediaSample</span><span class="sxs-lookup"><span data-stu-id="41c1a-103">MEMediaSample event</span></span>

<span data-ttu-id="41c1a-104">Inviato quando un flusso multimediale fornisce un nuovo esempio in risposta a una chiamata a [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="41c1a-104">Sent when a media stream delivers a new sample in response to a call to [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span>

## <a name="event-values"></a><span data-ttu-id="41c1a-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="41c1a-105">Event values</span></span>

<span data-ttu-id="41c1a-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="41c1a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="41c1a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="41c1a-107">VARTYPE</span></span>                | <span data-ttu-id="41c1a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41c1a-108">Description</span></span>                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c1a-109">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="41c1a-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="41c1a-110">Puntatore all'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="41c1a-110">Pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of the sample.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="41c1a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41c1a-111">Requirements</span></span>



| <span data-ttu-id="41c1a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c1a-112">Requirement</span></span> | <span data-ttu-id="41c1a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="41c1a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c1a-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c1a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="41c1a-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41c1a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41c1a-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c1a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="41c1a-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41c1a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41c1a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41c1a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c1a-119"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41c1a-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c1a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41c1a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c1a-121">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41c1a-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="41c1a-122">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="41c1a-122">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 




