---
description: Generato da un sink del flusso per richiedere un nuovo campione multimediale dalla pipeline.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Evento MEStreamSinkRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c5afbfa9f0cfe4b320b451e699612a4729c23a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309606"
---
# <a name="mestreamsinkrequestsample-event"></a><span data-ttu-id="1b411-103">Evento MEStreamSinkRequestSample</span><span class="sxs-lookup"><span data-stu-id="1b411-103">MEStreamSinkRequestSample event</span></span>

<span data-ttu-id="1b411-104">Generato da un sink del flusso per richiedere un nuovo campione multimediale dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1b411-104">Raised by a stream sink to request a new media sample from the pipeline.</span></span> <span data-ttu-id="1b411-105">Per ogni evento MEStreamSinkRequestSample, la pipeline richiede i dati dal componente upstream successivo.</span><span class="sxs-lookup"><span data-stu-id="1b411-105">For each MEStreamSinkRequestSample event, the pipeline requests data from the next upstream component.</span></span>

## <a name="event-values"></a><span data-ttu-id="1b411-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="1b411-106">Event values</span></span>

<span data-ttu-id="1b411-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="1b411-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1b411-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1b411-108">VARTYPE</span></span>              | <span data-ttu-id="1b411-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b411-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="1b411-110">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="1b411-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="1b411-111">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1b411-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="1b411-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b411-112">Requirements</span></span>



| <span data-ttu-id="1b411-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b411-113">Requirement</span></span> | <span data-ttu-id="1b411-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1b411-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b411-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b411-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1b411-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b411-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1b411-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b411-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1b411-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b411-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b411-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b411-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b411-120"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b411-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b411-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b411-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b411-122">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1b411-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="1b411-123">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="1b411-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




