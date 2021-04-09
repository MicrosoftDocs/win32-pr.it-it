---
description: Inviato da un'origine di acquisizione audio quando il dession audio è disconnesso perché l'utente si è disconnesso da una sessione di Servizi terminal di Windows (WTS).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Evento MECaptureAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae45ecded4a2a412525da70133845c2487aa604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130035"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a><span data-ttu-id="6b8d3-103">Evento MECaptureAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="6b8d3-103">MECaptureAudioSessionDisconnected event</span></span>

<span data-ttu-id="6b8d3-104">Inviato da un'origine di acquisizione audio quando il dession audio è disconnesso perché l'utente si è disconnesso da una sessione di Servizi terminal di Windows (WTS).</span><span class="sxs-lookup"><span data-stu-id="6b8d3-104">Sent by an audio capture source when the audio dession is disconnected because the user logged off from a Windows Terminal Services (WTS) session.</span></span>

## <a name="event-values"></a><span data-ttu-id="6b8d3-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="6b8d3-105">Event values</span></span>

<span data-ttu-id="6b8d3-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6b8d3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6b8d3-107">VARTYPE</span></span>               | <span data-ttu-id="6b8d3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b8d3-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="6b8d3-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="6b8d3-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="6b8d3-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6b8d3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b8d3-111">Remarks</span></span>

<span data-ttu-id="6b8d3-112">Questo evento viene inviato dal flusso multimediale dell'origine di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="6b8d3-113">L'origine di acquisizione Invia questo evento quando riceve un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) dalla sessione audio con il motivo di disconnessione uguale a **DisconnectReasonSessionDisconnected**.</span><span class="sxs-lookup"><span data-stu-id="6b8d3-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonSessionDisconnected**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8d3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8d3-114">Requirements</span></span>



| <span data-ttu-id="6b8d3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8d3-115">Requirement</span></span> | <span data-ttu-id="6b8d3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8d3-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8d3-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8d3-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6b8d3-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="6b8d3-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8d3-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6b8d3-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b8d3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b8d3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b8d3-122"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b8d3-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8d3-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8d3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8d3-124">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b8d3-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
