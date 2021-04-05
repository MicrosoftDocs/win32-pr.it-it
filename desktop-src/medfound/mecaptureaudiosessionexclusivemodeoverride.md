---
description: Inviato da un'origine di acquisizione audio quando un altro programma apre il dispositivo audio in modalità esclusiva.
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: Evento MECaptureAudioSessionExclusiveModeOverride (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751279"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a><span data-ttu-id="3097b-103">Evento MECaptureAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="3097b-103">MECaptureAudioSessionExclusiveModeOverride event</span></span>

<span data-ttu-id="3097b-104">Inviato da un'origine di acquisizione audio quando un altro programma apre il dispositivo audio in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="3097b-104">Sent by an audio capture source when another program opens the audio device in exclusive mode.</span></span>

## <a name="event-values"></a><span data-ttu-id="3097b-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="3097b-105">Event values</span></span>

<span data-ttu-id="3097b-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="3097b-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3097b-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3097b-107">VARTYPE</span></span>               | <span data-ttu-id="3097b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3097b-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="3097b-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="3097b-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="3097b-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3097b-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3097b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3097b-111">Remarks</span></span>

<span data-ttu-id="3097b-112">Questo evento viene inviato dal flusso multimediale dell'origine di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="3097b-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="3097b-113">L'origine di acquisizione Invia questo evento quando riceve un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a **DisconnectReasonExclusiveModeOverride**.</span><span class="sxs-lookup"><span data-stu-id="3097b-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonExclusiveModeOverride**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3097b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3097b-114">Requirements</span></span>



| <span data-ttu-id="3097b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3097b-115">Requirement</span></span> | <span data-ttu-id="3097b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3097b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3097b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3097b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3097b-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3097b-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="3097b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3097b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3097b-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3097b-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3097b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3097b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3097b-122"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3097b-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3097b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3097b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3097b-124">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3097b-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
