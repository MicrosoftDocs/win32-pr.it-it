---
description: Inviato da un'origine di acquisizione audio quando la sessione audio di acquisizione è disconnessa a causa dell'arresto del server audio.
ms.assetid: 43284B3E-3018-44F3-8D6C-8C3041DCCD3E
title: Evento MECaptureAudioSessionServerShutdown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad934f6d60868c1db7c5b5b7907ff720312ea439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315046"
---
# <a name="mecaptureaudiosessionservershutdown-event"></a><span data-ttu-id="114a5-103">Evento MECaptureAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="114a5-103">MECaptureAudioSessionServerShutdown event</span></span>

<span data-ttu-id="114a5-104">Inviato da un'origine di acquisizione audio quando la sessione audio di acquisizione è disconnessa a causa dell'arresto del server audio.</span><span class="sxs-lookup"><span data-stu-id="114a5-104">Sent by an audio capture source when the capture audio session is disconnected due to the audio server being shutdown.</span></span>

## <a name="event-values"></a><span data-ttu-id="114a5-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="114a5-105">Event values</span></span>

<span data-ttu-id="114a5-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="114a5-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="114a5-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="114a5-107">VARTYPE</span></span>               | <span data-ttu-id="114a5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="114a5-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="114a5-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="114a5-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="114a5-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="114a5-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="114a5-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="114a5-111">Requirements</span></span>



| <span data-ttu-id="114a5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="114a5-112">Requirement</span></span> | <span data-ttu-id="114a5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="114a5-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="114a5-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="114a5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="114a5-115">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="114a5-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="114a5-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="114a5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="114a5-117">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="114a5-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="114a5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="114a5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="114a5-119"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="114a5-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="114a5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="114a5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114a5-121">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="114a5-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




