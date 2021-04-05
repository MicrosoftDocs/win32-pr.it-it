---
description: Generato dal renderer audio quando il nome visualizzato della sessione audio cambia.
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: Evento MEAudioSessionNameChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb06244c196ab55bbd93e12ebff6a6a394176cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752879"
---
# <a name="meaudiosessionnamechanged-event"></a><span data-ttu-id="25f12-103">Evento MEAudioSessionNameChanged</span><span class="sxs-lookup"><span data-stu-id="25f12-103">MEAudioSessionNameChanged event</span></span>

<span data-ttu-id="25f12-104">Generato dal renderer audio quando il nome visualizzato della sessione audio cambia.</span><span class="sxs-lookup"><span data-stu-id="25f12-104">Raised by the audio renderer when the audio session display name changes.</span></span>

<span data-ttu-id="25f12-105">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25f12-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="25f12-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="25f12-106">Event values</span></span>

<span data-ttu-id="25f12-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="25f12-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="25f12-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="25f12-108">VARTYPE</span></span>                | <span data-ttu-id="25f12-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25f12-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f12-110">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="25f12-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="25f12-111">Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="25f12-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="25f12-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="25f12-112">Remarks</span></span>

<span data-ttu-id="25f12-113">Questo evento viene inviato dal sink di flusso del renderer audio.</span><span class="sxs-lookup"><span data-stu-id="25f12-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="25f12-114">L'evento viene generato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) dalla sessione audio.</span><span class="sxs-lookup"><span data-stu-id="25f12-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) event from the audio session.</span></span>

<span data-ttu-id="25f12-115">Per ottenere il nuovo nome visualizzato, chiamare [**IMFAudioPolicy:: GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span><span class="sxs-lookup"><span data-stu-id="25f12-115">To get the new display name, call [**IMFAudioPolicy::GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span></span>

## <a name="requirements"></a><span data-ttu-id="25f12-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25f12-116">Requirements</span></span>



| <span data-ttu-id="25f12-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f12-117">Requirement</span></span> | <span data-ttu-id="25f12-118">Valore</span><span class="sxs-lookup"><span data-stu-id="25f12-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f12-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25f12-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25f12-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25f12-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="25f12-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25f12-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25f12-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25f12-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25f12-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25f12-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="25f12-124"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25f12-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f12-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25f12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f12-126">**IMFAudioPolicy:: GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="25f12-126">**IMFAudioPolicy::GetDisplayName**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[<span data-ttu-id="25f12-127">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25f12-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="25f12-128">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="25f12-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
