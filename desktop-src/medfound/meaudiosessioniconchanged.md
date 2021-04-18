---
description: Generato dal renderer audio quando viene modificata l'icona della sessione audio.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Evento MEAudioSessionIconChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308274"
---
# <a name="meaudiosessioniconchanged-event"></a><span data-ttu-id="36bac-103">Evento MEAudioSessionIconChanged</span><span class="sxs-lookup"><span data-stu-id="36bac-103">MEAudioSessionIconChanged event</span></span>

<span data-ttu-id="36bac-104">Generato dal renderer audio quando viene modificata l'icona della sessione audio.</span><span class="sxs-lookup"><span data-stu-id="36bac-104">Raised by the audio renderer when the audio session icon changes.</span></span>

<span data-ttu-id="36bac-105">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="36bac-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="36bac-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="36bac-106">Event values</span></span>

<span data-ttu-id="36bac-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="36bac-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="36bac-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="36bac-108">VARTYPE</span></span>                | <span data-ttu-id="36bac-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36bac-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="36bac-110">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="36bac-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="36bac-111">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="36bac-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="36bac-112">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="36bac-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="36bac-113">Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="36bac-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="36bac-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="36bac-114">Remarks</span></span>

<span data-ttu-id="36bac-115">Questo evento viene inviato dal sink di flusso del renderer audio.</span><span class="sxs-lookup"><span data-stu-id="36bac-115">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="36bac-116">L'evento viene generato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) dalla sessione audio.</span><span class="sxs-lookup"><span data-stu-id="36bac-116">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) event from the audio session.</span></span>

<span data-ttu-id="36bac-117">Per ottenere l'icona nuova, chiamare [**IMFAudioPolicy:: GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span><span class="sxs-lookup"><span data-stu-id="36bac-117">To get the new icon, call [**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span></span>

## <a name="requirements"></a><span data-ttu-id="36bac-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36bac-118">Requirements</span></span>



| <span data-ttu-id="36bac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="36bac-119">Requirement</span></span> | <span data-ttu-id="36bac-120">Valore</span><span class="sxs-lookup"><span data-stu-id="36bac-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36bac-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36bac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36bac-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36bac-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="36bac-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36bac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36bac-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36bac-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36bac-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36bac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="36bac-126"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36bac-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36bac-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36bac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36bac-128">**IMFAudioPolicy::GetIconPath**</span><span class="sxs-lookup"><span data-stu-id="36bac-128">**IMFAudioPolicy::GetIconPath**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[<span data-ttu-id="36bac-129">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36bac-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="36bac-130">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="36bac-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
