---
description: Segnala lo stato di avanzamento di un oggetto abilitatore del contenuto. Gli oggetti che espongono l'interfaccia IMFContentEnabler possono generare questo evento per notificare all'applicazione lo stato di avanzamento delle azioni di abilitazione del contenuto.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Evento MEEnablerProgress (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226665"
---
# <a name="meenablerprogress-event"></a><span data-ttu-id="41e3f-104">Evento MEEnablerProgress</span><span class="sxs-lookup"><span data-stu-id="41e3f-104">MEEnablerProgress event</span></span>

<span data-ttu-id="41e3f-105">Segnala lo stato di avanzamento di un oggetto abilitatore del contenuto.</span><span class="sxs-lookup"><span data-stu-id="41e3f-105">Signals the progress of a content enabler object.</span></span> <span data-ttu-id="41e3f-106">Gli oggetti che espongono l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) possono generare questo evento per notificare all'applicazione lo stato di avanzamento delle azioni del Content Enabler.</span><span class="sxs-lookup"><span data-stu-id="41e3f-106">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event to notify the application about the progress of the content enabler's actions.</span></span>

## <a name="event-values"></a><span data-ttu-id="41e3f-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="41e3f-107">Event values</span></span>

<span data-ttu-id="41e3f-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="41e3f-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="41e3f-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="41e3f-109">VARTYPE</span></span>               | <span data-ttu-id="41e3f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41e3f-110">Description</span></span>                                                               |
|-----------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="41e3f-111">\_LPWSTR VT</span><span class="sxs-lookup"><span data-stu-id="41e3f-111">VT\_LPWSTR</span></span><br/> | <span data-ttu-id="41e3f-112">Stringa di caratteri wide che descrive lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="41e3f-112">Wide-character string that describes the progress.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="41e3f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="41e3f-113">Remarks</span></span>

<span data-ttu-id="41e3f-114">Per ricevere questo evento, eseguire una query sull'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="41e3f-114">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="41e3f-115">Chiamare quindi [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), come descritto nell'argomento [generatori di eventi multimediali](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="41e3f-115">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41e3f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41e3f-116">Requirements</span></span>



| <span data-ttu-id="41e3f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="41e3f-117">Requirement</span></span> | <span data-ttu-id="41e3f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="41e3f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41e3f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41e3f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="41e3f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41e3f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41e3f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41e3f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="41e3f-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41e3f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41e3f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41e3f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="41e3f-124"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41e3f-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e3f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41e3f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e3f-126">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="41e3f-126">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="41e3f-127">Generatori di eventi multimediali</span><span class="sxs-lookup"><span data-stu-id="41e3f-127">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="41e3f-128">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41e3f-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




