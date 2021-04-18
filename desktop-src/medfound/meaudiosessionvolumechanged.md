---
description: Inviato dal renderer di streaming audio (SAR) quando cambia lo stato del volume o del silenziamento della sessione audio.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Evento MEAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308272"
---
# <a name="meaudiosessionvolumechanged-event"></a><span data-ttu-id="2e739-103">Evento MEAudioSessionVolumeChanged</span><span class="sxs-lookup"><span data-stu-id="2e739-103">MEAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="2e739-104">Inviato dal renderer di streaming audio (SAR) quando cambia lo stato del volume o del silenziamento della sessione audio.</span><span class="sxs-lookup"><span data-stu-id="2e739-104">Sent by the streaming audio renderer (SAR) when the volume or mute state of the audio session changes.</span></span>

<span data-ttu-id="2e739-105">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2e739-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="2e739-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="2e739-106">Event values</span></span>

<span data-ttu-id="2e739-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e739-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2e739-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2e739-108">VARTYPE</span></span>                | <span data-ttu-id="2e739-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e739-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e739-110">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="2e739-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="2e739-111">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="2e739-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="2e739-112">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="2e739-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="2e739-113">Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="2e739-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2e739-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e739-114">Remarks</span></span>

<span data-ttu-id="2e739-115">Questo evento viene generato dal sink di flusso del SAR.</span><span class="sxs-lookup"><span data-stu-id="2e739-115">This event is raised by the stream sink of the SAR.</span></span> <span data-ttu-id="2e739-116">L'evento viene generato quando il SAR riceve un evento [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) dalla sessione audio.</span><span class="sxs-lookup"><span data-stu-id="2e739-116">The event is triggered when the SAR receives an [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) event from the audio session.</span></span> <span data-ttu-id="2e739-117">Per ottenere il nuovo livello di volume e lo stato di silenziamento, chiamare [**IMFSimpleAudioVolume:: GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) e [**IMFSimpleAudioVolume:: getmute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span><span class="sxs-lookup"><span data-stu-id="2e739-117">To get the new volume level and mute state, call [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) and [**IMFSimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span></span>

<span data-ttu-id="2e739-118">Il SAR Invia questo evento se un'azione esterna modifica il volume, ad esempio se l'utente modifica il volume tramite il programma di controllo del volume di sistema (SndVol).</span><span class="sxs-lookup"><span data-stu-id="2e739-118">The SAR sends this event if an external action changes the volume—for example, if the user changes the volume through the system volume-control program (SndVol).</span></span> <span data-ttu-id="2e739-119">Il SAR non invia l'evento se l'applicazione modifica il volume direttamente sulla SAR.</span><span class="sxs-lookup"><span data-stu-id="2e739-119">The SAR does not send the event if the application changes the volume directly on the SAR.</span></span>

<span data-ttu-id="2e739-120">Inoltre, il SAR non invia questo evento quando il volume del canale cambia ([**IAudioSessionEvents:: OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span><span class="sxs-lookup"><span data-stu-id="2e739-120">Also, the SAR does not send this event when the channel volume changes ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e739-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e739-121">Requirements</span></span>



| <span data-ttu-id="2e739-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e739-122">Requirement</span></span> | <span data-ttu-id="2e739-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2e739-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e739-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e739-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2e739-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e739-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2e739-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e739-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2e739-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e739-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2e739-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e739-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e739-129"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e739-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e739-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e739-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e739-131">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2e739-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="2e739-132">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="2e739-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
