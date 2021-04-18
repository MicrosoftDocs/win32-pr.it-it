---
description: Fornisce commenti e suggerimenti al responsabile qualità sulla qualità della riproduzione.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Evento MEQualityNotify (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528272"
---
# <a name="mequalitynotify-event"></a><span data-ttu-id="171c3-103">Evento MEQualityNotify</span><span class="sxs-lookup"><span data-stu-id="171c3-103">MEQualityNotify event</span></span>

<span data-ttu-id="171c3-104">Fornisce commenti e suggerimenti al responsabile qualità sulla qualità della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="171c3-104">Provides feedback to the quality manager about playback quality.</span></span>

## <a name="event-values"></a><span data-ttu-id="171c3-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="171c3-105">Event values</span></span>

<span data-ttu-id="171c3-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="171c3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="171c3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="171c3-107">VARTYPE</span></span>           | <span data-ttu-id="171c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171c3-108">Description</span></span>                         |
|-------------------|-------------------------------------|
| <span data-ttu-id="171c3-109">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="171c3-109">VT\_I8</span></span><br/> | <span data-ttu-id="171c3-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="171c3-110">See Remarks.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="171c3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="171c3-111">Remarks</span></span>

<span data-ttu-id="171c3-112">Questo evento viene generato da alcuni componenti della pipeline.</span><span class="sxs-lookup"><span data-stu-id="171c3-112">This event is raised by some pipeline components.</span></span> <span data-ttu-id="171c3-113">La sessione multimediale trasmette l'evento al gestore qualità chiamando il metodo [**IMFQualityManager:: NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .</span><span class="sxs-lookup"><span data-stu-id="171c3-113">The Media Session forwards the event to the quality manager by calling the [**IMFQualityManager::NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) method.</span></span>

<span data-ttu-id="171c3-114">Il tipo esteso dell'evento indica il significato dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="171c3-114">The event's extended type indicates the meaning of the event data.</span></span>



| <span data-ttu-id="171c3-115">Tipo esteso</span><span class="sxs-lookup"><span data-stu-id="171c3-115">Extended type</span></span>                            | <span data-ttu-id="171c3-116">Dati dell'evento</span><span class="sxs-lookup"><span data-stu-id="171c3-116">Event data</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171c3-117">\_ \_ \_ latenza di elaborazione \_ notifica MF qualità</span><span class="sxs-lookup"><span data-stu-id="171c3-117">MF\_QUALITY\_NOTIFY\_PROCESSING\_LATENCY</span></span> | <span data-ttu-id="171c3-118">Latenza di elaborazione approssimativa introdotta dal componente, in unità da 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="171c3-118">Approximate processing latency introduced by the component, in 100-nanosecond units.</span></span><br/> <span data-ttu-id="171c3-119">La latenza di elaborazione è la quantità di latenza introdotta da un componente nella pipeline mediante l'elaborazione di un esempio.</span><span class="sxs-lookup"><span data-stu-id="171c3-119">Processing latency is the amount of latency that a component introduces into the pipeline by processing a sample.</span></span> <span data-ttu-id="171c3-120">In alcuni casi, non è possibile derivare la latenza semplicemente esaminando le chiamate a [**IMFQualityManager:: NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) e [**IMFQualityManager:: NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span><span class="sxs-lookup"><span data-stu-id="171c3-120">In some cases, the latency cannot be derived simply by looking at the calls to [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) and [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput).</span></span> <span data-ttu-id="171c3-121">Ad esempio, potrebbe non essere presente una corrispondenza uno-a-uno tra gli esempi di input e di output.</span><span class="sxs-lookup"><span data-stu-id="171c3-121">For example, there may not be a one-to-one correspondence between input samples and output samples.</span></span> <span data-ttu-id="171c3-122">In questo caso, il componente potrebbe inviare un evento MEQualityNotify con la latenza di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="171c3-122">In this case, the component might send an MEQualityNotify event with the processing latency.</span></span> <span data-ttu-id="171c3-123">Se la latenza di elaborazione cambia, il componente può inviare un nuovo evento in qualsiasi momento durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="171c3-123">If the processing latency changes, the component can send a new event at any time during streaming.</span></span><br/> |
| <span data-ttu-id="171c3-124">\_ritardo di \_ esempio di notifica MF Quality \_ \_</span><span class="sxs-lookup"><span data-stu-id="171c3-124">MF\_QUALITY\_NOTIFY\_SAMPLE\_LAG</span></span>         | <span data-ttu-id="171c3-125">Tempo di ritardo per l'esempio, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="171c3-125">Lag time for the sample, in 100-nanosecond units.</span></span> <span data-ttu-id="171c3-126">Se il valore è positivo, l'esempio è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="171c3-126">If the value is positive, the sample was late.</span></span> <span data-ttu-id="171c3-127">Se il valore è negativo, il campione è stato anticipato.</span><span class="sxs-lookup"><span data-stu-id="171c3-127">If the value is negative, the sample was early.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="171c3-128">Per ottenere il tipo esteso, chiamare [**IMFMediaEvent:: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="171c3-128">To get the extended type, call [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

<span data-ttu-id="171c3-129">I componenti della pipeline non sono necessari per l'invio di questo evento.</span><span class="sxs-lookup"><span data-stu-id="171c3-129">Pipeline components are not required to send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="171c3-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="171c3-130">Requirements</span></span>



| <span data-ttu-id="171c3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="171c3-131">Requirement</span></span> | <span data-ttu-id="171c3-132">Valore</span><span class="sxs-lookup"><span data-stu-id="171c3-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171c3-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="171c3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="171c3-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="171c3-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="171c3-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="171c3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="171c3-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="171c3-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="171c3-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="171c3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="171c3-138"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="171c3-138"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="171c3-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="171c3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="171c3-140">**IMFQualityManager**</span><span class="sxs-lookup"><span data-stu-id="171c3-140">**IMFQualityManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[<span data-ttu-id="171c3-141">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="171c3-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




