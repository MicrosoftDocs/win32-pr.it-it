---
description: Inviato da un sink di flusso quando il formato downstream è stato invalidato e deve essere rinegoziato.
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: Evento MEStreamSinkFormatInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307992"
---
# <a name="mestreamsinkformatinvalidated-event"></a><span data-ttu-id="ab951-103">Evento MEStreamSinkFormatInvalidated</span><span class="sxs-lookup"><span data-stu-id="ab951-103">MEStreamSinkFormatInvalidated event</span></span>

<span data-ttu-id="ab951-104">Inviato da un sink di flusso quando il formato downstream è stato invalidato e deve essere rinegoziato.</span><span class="sxs-lookup"><span data-stu-id="ab951-104">Sent by a stream sink when the downstream format has become invalidated and it needs to be renegotiated.</span></span>

## <a name="event-values"></a><span data-ttu-id="ab951-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="ab951-105">Event values</span></span>

<span data-ttu-id="ab951-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="ab951-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ab951-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ab951-107">VARTYPE</span></span>              | <span data-ttu-id="ab951-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab951-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ab951-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="ab951-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ab951-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="ab951-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ab951-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab951-111">Remarks</span></span>

<span data-ttu-id="ab951-112">I dati accodati al sink, oltre la posizione di riproduzione corrente, devono essere inviati nuovamente.</span><span class="sxs-lookup"><span data-stu-id="ab951-112">Data that was queued to the sink, past the current playback position, should be resent.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab951-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab951-113">Requirements</span></span>



| <span data-ttu-id="ab951-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab951-114">Requirement</span></span> | <span data-ttu-id="ab951-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ab951-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab951-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab951-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab951-117">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ab951-117">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                                      |
| <span data-ttu-id="ab951-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab951-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab951-119">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ab951-119">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="ab951-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab951-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab951-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab951-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab951-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab951-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab951-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab951-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




