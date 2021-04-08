---
description: Generato da un flusso multimediale al termine del flusso.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Evento MEEndOfStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880262"
---
# <a name="meendofstream-event"></a><span data-ttu-id="71f7a-103">Evento MEEndOfStream</span><span class="sxs-lookup"><span data-stu-id="71f7a-103">MEEndOfStream event</span></span>

<span data-ttu-id="71f7a-104">Generato da un flusso multimediale al termine del flusso.</span><span class="sxs-lookup"><span data-stu-id="71f7a-104">Raised by a media stream when the stream ends.</span></span>

## <a name="event-values"></a><span data-ttu-id="71f7a-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="71f7a-105">Event values</span></span>

<span data-ttu-id="71f7a-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="71f7a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="71f7a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="71f7a-107">VARTYPE</span></span>              | <span data-ttu-id="71f7a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71f7a-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="71f7a-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="71f7a-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="71f7a-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="71f7a-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="71f7a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="71f7a-111">Remarks</span></span>

<span data-ttu-id="71f7a-112">Quando la [sessione multimediale](media-session.md) riceve l'evento MEEndOfStream, chiama [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) sul sink multimediale corrispondente, con il **\_ marcatore MFSTREAMSINK \_ ENDOFSEGMENT** tipo di marcatore.</span><span class="sxs-lookup"><span data-stu-id="71f7a-112">When the [Media Session](media-session.md) receives the MEEndOfStream event, it calls [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) on the corresponding media sink, with the **MFSTREAMSINK\_MARKER\_ENDOFSEGMENT** marker type.</span></span>

## <a name="requirements"></a><span data-ttu-id="71f7a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71f7a-113">Requirements</span></span>



| <span data-ttu-id="71f7a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="71f7a-114">Requirement</span></span> | <span data-ttu-id="71f7a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="71f7a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f7a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71f7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="71f7a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71f7a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71f7a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71f7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="71f7a-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="71f7a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71f7a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71f7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="71f7a-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71f7a-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71f7a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71f7a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f7a-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71f7a-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




