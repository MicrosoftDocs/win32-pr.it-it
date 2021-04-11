---
description: Generato dal renderer audio quando la sessione audio viene superata da una connessione in modalità esclusiva. Il renderer audio non è ora valido.
ms.assetid: f89acfe4-14a7-4051-a816-e5e0ba8db80a
title: Evento MEAudioSessionExclusiveModeOverride (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3732be3fec73e3e948f6093187f32dd46839bea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226335"
---
# <a name="meaudiosessionexclusivemodeoverride-event"></a><span data-ttu-id="4fceb-104">Evento MEAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="4fceb-104">MEAudioSessionExclusiveModeOverride event</span></span>

<span data-ttu-id="4fceb-105">Generato dal renderer audio quando la sessione audio viene superata da una connessione in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="4fceb-105">Raised by the audio renderer when the audio session is preempted by an exclusive-mode connection.</span></span> <span data-ttu-id="4fceb-106">Il renderer audio non è ora valido.</span><span class="sxs-lookup"><span data-stu-id="4fceb-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="4fceb-107">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4fceb-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="4fceb-108">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="4fceb-108">Event values</span></span>

<span data-ttu-id="4fceb-109">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="4fceb-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4fceb-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4fceb-110">VARTYPE</span></span>                | <span data-ttu-id="4fceb-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fceb-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fceb-112">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="4fceb-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="4fceb-113">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4fceb-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="4fceb-114">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="4fceb-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="4fceb-115">Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="4fceb-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4fceb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fceb-116">Remarks</span></span>

<span data-ttu-id="4fceb-117">Questo evento viene inviato dal sink di flusso del renderer audio.</span><span class="sxs-lookup"><span data-stu-id="4fceb-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="4fceb-118">L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a DisconnectReasonExclusiveModeOverride.</span><span class="sxs-lookup"><span data-stu-id="4fceb-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to DisconnectReasonExclusiveModeOverride.</span></span>

<span data-ttu-id="4fceb-119">Il puntatore [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , se impostato, non è utile perché il flusso audio non è più valido.</span><span class="sxs-lookup"><span data-stu-id="4fceb-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fceb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fceb-120">Requirements</span></span>



| <span data-ttu-id="4fceb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fceb-121">Requirement</span></span> | <span data-ttu-id="4fceb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4fceb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fceb-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fceb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4fceb-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4fceb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4fceb-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fceb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4fceb-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4fceb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4fceb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fceb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fceb-128"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4fceb-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fceb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fceb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fceb-130">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4fceb-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="4fceb-131">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="4fceb-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
