---
description: Generato da un sink del flusso quando il tipo di supporto sink non è più valido.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Evento MEStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226652"
---
# <a name="mestreamsinkformatchanged-event"></a><span data-ttu-id="4db0c-103">Evento MEStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="4db0c-103">MEStreamSinkFormatChanged event</span></span>

<span data-ttu-id="4db0c-104">Generato da un sink del flusso quando il tipo di supporto del sink non è più valido.</span><span class="sxs-lookup"><span data-stu-id="4db0c-104">Raised by a stream sink when the sink's media type is no longer valid.</span></span>

## <a name="event-values"></a><span data-ttu-id="4db0c-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="4db0c-105">Event values</span></span>

<span data-ttu-id="4db0c-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="4db0c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4db0c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4db0c-107">VARTYPE</span></span>              | <span data-ttu-id="4db0c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4db0c-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4db0c-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="4db0c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4db0c-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4db0c-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4db0c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4db0c-111">Remarks</span></span>

<span data-ttu-id="4db0c-112">Un sink di flusso può generare questa situazione anche se si verifica un evento che invalida il tipo di supporto del sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="4db0c-112">A stream sink can raise this even if something happens that invalidates the stream sink's media type.</span></span> <span data-ttu-id="4db0c-113">Ad esempio, il renderer video avanzato (EVR) Invia questo evento quando cambia la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4db0c-113">For example, the enhanced video renderer (EVR) sends this event when the display changes.</span></span>

<span data-ttu-id="4db0c-114">Il valore **HRESULT** recuperato da [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) potrebbe indicare il motivo per cui il tipo di supporto non è più valido.</span><span class="sxs-lookup"><span data-stu-id="4db0c-114">The **HRESULT** value retrieved by [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) might indicate why the media type is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db0c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4db0c-115">Requirements</span></span>



| <span data-ttu-id="4db0c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4db0c-116">Requirement</span></span> | <span data-ttu-id="4db0c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4db0c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db0c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4db0c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4db0c-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4db0c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4db0c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4db0c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4db0c-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4db0c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4db0c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4db0c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4db0c-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4db0c-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db0c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4db0c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db0c-125">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4db0c-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4db0c-126">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="4db0c-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




