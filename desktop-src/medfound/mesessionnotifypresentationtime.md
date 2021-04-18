---
description: Generato dalla sessione multimediale all'avvio di una nuova presentazione. Questo evento indica quando verrà avviata la presentazione e l'offset tra l'ora di presentazione e l'ora di origine.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Evento MESessionNotifyPresentationTime (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309614"
---
# <a name="mesessionnotifypresentationtime-event"></a><span data-ttu-id="be277-104">Evento MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="be277-104">MESessionNotifyPresentationTime event</span></span>

<span data-ttu-id="be277-105">Generato dalla sessione multimediale all'avvio di una nuova presentazione.</span><span class="sxs-lookup"><span data-stu-id="be277-105">Raised by the Media Session when a new presentation starts.</span></span> <span data-ttu-id="be277-106">Questo evento indica quando verrà avviata la presentazione e l'offset tra l'ora di presentazione e l'ora di origine.</span><span class="sxs-lookup"><span data-stu-id="be277-106">This event indicates when the presentation will start and the offset between the presentation time and the source time.</span></span>

## <a name="event-values"></a><span data-ttu-id="be277-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="be277-107">Event values</span></span>

<span data-ttu-id="be277-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="be277-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="be277-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="be277-109">VARTYPE</span></span>              | <span data-ttu-id="be277-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be277-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="be277-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="be277-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="be277-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="be277-112">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="be277-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="be277-113">Attributes</span></span>

<span data-ttu-id="be277-114">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="be277-114">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="be277-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="be277-115">Attribute</span></span>                                                                                                                   | <span data-ttu-id="be277-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be277-116">Description</span></span>                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be277-117">**\_ora di \_ presentazione di inizio evento \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="be277-117">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)<br/>                       | <span data-ttu-id="be277-118">Ora di inizio della presentazione.</span><span class="sxs-lookup"><span data-stu-id="be277-118">Starting time for the presentation.</span></span><br/> <br/>                                                      |
| [<span data-ttu-id="be277-119">**\_ \_ \_ offset ora presentazione evento \_ MF**</span><span class="sxs-lookup"><span data-stu-id="be277-119">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/>                     | <span data-ttu-id="be277-120">Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="be277-120">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/>                 |
| [<span data-ttu-id="be277-121">**\_ \_ \_ \_ ora di presentazione dell'avvio \_ dell'evento MF nell' \_ output**</span><span class="sxs-lookup"><span data-stu-id="be277-121">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md)<br/> | <span data-ttu-id="be277-122">Tempo di presentazione quando i sink del supporto eseguiranno il rendering del primo campione della nuova topologia.</span><span class="sxs-lookup"><span data-stu-id="be277-122">Presentation time when the media sinks will render the first sample of the new topology.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="be277-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be277-123">Requirements</span></span>



| <span data-ttu-id="be277-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="be277-124">Requirement</span></span> | <span data-ttu-id="be277-125">Valore</span><span class="sxs-lookup"><span data-stu-id="be277-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be277-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be277-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be277-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be277-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="be277-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be277-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be277-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be277-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="be277-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be277-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="be277-131"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be277-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be277-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be277-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be277-133">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="be277-133">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="be277-134">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be277-134">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




