---
description: Generato da un flusso multimediale quando il metodo IMFMediaSource::P ause viene completato in modo asincrono.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: Evento MEStreamPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307993"
---
# <a name="mestreampaused-event"></a><span data-ttu-id="23b1d-103">Evento MEStreamPaused</span><span class="sxs-lookup"><span data-stu-id="23b1d-103">MEStreamPaused event</span></span>

<span data-ttu-id="23b1d-104">Generato da un flusso multimediale quando il metodo [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="23b1d-104">Raised by a media stream when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="23b1d-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="23b1d-105">Event values</span></span>

<span data-ttu-id="23b1d-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="23b1d-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="23b1d-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="23b1d-107">VARTYPE</span></span>              | <span data-ttu-id="23b1d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23b1d-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="23b1d-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="23b1d-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="23b1d-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="23b1d-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="23b1d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="23b1d-111">Remarks</span></span>

<span data-ttu-id="23b1d-112">Ogni flusso attivo nella presentazione Invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="23b1d-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="23b1d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23b1d-113">Requirements</span></span>



| <span data-ttu-id="23b1d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b1d-114">Requirement</span></span> | <span data-ttu-id="23b1d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="23b1d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23b1d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23b1d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23b1d-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23b1d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="23b1d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23b1d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23b1d-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23b1d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="23b1d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23b1d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b1d-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23b1d-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b1d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23b1d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b1d-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23b1d-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




