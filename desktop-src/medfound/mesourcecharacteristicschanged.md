---
description: Generato da un'origine multimediale quando le caratteristiche delle origini cambiano.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Evento MESourceCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309612"
---
# <a name="mesourcecharacteristicschanged-event"></a><span data-ttu-id="5fc43-103">Evento MESourceCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="5fc43-103">MESourceCharacteristicsChanged event</span></span>

<span data-ttu-id="5fc43-104">Generato da un'origine multimediale quando le caratteristiche dell'origine cambiano.</span><span class="sxs-lookup"><span data-stu-id="5fc43-104">Raised by a media source when the source's characteristics change.</span></span>

## <a name="event-values"></a><span data-ttu-id="5fc43-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="5fc43-105">Event values</span></span>

<span data-ttu-id="5fc43-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="5fc43-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5fc43-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5fc43-107">VARTYPE</span></span>              | <span data-ttu-id="5fc43-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fc43-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5fc43-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="5fc43-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5fc43-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5fc43-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="5fc43-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="5fc43-111">Attributes</span></span>

<span data-ttu-id="5fc43-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="5fc43-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="5fc43-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="5fc43-113">Attribute</span></span>                                                                                                   | <span data-ttu-id="5fc43-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fc43-114">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="5fc43-115">**\_caratteristiche dell' \_ origine \_ evento MF**</span><span class="sxs-lookup"><span data-stu-id="5fc43-115">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)<br/>          | <span data-ttu-id="5fc43-116">Nuove caratteristiche dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="5fc43-116">New characteristics of the media source.</span></span><br/> <br/>      |
| [<span data-ttu-id="5fc43-117">**\_ \_ caratteristiche origine evento \_ MF \_ obsolete**</span><span class="sxs-lookup"><span data-stu-id="5fc43-117">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)<br/> | <span data-ttu-id="5fc43-118">Caratteristiche precedenti dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="5fc43-118">Previous characteristics of the media source.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5fc43-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fc43-119">Requirements</span></span>



| <span data-ttu-id="5fc43-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc43-120">Requirement</span></span> | <span data-ttu-id="5fc43-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5fc43-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc43-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fc43-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc43-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fc43-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5fc43-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fc43-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc43-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5fc43-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5fc43-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fc43-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc43-127"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fc43-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc43-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fc43-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc43-129">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="5fc43-129">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[<span data-ttu-id="5fc43-130">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5fc43-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




