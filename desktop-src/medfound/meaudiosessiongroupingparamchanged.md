---
description: Generato dal renderer audio quando i parametri di raggruppamento cambiano per la sessione audio.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Evento MEAudioSessionGroupingParamChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226334"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a><span data-ttu-id="9dd52-103">Evento MEAudioSessionGroupingParamChanged</span><span class="sxs-lookup"><span data-stu-id="9dd52-103">MEAudioSessionGroupingParamChanged event</span></span>

<span data-ttu-id="9dd52-104">Generato dal renderer audio quando i parametri di raggruppamento cambiano per la sessione audio.</span><span class="sxs-lookup"><span data-stu-id="9dd52-104">Raised by the audio renderer when the grouping parameters change for the audio session.</span></span>

<span data-ttu-id="9dd52-105">La sessione multimediale trasmette questo evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9dd52-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="9dd52-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="9dd52-106">Event values</span></span>

<span data-ttu-id="9dd52-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9dd52-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9dd52-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9dd52-108">VARTYPE</span></span>                | <span data-ttu-id="9dd52-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dd52-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd52-110">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="9dd52-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="9dd52-111">Puntatore all'interfaccia [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="9dd52-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9dd52-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dd52-112">Remarks</span></span>

<span data-ttu-id="9dd52-113">Questo evento viene inviato dal sink di flusso del renderer audio.</span><span class="sxs-lookup"><span data-stu-id="9dd52-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="9dd52-114">L'evento viene generato quando il renderer audio riceve un evento [**IAudioSessionEvents:: OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) dalla sessione audio.</span><span class="sxs-lookup"><span data-stu-id="9dd52-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) event from the audio session.</span></span>

<span data-ttu-id="9dd52-115">Per ottenere i nuovi parametri di raggruppamento, chiamare [**IMFAudioPolicy:: GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span><span class="sxs-lookup"><span data-stu-id="9dd52-115">To get the new grouping parameters, call [**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd52-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dd52-116">Requirements</span></span>



| <span data-ttu-id="9dd52-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dd52-117">Requirement</span></span> | <span data-ttu-id="9dd52-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9dd52-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd52-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dd52-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd52-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9dd52-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9dd52-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dd52-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd52-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9dd52-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9dd52-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dd52-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dd52-124"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9dd52-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dd52-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dd52-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd52-126">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9dd52-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="9dd52-127">**IMFAudioPolicy::GetGroupingParam**</span><span class="sxs-lookup"><span data-stu-id="9dd52-127">**IMFAudioPolicy::GetGroupingParam**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[<span data-ttu-id="9dd52-128">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="9dd52-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
