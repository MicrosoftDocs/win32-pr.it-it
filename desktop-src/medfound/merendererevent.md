---
description: Segnala un evento da un sink multimediale che esegue il rendering dei dati multimediali.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Evento MERendererEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226660"
---
# <a name="merendererevent-event"></a><span data-ttu-id="8aa9d-103">Evento MERendererEvent</span><span class="sxs-lookup"><span data-stu-id="8aa9d-103">MERendererEvent event</span></span>

<span data-ttu-id="8aa9d-104">Segnala un evento da un sink multimediale che esegue il rendering dei dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="8aa9d-104">Signals an event from a media sink that renders media data.</span></span>

<span data-ttu-id="8aa9d-105">Il [renderer video avanzato](enhanced-video-renderer.md) (EVR) Invia questo evento quando riceve un evento utente dal Presenter di EVR.</span><span class="sxs-lookup"><span data-stu-id="8aa9d-105">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) sends this event when it receives a user event from the EVR presenter.</span></span>

## <a name="event-values"></a><span data-ttu-id="8aa9d-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="8aa9d-106">Event values</span></span>

<span data-ttu-id="8aa9d-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="8aa9d-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8aa9d-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8aa9d-108">VARTYPE</span></span>           | <span data-ttu-id="8aa9d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8aa9d-109">Description</span></span>                        |
|-------------------|------------------------------------|
| <span data-ttu-id="8aa9d-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="8aa9d-110">VT\_I4</span></span><br/> | <span data-ttu-id="8aa9d-111">Codice evento.</span><span class="sxs-lookup"><span data-stu-id="8aa9d-111">Event code.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8aa9d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8aa9d-112">Remarks</span></span>

<span data-ttu-id="8aa9d-113">Se il relatore chiama il metodo **IMediaEventSink:: Notify** di EVR con un codice evento nell'intervallo EC \_ utente o superiore, EVR Invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="8aa9d-113">If the presenter calls the EVR's **IMediaEventSink::Notify** method with an event code in the range EC\_USER or higher, the EVR sends this event.</span></span> <span data-ttu-id="8aa9d-114">I dati dell'evento sono il codice evento passato al metodo **Notify** .</span><span class="sxs-lookup"><span data-stu-id="8aa9d-114">The event data is the event code that was passed to the **Notify** method.</span></span>

<span data-ttu-id="8aa9d-115">I parametri dell'evento originale (*EventParam1* e *EventParam2* nel metodo **IMediaEventSink:: Notify** ) vengono ignorati, quindi il Presenter deve impostare questi valori su **null**.</span><span class="sxs-lookup"><span data-stu-id="8aa9d-115">The original event parameters (*EventParam1* and *EventParam2* in the **IMediaEventSink::Notify** method) are ignored, so the presenter should set these values to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa9d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8aa9d-116">Requirements</span></span>



| <span data-ttu-id="8aa9d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa9d-117">Requirement</span></span> | <span data-ttu-id="8aa9d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8aa9d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa9d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aa9d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa9d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8aa9d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8aa9d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aa9d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa9d-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8aa9d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8aa9d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8aa9d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aa9d-124"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8aa9d-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa9d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8aa9d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa9d-126">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8aa9d-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




