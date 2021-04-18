---
description: Inviato da una trasformazione di Media Foundation asincrona (MFT) quando sono disponibili nuovi dati di output dalla MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Evento METransformHaveOutput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307989"
---
# <a name="metransformhaveoutput-event"></a><span data-ttu-id="b3b17-103">Evento METransformHaveOutput</span><span class="sxs-lookup"><span data-stu-id="b3b17-103">METransformHaveOutput event</span></span>

<span data-ttu-id="b3b17-104">Inviato da una trasformazione di Media Foundation asincrona (MFT) quando sono disponibili nuovi dati di output dalla MFT.</span><span class="sxs-lookup"><span data-stu-id="b3b17-104">Sent by an asynchronous Media Foundation transform (MFT) when new output data is available from the MFT.</span></span>

## <a name="event-values"></a><span data-ttu-id="b3b17-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="b3b17-105">Event values</span></span>

<span data-ttu-id="b3b17-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3b17-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b3b17-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b3b17-107">VARTYPE</span></span>              | <span data-ttu-id="b3b17-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3b17-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="b3b17-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="b3b17-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b3b17-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b3b17-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="b3b17-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="b3b17-111">Attributes</span></span>

<span data-ttu-id="b3b17-112">Per questo evento non sono definiti attributi.</span><span class="sxs-lookup"><span data-stu-id="b3b17-112">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b17-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3b17-113">Remarks</span></span>

<span data-ttu-id="b3b17-114">Il MFTs asincrono invia questo evento tramite l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="b3b17-114">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="b3b17-115">MFTs sincroni non inviano mai questo evento.</span><span class="sxs-lookup"><span data-stu-id="b3b17-115">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="b3b17-116">Quando il client di MFT riceve questo evento, deve chiamare [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere l'output.</span><span class="sxs-lookup"><span data-stu-id="b3b17-116">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get the output.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3b17-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3b17-117">Requirements</span></span>



| <span data-ttu-id="b3b17-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b17-118">Requirement</span></span> | <span data-ttu-id="b3b17-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b3b17-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b17-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3b17-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3b17-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b3b17-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="b3b17-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3b17-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3b17-123">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3b17-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="b3b17-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3b17-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3b17-125"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3b17-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3b17-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3b17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b17-127">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3b17-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="b3b17-128">MFTs asincrono</span><span class="sxs-lookup"><span data-stu-id="b3b17-128">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




