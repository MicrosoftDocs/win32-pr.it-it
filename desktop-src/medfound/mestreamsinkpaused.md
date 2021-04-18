---
description: Generato da un sink del flusso quando completa la transizione allo stato sospeso.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Evento MEStreamSinkPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315047"
---
# <a name="mestreamsinkpaused-event"></a><span data-ttu-id="e7023-103">Evento MEStreamSinkPaused</span><span class="sxs-lookup"><span data-stu-id="e7023-103">MEStreamSinkPaused event</span></span>

<span data-ttu-id="e7023-104">Generato da un sink del flusso quando completa la transizione allo stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="e7023-104">Raised by a stream sink when it completes the transition to the paused state.</span></span> <span data-ttu-id="e7023-105">La transizione a Paused si verifica quando viene chiamato il metodo [**IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) sul clock di presentazione del sink.</span><span class="sxs-lookup"><span data-stu-id="e7023-105">The transition to paused occurs when the [**IMFPresentationClock::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="e7023-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="e7023-106">Event values</span></span>

<span data-ttu-id="e7023-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7023-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e7023-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e7023-108">VARTYPE</span></span>              | <span data-ttu-id="e7023-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7023-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e7023-110">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="e7023-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e7023-111">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="e7023-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e7023-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7023-112">Requirements</span></span>



| <span data-ttu-id="e7023-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7023-113">Requirement</span></span> | <span data-ttu-id="e7023-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e7023-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7023-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7023-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e7023-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7023-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7023-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7023-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e7023-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7023-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7023-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7023-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7023-120"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7023-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7023-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7023-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7023-122">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7023-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e7023-123">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="e7023-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




