---
description: Inviato da una trasformazione di Media Foundation asincrona (MFT) in risposta a un \_ messaggio dell'indicatore del comando del messaggio MFT \_ \_ .
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309601"
---
# <a name="metransformmarker-event"></a><span data-ttu-id="e7fc2-103">Evento METransformMarker</span><span class="sxs-lookup"><span data-stu-id="e7fc2-103">METransformMarker event</span></span>

<span data-ttu-id="e7fc2-104">Inviato da una trasformazione di Media Foundation asincrona (MFT) in risposta a un messaggio dell' **\_ indicatore del \_ comando \_ del messaggio MFT** .</span><span class="sxs-lookup"><span data-stu-id="e7fc2-104">Sent by an asynchronous Media Foundation transform (MFT) in response to an **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span>

## <a name="event-values"></a><span data-ttu-id="e7fc2-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="e7fc2-105">Event values</span></span>

<span data-ttu-id="e7fc2-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e7fc2-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e7fc2-107">VARTYPE</span></span>              | <span data-ttu-id="e7fc2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7fc2-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="e7fc2-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="e7fc2-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e7fc2-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="e7fc2-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="e7fc2-111">Attributes</span></span>

<span data-ttu-id="e7fc2-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="e7fc2-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="e7fc2-113">Attribute</span></span>                                                      | <span data-ttu-id="e7fc2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7fc2-114">Description</span></span>                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7fc2-115">\_ \_ contesto MFT evento \_ MF</span><span class="sxs-lookup"><span data-stu-id="e7fc2-115">MF\_EVENT\_MFT\_CONTEXT</span></span>](mf-event-mft-context.md)<br/> | <span data-ttu-id="e7fc2-116">Il valore del parametro *ulParam* del messaggio del **\_ \_ \_ marcatore del comando del messaggio MFT** .</span><span class="sxs-lookup"><span data-stu-id="e7fc2-116">The value of the *ulParam* parameter from the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span><br/><span data-ttu-id="e7fc2-117">*Necessaria*</span><span class="sxs-lookup"><span data-stu-id="e7fc2-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e7fc2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7fc2-118">Remarks</span></span>

<span data-ttu-id="e7fc2-119">Il MFTs asincrono invia questo evento tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="e7fc2-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="e7fc2-120">MFTs sincroni non inviano mai questo evento.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="e7fc2-121">Il client di una MFT asincrona può inserire un marcatore nel flusso chiamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio **del \_ \_ \_ marcatore del comando del messaggio MFT** .</span><span class="sxs-lookup"><span data-stu-id="e7fc2-121">The client of an asynchronous MFT can place a marker in the stream by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span> <span data-ttu-id="e7fc2-122">Il parametro *ulParam* contiene dati definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-122">The *ulParam* parameter contains application-defined data.</span></span>

<span data-ttu-id="e7fc2-123">Al termine dell'elaborazione di tutti i dati di input disponibili al momento della chiamata [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , il MFT Accoda un evento METransformMarker.</span><span class="sxs-lookup"><span data-stu-id="e7fc2-123">When the MFT finishes processing all of the input data that was available at the time of the [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) call, the MFT queues an METransformMarker event.</span></span> <span data-ttu-id="e7fc2-124">L'attributo di [ \_ \_ \_ contesto MFT](mf-event-mft-context.md) dell'evento MF dell'evento contiene il valore del parametro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="e7fc2-124">The [MF\_EVENT\_MFT\_CONTEXT](mf-event-mft-context.md) attribute of the event contains the value of the *ulParam* parameter.</span></span> <span data-ttu-id="e7fc2-125">Per altre informazioni, vedere [MFTS asincrono](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="e7fc2-125">For more information, see [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7fc2-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7fc2-126">Requirements</span></span>



| <span data-ttu-id="e7fc2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7fc2-127">Requirement</span></span> | <span data-ttu-id="e7fc2-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e7fc2-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fc2-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7fc2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e7fc2-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7fc2-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e7fc2-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7fc2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e7fc2-132">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7fc2-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e7fc2-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7fc2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7fc2-134"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7fc2-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7fc2-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7fc2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7fc2-136">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7fc2-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e7fc2-137">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="e7fc2-137">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




