---
description: Inviato da un flusso di byte quando le caratteristiche del flusso di byte sono state modificate.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Evento MEByteStreamCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308742"
---
# <a name="mebytestreamcharacteristicschanged-event"></a><span data-ttu-id="06c97-103">Evento MEByteStreamCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="06c97-103">MEByteStreamCharacteristicsChanged event</span></span>

<span data-ttu-id="06c97-104">Inviato da un flusso di byte quando le caratteristiche del flusso di byte sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="06c97-104">Sent by a byte stream when the characteristics of the byte stream have changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="06c97-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="06c97-105">Event values</span></span>

<span data-ttu-id="06c97-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="06c97-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="06c97-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="06c97-107">VARTYPE</span></span>               | <span data-ttu-id="06c97-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06c97-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="06c97-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="06c97-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="06c97-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="06c97-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="06c97-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="06c97-111">Remarks</span></span>

<span data-ttu-id="06c97-112">Questo evento indica che sono state modificate una o più delle seguenti caratteristiche:</span><span class="sxs-lookup"><span data-stu-id="06c97-112">This event indicates that one or more of the following characteristics has changed:</span></span>

-   <span data-ttu-id="06c97-113">Flag funzionalità ([**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span><span class="sxs-lookup"><span data-stu-id="06c97-113">Capability flags ([**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span></span>
-   <span data-ttu-id="06c97-114">Flag di fine flusso ([**IMFByteStream:: IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span><span class="sxs-lookup"><span data-stu-id="06c97-114">End-of-stream flag ([**IMFByteStream::IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span></span>
-   <span data-ttu-id="06c97-115">Lunghezza ([**IMFByteStream:: GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span><span class="sxs-lookup"><span data-stu-id="06c97-115">Length ([**IMFByteStream::GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span></span>

<span data-ttu-id="06c97-116">Non tutte le implementazioni di [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) supportano questo evento.</span><span class="sxs-lookup"><span data-stu-id="06c97-116">Not all [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) implementations support this event.</span></span> <span data-ttu-id="06c97-117">Per ricevere l'evento, eseguire una query sull'oggetto flusso di byte per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="06c97-117">To receive the event, query the byte-stream object for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c97-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06c97-118">Requirements</span></span>



| <span data-ttu-id="06c97-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c97-119">Requirement</span></span> | <span data-ttu-id="06c97-120">Valore</span><span class="sxs-lookup"><span data-stu-id="06c97-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c97-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="06c97-122">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="06c97-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="06c97-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="06c97-124">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="06c97-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06c97-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06c97-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c97-126"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06c97-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c97-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06c97-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c97-128">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="06c97-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




