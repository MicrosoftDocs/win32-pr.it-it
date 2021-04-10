---
description: Generato dal renderer audio quando il formato audio predefinito per il dispositivo audio viene modificato. Il renderer audio non è ora valido.
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: Evento MEAudioSessionFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1faddc73622c65d1eb32e0d723f576b9410d978b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879714"
---
# <a name="meaudiosessionformatchanged-event"></a><span data-ttu-id="c931d-104">Evento MEAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="c931d-104">MEAudioSessionFormatChanged event</span></span>

<span data-ttu-id="c931d-105">Generato dal renderer audio quando il formato audio predefinito per il dispositivo audio viene modificato.</span><span class="sxs-lookup"><span data-stu-id="c931d-105">Raised by the audio renderer when the default audio format for the audio device changes.</span></span> <span data-ttu-id="c931d-106">Il renderer audio non è ora valido.</span><span class="sxs-lookup"><span data-stu-id="c931d-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="c931d-107">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c931d-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="c931d-108">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="c931d-108">Event values</span></span>

<span data-ttu-id="c931d-109">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="c931d-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c931d-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c931d-110">VARTYPE</span></span>                | <span data-ttu-id="c931d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c931d-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c931d-112">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="c931d-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="c931d-113">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c931d-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="c931d-114">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="c931d-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="c931d-115">Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="c931d-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c931d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c931d-116">Remarks</span></span>

<span data-ttu-id="c931d-117">Questo evento viene inviato dal sink di flusso del renderer audio.</span><span class="sxs-lookup"><span data-stu-id="c931d-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="c931d-118">L'evento viene attivato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio in modalità utente con il motivo di disconnessione uguale a **DisconnectReasonFormatChanged**.</span><span class="sxs-lookup"><span data-stu-id="c931d-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the user-mode audio session with the disconnection reason equal to **DisconnectReasonFormatChanged**.</span></span>

<span data-ttu-id="c931d-119">Il puntatore [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , se impostato, non è utile perché il flusso audio non è più valido.</span><span class="sxs-lookup"><span data-stu-id="c931d-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="c931d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c931d-120">Requirements</span></span>



| <span data-ttu-id="c931d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c931d-121">Requirement</span></span> | <span data-ttu-id="c931d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c931d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c931d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c931d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c931d-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c931d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c931d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c931d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c931d-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c931d-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c931d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c931d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c931d-128"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c931d-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c931d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c931d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c931d-130">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c931d-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="c931d-131">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="c931d-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
