---
description: Segnala che un'origine multimediale ha interrotto l'inserimento dei dati nel buffer.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Evento MEBufferingStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344301"
---
# <a name="mebufferingstopped-event"></a><span data-ttu-id="87e0d-103">Evento MEBufferingStopped</span><span class="sxs-lookup"><span data-stu-id="87e0d-103">MEBufferingStopped event</span></span>

<span data-ttu-id="87e0d-104">Segnala che un'origine multimediale ha interrotto l'inserimento dei dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="87e0d-104">Signals that a media source has stopped buffering data.</span></span>

<span data-ttu-id="87e0d-105">Un'origine multimediale Invia questo elemento quando interrompe il buffering dei dati dopo l'invio dell'evento [MEBufferingStarted](mebufferingstarted.md) .</span><span class="sxs-lookup"><span data-stu-id="87e0d-105">A media source sends this when it stops buffering data after sending the [MEBufferingStarted](mebufferingstarted.md) event.</span></span>

<span data-ttu-id="87e0d-106">Anche i flussi di byte che implementano l'interfaccia [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) inviano questo evento.</span><span class="sxs-lookup"><span data-stu-id="87e0d-106">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="87e0d-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="87e0d-107">Event values</span></span>

<span data-ttu-id="87e0d-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="87e0d-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="87e0d-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="87e0d-109">VARTYPE</span></span>              | <span data-ttu-id="87e0d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87e0d-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="87e0d-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="87e0d-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="87e0d-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="87e0d-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="87e0d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="87e0d-113">Remarks</span></span>

<span data-ttu-id="87e0d-114">Quando la sessione multimediale riceve questo evento, riavvia il clock di presentazione.</span><span class="sxs-lookup"><span data-stu-id="87e0d-114">When the Media Session receives this event, it restarts the presentation clock.</span></span> <span data-ttu-id="87e0d-115">La sessione multimediale trasmette inoltre l'evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="87e0d-115">The Media Session also forwards the event to the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e0d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87e0d-116">Requirements</span></span>



| <span data-ttu-id="87e0d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="87e0d-117">Requirement</span></span> | <span data-ttu-id="87e0d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="87e0d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87e0d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87e0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="87e0d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87e0d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="87e0d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87e0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="87e0d-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87e0d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87e0d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87e0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="87e0d-124"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87e0d-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e0d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87e0d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e0d-126">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87e0d-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




