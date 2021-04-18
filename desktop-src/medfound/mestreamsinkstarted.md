---
description: Generato da un sink del flusso quando completa la transizione allo stato di esecuzione.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Evento MEStreamSinkStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309603"
---
# <a name="mestreamsinkstarted-event"></a><span data-ttu-id="93673-103">Evento MEStreamSinkStarted</span><span class="sxs-lookup"><span data-stu-id="93673-103">MEStreamSinkStarted event</span></span>

<span data-ttu-id="93673-104">Generato da un sink del flusso quando completa la transizione allo stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="93673-104">Raised by a stream sink when it completes the transition to the running state.</span></span> <span data-ttu-id="93673-105">La transizione all'esecuzione si verifica quando viene chiamato il metodo [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) sul clock di presentazione del sink.</span><span class="sxs-lookup"><span data-stu-id="93673-105">The transition to running occurs when the [**IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) method is called on the sink's presentation clock.</span></span> <span data-ttu-id="93673-106">Il sink multimediale riceve la notifica tramite il metodo [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) o [**IMFClockStateSink:: OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) .</span><span class="sxs-lookup"><span data-stu-id="93673-106">The media sink receives the notification through its [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="93673-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="93673-107">Event values</span></span>

<span data-ttu-id="93673-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="93673-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="93673-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="93673-109">VARTYPE</span></span>              | <span data-ttu-id="93673-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93673-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="93673-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="93673-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="93673-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="93673-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="93673-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93673-113">Requirements</span></span>



| <span data-ttu-id="93673-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="93673-114">Requirement</span></span> | <span data-ttu-id="93673-115">Valore</span><span class="sxs-lookup"><span data-stu-id="93673-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93673-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93673-116">Minimum supported client</span></span><br/> | <span data-ttu-id="93673-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93673-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="93673-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93673-118">Minimum supported server</span></span><br/> | <span data-ttu-id="93673-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93673-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="93673-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93673-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="93673-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93673-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93673-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93673-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93673-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="93673-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="93673-124">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="93673-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




