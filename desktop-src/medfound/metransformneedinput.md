---
description: Inviato da una trasformazione di Media Foundation asincrona (MFT) per richiedere un nuovo esempio di input.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129806"
---
# <a name="metransformneedinput-event"></a><span data-ttu-id="82b0c-103">Evento METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="82b0c-103">METransformNeedInput event</span></span>

<span data-ttu-id="82b0c-104">Inviato da una trasformazione di Media Foundation asincrona (MFT) per richiedere un nuovo esempio di input.</span><span class="sxs-lookup"><span data-stu-id="82b0c-104">Sent by an asynchronous Media Foundation transform (MFT) to request a new input sample.</span></span>

## <a name="event-values"></a><span data-ttu-id="82b0c-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="82b0c-105">Event values</span></span>

<span data-ttu-id="82b0c-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="82b0c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="82b0c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="82b0c-107">VARTYPE</span></span>              | <span data-ttu-id="82b0c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82b0c-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="82b0c-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="82b0c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="82b0c-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="82b0c-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="82b0c-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="82b0c-111">Attributes</span></span>

<span data-ttu-id="82b0c-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="82b0c-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="82b0c-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="82b0c-113">Attribute</span></span>                                                                        | <span data-ttu-id="82b0c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82b0c-114">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="82b0c-115">ID del flusso di input per l' \_ evento \_ MFT MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="82b0c-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="82b0c-116">Identificatore del flusso che necessita di dati di input.</span><span class="sxs-lookup"><span data-stu-id="82b0c-116">The identifier of the stream that needs input data.</span></span><br/><span data-ttu-id="82b0c-117">*Necessaria*</span><span class="sxs-lookup"><span data-stu-id="82b0c-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="82b0c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="82b0c-118">Remarks</span></span>

<span data-ttu-id="82b0c-119">Il MFTs asincrono invia questo evento tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="82b0c-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="82b0c-120">MFTs sincroni non inviano mai questo evento.</span><span class="sxs-lookup"><span data-stu-id="82b0c-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="82b0c-121">Quando il client di MFT riceve questo evento, deve chiamare [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) per recapitare l'esempio successivo.</span><span class="sxs-lookup"><span data-stu-id="82b0c-121">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) to deliver the next sample.</span></span> <span data-ttu-id="82b0c-122">L'attributo [MF \_ Event \_ MFT \_ input \_ Stream \_ ID](mf-event-mft-input-stream-id.md) dell'oggetto evento specifica il flusso di input che richiede i dati.</span><span class="sxs-lookup"><span data-stu-id="82b0c-122">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event object specifies which input stream requires data.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b0c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82b0c-123">Requirements</span></span>



| <span data-ttu-id="82b0c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="82b0c-124">Requirement</span></span> | <span data-ttu-id="82b0c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="82b0c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b0c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82b0c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="82b0c-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="82b0c-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="82b0c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82b0c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="82b0c-129">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="82b0c-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="82b0c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82b0c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b0c-131"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82b0c-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82b0c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82b0c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b0c-133">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="82b0c-133">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="82b0c-134">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="82b0c-134">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




