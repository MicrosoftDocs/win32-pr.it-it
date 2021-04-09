---
description: 'Generato quando il metodo IMFMediaSession:: Start viene completato in modo asincrono.'
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: Evento MESessionStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9510fb5f5dda3d14b916ed40dcba4ca05800b52b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049720"
---
# <a name="mesessionstarted-event"></a><span data-ttu-id="e4b59-103">Evento MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="e4b59-103">MESessionStarted event</span></span>

<span data-ttu-id="e4b59-104">Generato quando il metodo [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e4b59-104">Raised when the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="e4b59-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="e4b59-105">Event values</span></span>

<span data-ttu-id="e4b59-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4b59-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e4b59-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e4b59-107">VARTYPE</span></span>              | <span data-ttu-id="e4b59-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4b59-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e4b59-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="e4b59-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e4b59-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="e4b59-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="e4b59-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="e4b59-111">Attributes</span></span>

<span data-ttu-id="e4b59-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4b59-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="e4b59-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="e4b59-113">Attribute</span></span>                                                                                               | <span data-ttu-id="e4b59-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4b59-114">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4b59-115">**\_ \_ \_ offset ora presentazione evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="e4b59-115">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/> | <span data-ttu-id="e4b59-116">Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="e4b59-116">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e4b59-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4b59-117">Requirements</span></span>



| <span data-ttu-id="e4b59-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b59-118">Requirement</span></span> | <span data-ttu-id="e4b59-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e4b59-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b59-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4b59-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b59-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4b59-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e4b59-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4b59-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b59-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4b59-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e4b59-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4b59-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b59-125"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b59-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b59-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4b59-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b59-127">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4b59-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




