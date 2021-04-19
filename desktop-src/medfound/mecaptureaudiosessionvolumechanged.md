---
description: Inviato da un'origine di acquisizione audio quando cambia il volume.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Evento MECaptureAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308473"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a><span data-ttu-id="85c8a-103">Evento MECaptureAudioSessionVolumeChanged</span><span class="sxs-lookup"><span data-stu-id="85c8a-103">MECaptureAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="85c8a-104">Inviato da un'origine di acquisizione audio quando cambia il volume.</span><span class="sxs-lookup"><span data-stu-id="85c8a-104">Sent by an audio capture source when the volume changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="85c8a-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="85c8a-105">Event values</span></span>

<span data-ttu-id="85c8a-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="85c8a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="85c8a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="85c8a-107">VARTYPE</span></span>               | <span data-ttu-id="85c8a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85c8a-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="85c8a-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="85c8a-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="85c8a-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="85c8a-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="85c8a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="85c8a-111">Remarks</span></span>

<span data-ttu-id="85c8a-112">Questo evento viene inviato dal flusso multimediale dell'origine di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="85c8a-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="85c8a-113">L'origine di acquisizione audio Invia questo evento se un'azione esterna modifica il volume, ad esempio se l'utente modifica il volume tramite il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="85c8a-113">The audio capture source sends this event if an external action changes the volume—for example, if the user changes the volume through the Control Panel.</span></span> <span data-ttu-id="85c8a-114">L'origine di acquisizione non invia l'evento se l'applicazione modifica il volume direttamente nell'origine.</span><span class="sxs-lookup"><span data-stu-id="85c8a-114">The capture source does not send the event if the application changes the volume directly on the source.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c8a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85c8a-115">Requirements</span></span>



| <span data-ttu-id="85c8a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c8a-116">Requirement</span></span> | <span data-ttu-id="85c8a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="85c8a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c8a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85c8a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85c8a-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="85c8a-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="85c8a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85c8a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85c8a-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="85c8a-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="85c8a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85c8a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="85c8a-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85c8a-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c8a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85c8a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c8a-125">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="85c8a-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




