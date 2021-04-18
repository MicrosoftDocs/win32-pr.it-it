---
description: Generato dal renderer audio quando il sistema server audio Windows viene arrestato. Il renderer audio non è ora valido.
ms.assetid: 8e80903c-d6ce-4fa2-87db-552c7fba3c6a
title: Evento MEAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d819d850df481477b2ea1a5052c18d140a41cdb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308273"
---
# <a name="meaudiosessionservershutdown-event"></a><span data-ttu-id="a06d5-104">Evento MEAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="a06d5-104">MEAudioSessionServerShutdown event</span></span>

<span data-ttu-id="a06d5-105">Generato dal renderer audio quando il sistema server audio Windows viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="a06d5-105">Raised by the audio renderer when the Windows audio server system is shut down.</span></span> <span data-ttu-id="a06d5-106">Il renderer audio non è ora valido.</span><span class="sxs-lookup"><span data-stu-id="a06d5-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="a06d5-107">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a06d5-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="a06d5-108">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="a06d5-108">Event values</span></span>

<span data-ttu-id="a06d5-109">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="a06d5-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a06d5-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a06d5-110">VARTYPE</span></span>                | <span data-ttu-id="a06d5-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a06d5-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a06d5-112">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="a06d5-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="a06d5-113">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="a06d5-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="a06d5-114">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="a06d5-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="a06d5-115">Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="a06d5-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a06d5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a06d5-116">Remarks</span></span>

<span data-ttu-id="a06d5-117">Questo evento viene inviato dal sink di flusso del renderer audio.</span><span class="sxs-lookup"><span data-stu-id="a06d5-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="a06d5-118">L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a **DisconnectReasonServerShutdown**.</span><span class="sxs-lookup"><span data-stu-id="a06d5-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonServerShutdown**.</span></span>

<span data-ttu-id="a06d5-119">Il puntatore [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , se impostato, non è utile perché il flusso audio non è più valido.</span><span class="sxs-lookup"><span data-stu-id="a06d5-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="a06d5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a06d5-120">Requirements</span></span>



| <span data-ttu-id="a06d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a06d5-121">Requirement</span></span> | <span data-ttu-id="a06d5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a06d5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a06d5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a06d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a06d5-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a06d5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a06d5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a06d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a06d5-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a06d5-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a06d5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a06d5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a06d5-128"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a06d5-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a06d5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a06d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a06d5-130">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a06d5-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="a06d5-131">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="a06d5-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
