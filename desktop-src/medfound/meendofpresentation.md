---
description: Generato da un'origine multimediale al termine di una presentazione. Questo evento segnala che tutti i flussi nella presentazione sono completati. La sessione multimediale trasmette questo evento all'applicazione.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Evento MEEndOfPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309647"
---
# <a name="meendofpresentation-event"></a><span data-ttu-id="1f72b-105">Evento MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="1f72b-105">MEEndOfPresentation event</span></span>

<span data-ttu-id="1f72b-106">Generato da un'origine multimediale al termine di una presentazione.</span><span class="sxs-lookup"><span data-stu-id="1f72b-106">Raised by a media source when a presentation ends.</span></span> <span data-ttu-id="1f72b-107">Questo evento segnala che tutti i flussi nella presentazione sono completati.</span><span class="sxs-lookup"><span data-stu-id="1f72b-107">This event signals that all streams in the presentation are complete.</span></span> <span data-ttu-id="1f72b-108">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1f72b-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="1f72b-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="1f72b-109">Event values</span></span>

<span data-ttu-id="1f72b-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f72b-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1f72b-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1f72b-111">VARTYPE</span></span>              | <span data-ttu-id="1f72b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f72b-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="1f72b-113">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="1f72b-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="1f72b-114">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1f72b-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="1f72b-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="1f72b-115">Attributes</span></span>

<span data-ttu-id="1f72b-116">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f72b-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="1f72b-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="1f72b-117">Attribute</span></span>                                                                                               | <span data-ttu-id="1f72b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f72b-118">Description</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f72b-119">**\_ \_ topologia di origine evento MF \_ \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="1f72b-119">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="1f72b-120">Specifica se l'origine del sequencer ha annullato la presentazione.</span><span class="sxs-lookup"><span data-stu-id="1f72b-120">Specifies whether the sequencer source canceled this presentation.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="1f72b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f72b-121">Requirements</span></span>



| <span data-ttu-id="1f72b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f72b-122">Requirement</span></span> | <span data-ttu-id="1f72b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1f72b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f72b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f72b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1f72b-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f72b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1f72b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f72b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1f72b-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f72b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1f72b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f72b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f72b-129"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f72b-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f72b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f72b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f72b-131">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f72b-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




