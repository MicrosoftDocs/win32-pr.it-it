---
description: Generato quando un sink multimediale diventa non valido.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Evento MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226272"
---
# <a name="mesinkinvalidated-event"></a><span data-ttu-id="16639-103">Evento MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="16639-103">MESinkInvalidated event</span></span>

<span data-ttu-id="16639-104">Generato quando un sink multimediale diventa non valido.</span><span class="sxs-lookup"><span data-stu-id="16639-104">Raised when a media sink becomes invalid.</span></span>

## <a name="event-values"></a><span data-ttu-id="16639-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="16639-105">Event values</span></span>

<span data-ttu-id="16639-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="16639-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="16639-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="16639-107">VARTYPE</span></span>              | <span data-ttu-id="16639-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16639-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="16639-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="16639-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="16639-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="16639-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="16639-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="16639-111">Attributes</span></span>

<span data-ttu-id="16639-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="16639-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="16639-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="16639-113">Attribute</span></span>                                                                    | <span data-ttu-id="16639-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16639-114">Description</span></span>                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="16639-115">**\_nodo di \_ output \_ evento MF**</span><span class="sxs-lookup"><span data-stu-id="16639-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="16639-116">Identifica il nodo della topologia per questo sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="16639-116">Identifies the topology node for this media sink.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="16639-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="16639-117">Remarks</span></span>

<span data-ttu-id="16639-118">La sessione multimediale genera questo evento se riceve uno qualsiasi degli eventi seguenti dal sink multimediale:</span><span class="sxs-lookup"><span data-stu-id="16639-118">The Media Session raises this event if it receives any of the following events from the media sink:</span></span>

-   [<span data-ttu-id="16639-119">MEAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="16639-119">MEAudioSessionDeviceRemoved</span></span>](meaudiosessiondeviceremoved.md)

-   [<span data-ttu-id="16639-120">MEAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="16639-120">MEAudioSessionDisconnected</span></span>](meaudiosessiondisconnected.md)

-   [<span data-ttu-id="16639-121">MEAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="16639-121">MEAudioSessionExclusiveModeOverride</span></span>](meaudiosessionexclusivemodeoverride.md)

-   [<span data-ttu-id="16639-122">MEAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="16639-122">MEAudioSessionFormatChanged</span></span>](meaudiosessionformatchanged.md)

-   [<span data-ttu-id="16639-123">MEAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="16639-123">MEAudioSessionServerShutdown</span></span>](meaudiosessionservershutdown.md)

<span data-ttu-id="16639-124">Un sink multimediale può anche generare questo evento, nel qual caso la sessione multimediale imposta l'attributo del [**\_ \_ \_ nodo di output eventi MF**](mf-event-output-node-attribute.md) nell'evento e lo trasmette all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="16639-124">A media sink can also raise this event, in which case the Media Session sets the [**MF\_EVENT\_OUTPUT\_NODE**](mf-event-output-node-attribute.md) attribute on the event and forwards the event to the application.</span></span>

<span data-ttu-id="16639-125">Se l'applicazione riceve questo evento, deve ricreare il sink multimediale e accodare nuovamente la topologia.</span><span class="sxs-lookup"><span data-stu-id="16639-125">If the application receives this event, it needs to recreate the media sink and queue the topology again.</span></span>

## <a name="requirements"></a><span data-ttu-id="16639-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16639-126">Requirements</span></span>



| <span data-ttu-id="16639-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="16639-127">Requirement</span></span> | <span data-ttu-id="16639-128">Valore</span><span class="sxs-lookup"><span data-stu-id="16639-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16639-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16639-129">Minimum supported client</span></span><br/> | <span data-ttu-id="16639-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16639-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="16639-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16639-131">Minimum supported server</span></span><br/> | <span data-ttu-id="16639-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16639-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16639-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16639-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="16639-134"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16639-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16639-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16639-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16639-136">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="16639-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




