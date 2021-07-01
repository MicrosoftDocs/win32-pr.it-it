---
description: Generato da un oggetto di abilitazione del contenuto quando l'azione di abilitazione degli oggetti viene completata.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05459a648f6b357fd483baa9fc56809540e64a1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119446"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="951f1-103">Evento MEEnablerCompleted</span><span class="sxs-lookup"><span data-stu-id="951f1-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="951f1-104">Generato da un oggetto content enabler quando viene completata l'azione di abilitazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="951f1-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="951f1-105">Gli oggetti che espongono [**l'interfaccia IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) possono generare questo evento.</span><span class="sxs-lookup"><span data-stu-id="951f1-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="951f1-106">L'evento viene generato se si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="951f1-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="951f1-107">Il [**metodo IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="951f1-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="951f1-108">L'applicazione chiama [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)e quindi l'applicazione completa la richiesta HTTP POST, come descritto nel **metodo MonitorEnable.**</span><span class="sxs-lookup"><span data-stu-id="951f1-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="951f1-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="951f1-109">Event values</span></span>

<span data-ttu-id="951f1-110">I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="951f1-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="951f1-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="951f1-111">VARTYPE</span></span>              | <span data-ttu-id="951f1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="951f1-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="951f1-113">VT \_ EMPTY</span><span class="sxs-lookup"><span data-stu-id="951f1-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="951f1-114">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="951f1-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="951f1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="951f1-115">Remarks</span></span>

<span data-ttu-id="951f1-116">Il codice di stato dell'evento può contenere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="951f1-116">The status code from the event may contain one of the following values.</span></span>



| <span data-ttu-id="951f1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="951f1-117">Value</span></span>                                     | <span data-ttu-id="951f1-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="951f1-118">Description</span></span>                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="951f1-119">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="951f1-119">**S\_OK**</span></span>                            | <span data-ttu-id="951f1-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="951f1-120">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="951f1-121">**LICENZA \_ NS E \_ DRM \_ NON \_ RICHIESTA**</span><span class="sxs-lookup"><span data-stu-id="951f1-121">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="951f1-122">La licenza DRM non è stata acquisita.</span><span class="sxs-lookup"><span data-stu-id="951f1-122">The DRM license was not acquired.</span></span> <span data-ttu-id="951f1-123">Se il tentativo precedente usa [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), l'applicazione deve provare l'acquisizione non invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="951f1-123">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="951f1-124">**MONITORAGGIO \_ \_ DRM S \_ NS \_ ANNULLATO**</span><span class="sxs-lookup"><span data-stu-id="951f1-124">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="951f1-125">[**L'operazione MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="951f1-125">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="951f1-126">Per ricevere questo evento, eseguire una query [**sull'interfaccia IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) per [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)</span><span class="sxs-lookup"><span data-stu-id="951f1-126">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="951f1-127">Chiamare quindi [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), come descritto nell'argomento [Generatori di eventi multimediali](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="951f1-127">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="951f1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="951f1-128">Requirements</span></span>



| <span data-ttu-id="951f1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="951f1-129">Requirement</span></span> | <span data-ttu-id="951f1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="951f1-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="951f1-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="951f1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="951f1-132">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="951f1-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="951f1-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="951f1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="951f1-134">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="951f1-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="951f1-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="951f1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="951f1-136"><dt>Mfobjects.h (includere Mfidl.h)</dt></span><span class="sxs-lookup"><span data-stu-id="951f1-136"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="951f1-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="951f1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951f1-138">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="951f1-138">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="951f1-139">Generatori di eventi multimediali</span><span class="sxs-lookup"><span data-stu-id="951f1-139">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="951f1-140">Media Foundation eventi</span><span class="sxs-lookup"><span data-stu-id="951f1-140">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




