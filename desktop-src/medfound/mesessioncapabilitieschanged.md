---
description: Generato dalla sessione multimediale quando le funzionalità della sessione cambiano.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Evento MESessionCapabilitiesChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309617"
---
# <a name="mesessioncapabilitieschanged-event"></a><span data-ttu-id="53007-103">Evento MESessionCapabilitiesChanged</span><span class="sxs-lookup"><span data-stu-id="53007-103">MESessionCapabilitiesChanged event</span></span>

<span data-ttu-id="53007-104">Generato dalla sessione multimediale quando le funzionalità della sessione cambiano.</span><span class="sxs-lookup"><span data-stu-id="53007-104">Raised by the Media Session when the session capabilities change.</span></span>

## <a name="event-values"></a><span data-ttu-id="53007-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="53007-105">Event values</span></span>

<span data-ttu-id="53007-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="53007-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="53007-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="53007-107">VARTYPE</span></span>              | <span data-ttu-id="53007-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53007-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="53007-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="53007-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="53007-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="53007-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="53007-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="53007-111">Remarks</span></span>

<span data-ttu-id="53007-112">L'evento contiene gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="53007-112">The event contains the following attributes.</span></span>



| <span data-ttu-id="53007-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="53007-113">Attribute</span></span>                                                                     | <span data-ttu-id="53007-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53007-114">Description</span></span>                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="53007-115">**\_SESSIONCAPS evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="53007-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)              | <span data-ttu-id="53007-116">Nuovi flag delle funzionalità della sessione.</span><span class="sxs-lookup"><span data-stu-id="53007-116">New session capabilities flags.</span></span>                  |
| [<span data-ttu-id="53007-117">**\_ \_ Delta SESSIONCAPS evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="53007-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md) | <span data-ttu-id="53007-118">Indica quali flag delle funzionalità sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="53007-118">Indicates which capabilities flags have changed.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="53007-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53007-119">Requirements</span></span>



| <span data-ttu-id="53007-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="53007-120">Requirement</span></span> | <span data-ttu-id="53007-121">Valore</span><span class="sxs-lookup"><span data-stu-id="53007-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53007-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53007-122">Minimum supported client</span></span><br/> | <span data-ttu-id="53007-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53007-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53007-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53007-124">Minimum supported server</span></span><br/> | <span data-ttu-id="53007-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53007-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53007-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53007-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="53007-127"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53007-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53007-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53007-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53007-129">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53007-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




