---
description: Generato dall'origine del sequencer quando un segmento viene completato ed è seguito da un altro segmento. Al termine del segmento finale, l'origine del sequencer genera un evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880265"
---
# <a name="meendofpresentationsegment-event"></a><span data-ttu-id="d0718-104">Evento MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="d0718-104">MEEndOfPresentationSegment event</span></span>

<span data-ttu-id="d0718-105">Generato dall'origine del sequencer quando un segmento viene completato ed è seguito da un altro segmento.</span><span class="sxs-lookup"><span data-stu-id="d0718-105">Raised by the sequencer source when a segment is completed and is followed by another segment.</span></span> <span data-ttu-id="d0718-106">Al termine del segmento finale, l'origine del sequencer genera un evento [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="d0718-106">When the final segment is completed, the sequencer source raises an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

<span data-ttu-id="d0718-107">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d0718-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="d0718-108">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="d0718-108">Event values</span></span>

<span data-ttu-id="d0718-109">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0718-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d0718-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d0718-110">VARTYPE</span></span>              | <span data-ttu-id="d0718-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0718-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d0718-112">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="d0718-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d0718-113">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d0718-113">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="d0718-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="d0718-114">Attributes</span></span>

<span data-ttu-id="d0718-115">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0718-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="d0718-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="d0718-116">Attribute</span></span>                                                                                               | <span data-ttu-id="d0718-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0718-117">Description</span></span>                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0718-118">**\_ \_ topologia di origine evento MF \_ \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="d0718-118">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="d0718-119">Specifica se l'origine del sequencer ha annullato il segmento.</span><span class="sxs-lookup"><span data-stu-id="d0718-119">Specifies whether the sequencer source canceled this segment.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d0718-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0718-120">Requirements</span></span>



| <span data-ttu-id="d0718-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0718-121">Requirement</span></span> | <span data-ttu-id="d0718-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d0718-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0718-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0718-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d0718-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0718-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d0718-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0718-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d0718-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d0718-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0718-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0718-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0718-128"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0718-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0718-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0718-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0718-130">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0718-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="d0718-131">Informazioni sull'origine del sequencer</span><span class="sxs-lookup"><span data-stu-id="d0718-131">About the Sequencer Source</span></span>](about-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="d0718-132">Eventi di origine di Sequencer</span><span class="sxs-lookup"><span data-stu-id="d0718-132">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




