---
description: Generato da un sink del flusso quando completa la transizione allo stato interrotto. La transizione a stopped si verifica quando viene chiamato il metodo Stop IMFPresentationClock sul clock di presentazione dei sink.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Evento MEStreamSinkStopped (Mfobjects. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057852"
---
# <a name="mestreamsinkstopped-event"></a><span data-ttu-id="62744-104">Evento MEStreamSinkStopped</span><span class="sxs-lookup"><span data-stu-id="62744-104">MEStreamSinkStopped event</span></span>

<span data-ttu-id="62744-105">Generato da un sink del flusso quando completa la transizione allo stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="62744-105">Raised by a stream sink when it completes the transition to the stopped state.</span></span> <span data-ttu-id="62744-106">La transizione a stopped si verifica quando viene chiamato il metodo [**IMFPresentationClock:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) sul clock di presentazione del sink.</span><span class="sxs-lookup"><span data-stu-id="62744-106">The transition to stopped occurs when the [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="62744-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="62744-107">Event values</span></span>

<span data-ttu-id="62744-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="62744-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="62744-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="62744-109">VARTYPE</span></span>              | <span data-ttu-id="62744-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62744-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="62744-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="62744-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="62744-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="62744-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="62744-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62744-113">Requirements</span></span>



| <span data-ttu-id="62744-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="62744-114">Requirement</span></span> | <span data-ttu-id="62744-115">Valore</span><span class="sxs-lookup"><span data-stu-id="62744-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62744-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62744-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62744-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62744-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="62744-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62744-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62744-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="62744-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62744-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62744-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="62744-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62744-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62744-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62744-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62744-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62744-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="62744-124">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="62744-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




