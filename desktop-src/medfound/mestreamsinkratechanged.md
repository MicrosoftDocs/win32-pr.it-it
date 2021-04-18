---
description: Generato da un sink del flusso quando la frequenza è cambiata.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Evento MEStreamSinkRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315045"
---
# <a name="mestreamsinkratechanged-event"></a><span data-ttu-id="c0966-103">Evento MEStreamSinkRateChanged</span><span class="sxs-lookup"><span data-stu-id="c0966-103">MEStreamSinkRateChanged event</span></span>

<span data-ttu-id="c0966-104">Generato da un sink del flusso quando la frequenza è cambiata.</span><span class="sxs-lookup"><span data-stu-id="c0966-104">Raised by a stream sink when the rate has changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="c0966-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="c0966-105">Event values</span></span>

<span data-ttu-id="c0966-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0966-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c0966-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c0966-107">VARTYPE</span></span>              | <span data-ttu-id="c0966-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0966-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c0966-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="c0966-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c0966-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c0966-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c0966-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0966-111">Remarks</span></span>

<span data-ttu-id="c0966-112">Se un sink del flusso supporta le modifiche di frequenza, questo evento viene inviato dopo il completamento della modifica della frequenza.</span><span class="sxs-lookup"><span data-stu-id="c0966-112">If a stream sink supports rate changes, it sends this event after the rate change is complete.</span></span> <span data-ttu-id="c0966-113">L'evento viene inviato una volta per ogni chiamata al metodo [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del sink.</span><span class="sxs-lookup"><span data-stu-id="c0966-113">The event is sent once for each call to the sink's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span> <span data-ttu-id="c0966-114">Se la modifica della frequenza ha esito negativo, il valore dello stato dell'evento è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="c0966-114">If the rate change is not successful, the event status value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0966-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0966-115">Requirements</span></span>



| <span data-ttu-id="c0966-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0966-116">Requirement</span></span> | <span data-ttu-id="c0966-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c0966-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0966-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0966-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c0966-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0966-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c0966-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0966-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c0966-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0966-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c0966-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0966-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0966-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0966-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0966-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0966-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0966-125">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0966-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="c0966-126">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="c0966-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




