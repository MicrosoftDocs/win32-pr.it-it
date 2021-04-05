---
description: Generato da un sink del flusso quando il flusso ha ricevuto un numero sufficiente di dati di pre-roll per avviare il rendering. Questo evento viene generato dai sink di supporto che supportano l'interfaccia IMFMediaSinkPreroll.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Evento MEStreamSinkPrerolled (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754290"
---
# <a name="mestreamsinkprerolled-event"></a><span data-ttu-id="58529-104">Evento MEStreamSinkPrerolled</span><span class="sxs-lookup"><span data-stu-id="58529-104">MEStreamSinkPrerolled event</span></span>

<span data-ttu-id="58529-105">Generato da un sink del flusso quando il flusso ha ricevuto un numero sufficiente di dati di pre-roll per avviare il rendering.</span><span class="sxs-lookup"><span data-stu-id="58529-105">Raised by a stream sink when the stream has received enough pre-roll data to begin rendering.</span></span> <span data-ttu-id="58529-106">Questo evento viene generato dai sink di supporto che supportano l'interfaccia [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="58529-106">This event is raised by media sinks that support the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="58529-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="58529-107">Event values</span></span>

<span data-ttu-id="58529-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="58529-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="58529-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="58529-109">VARTYPE</span></span>              | <span data-ttu-id="58529-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58529-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="58529-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="58529-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="58529-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="58529-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="58529-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58529-113">Requirements</span></span>



| <span data-ttu-id="58529-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="58529-114">Requirement</span></span> | <span data-ttu-id="58529-115">Valore</span><span class="sxs-lookup"><span data-stu-id="58529-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58529-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58529-116">Minimum supported client</span></span><br/> | <span data-ttu-id="58529-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58529-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58529-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58529-118">Minimum supported server</span></span><br/> | <span data-ttu-id="58529-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58529-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58529-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58529-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="58529-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58529-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58529-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58529-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58529-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58529-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="58529-124">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="58529-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




