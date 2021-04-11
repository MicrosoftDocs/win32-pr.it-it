---
description: Generato da un oggetto Enabler del contenuto quando viene completata l'azione di abilitazione degli oggetti.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130746"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="c2c6d-103">Evento MEEnablerCompleted</span><span class="sxs-lookup"><span data-stu-id="c2c6d-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="c2c6d-104">Generato da un oggetto Enabler del contenuto quando l'azione di abilitazione dell'oggetto viene completata.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="c2c6d-105">Gli oggetti che espongono l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) possono generare questo evento.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="c2c6d-106">L'evento viene generato se si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2c6d-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="c2c6d-107">Il metodo [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="c2c6d-108">Tramite l'applicazione viene chiamato [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), quindi l'applicazione completa la richiesta HTTP post, come descritto nel metodo **MonitorEnable** .</span><span class="sxs-lookup"><span data-stu-id="c2c6d-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="c2c6d-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="c2c6d-109">Event values</span></span>

<span data-ttu-id="c2c6d-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c2c6d-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c2c6d-111">VARTYPE</span></span>              | <span data-ttu-id="c2c6d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2c6d-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c2c6d-113">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="c2c6d-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c2c6d-114">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c2c6d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2c6d-115">Remarks</span></span>

<span data-ttu-id="c2c6d-116">Il codice di stato dell'evento può contenere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-116">The status code from the event may contain one of the following values.</span></span>



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c6d-117">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="c2c6d-117">**S\_OK**</span></span>                            | <span data-ttu-id="c2c6d-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-118">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="c2c6d-119">**NS \_ E \_ DRM \_ License \_ NOTACQUIRED**</span><span class="sxs-lookup"><span data-stu-id="c2c6d-119">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="c2c6d-120">La licenza DRM non è stata acquisita.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-120">The DRM license was not acquired.</span></span> <span data-ttu-id="c2c6d-121">Se il tentativo precedente usava [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), l'applicazione dovrebbe provare a eseguire un'acquisizione non invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-121">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="c2c6d-122">**\_monitoraggio DRM di NS è stato \_ \_ \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="c2c6d-122">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="c2c6d-123">L'operazione [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="c2c6d-123">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="c2c6d-124">Per ricevere questo evento, eseguire una query sull'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="c2c6d-124">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="c2c6d-125">Chiamare quindi [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), come descritto nell'argomento [generatori di eventi multimediali](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="c2c6d-125">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2c6d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2c6d-126">Requirements</span></span>



| <span data-ttu-id="c2c6d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2c6d-127">Requirement</span></span> | <span data-ttu-id="c2c6d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c2c6d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c6d-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2c6d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c6d-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2c6d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c2c6d-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2c6d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c6d-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2c6d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c2c6d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2c6d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2c6d-134"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2c6d-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2c6d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2c6d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c6d-136">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="c2c6d-136">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="c2c6d-137">Generatori di eventi multimediali</span><span class="sxs-lookup"><span data-stu-id="c2c6d-137">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="c2c6d-138">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c2c6d-138">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




