---
description: Inviato da una trasformazione di Media Foundation asincrona (MFT) quando un'operazione di svuotamento è stata completata.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348746"
---
# <a name="metransformdraincomplete-event"></a><span data-ttu-id="9ffe2-103">Evento METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="9ffe2-103">METransformDrainComplete event</span></span>

<span data-ttu-id="9ffe2-104">Inviato da una trasformazione di Media Foundation asincrona (MFT) quando un'operazione di svuotamento è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-104">Sent by an asynchronous Media Foundation transform (MFT) when a drain operation is complete.</span></span>

## <a name="event-values"></a><span data-ttu-id="9ffe2-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="9ffe2-105">Event values</span></span>

<span data-ttu-id="9ffe2-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9ffe2-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9ffe2-107">VARTYPE</span></span>              | <span data-ttu-id="9ffe2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ffe2-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="9ffe2-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="9ffe2-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="9ffe2-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="9ffe2-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="9ffe2-111">Attributes</span></span>

<span data-ttu-id="9ffe2-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="9ffe2-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="9ffe2-113">Attribute</span></span>                                                                        | <span data-ttu-id="9ffe2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ffe2-114">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="9ffe2-115">ID del flusso di input per l' \_ evento \_ MFT MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ffe2-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="9ffe2-116">Identificatore del flusso che è stato svuotato.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-116">The identifier of the stream that was drained.</span></span><br/><span data-ttu-id="9ffe2-117">*Necessaria*</span><span class="sxs-lookup"><span data-stu-id="9ffe2-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9ffe2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ffe2-118">Remarks</span></span>

<span data-ttu-id="9ffe2-119">Il MFTs asincrono invia questo evento tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="9ffe2-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="9ffe2-120">MFTs sincroni non inviano mai questo evento.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="9ffe2-121">Per svuotare un MFT, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con il messaggio di **svuotamento del \_ \_ comando \_ del messaggio MFT** .</span><span class="sxs-lookup"><span data-stu-id="9ffe2-121">To drain an MFT, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_DRAIN** message.</span></span> <span data-ttu-id="9ffe2-122">Specificare il flusso di input da svuotare nel parametro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="9ffe2-122">Specify the input stream to drain in the *ulParam* parameter.</span></span> <span data-ttu-id="9ffe2-123">Al termine dell'operazione di svuotamento, un MFT asincrono invia l'evento METransformDrainComplete.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-123">When the drain operation is completed, an asynchronous MFT sends the METransformDrainComplete event.</span></span> <span data-ttu-id="9ffe2-124">L'attributo [MF \_ Event \_ MFT \_ input \_ Stream \_ ID](mf-event-mft-input-stream-id.md) dell'evento contiene l'identificatore di flusso specificato nel parametro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="9ffe2-124">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event contains the stream identifier given in the *ulParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ffe2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ffe2-125">Requirements</span></span>



| <span data-ttu-id="9ffe2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ffe2-126">Requirement</span></span> | <span data-ttu-id="9ffe2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9ffe2-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffe2-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ffe2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9ffe2-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9ffe2-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="9ffe2-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ffe2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9ffe2-131">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ffe2-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="9ffe2-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ffe2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ffe2-133"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ffe2-133"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ffe2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ffe2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffe2-135">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9ffe2-135">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="9ffe2-136">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="9ffe2-136">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




