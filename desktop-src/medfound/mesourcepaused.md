---
description: Generato da un'origine multimediale quando il metodo IMFMediaSource::P ause viene completato in modo asincrono.
ms.assetid: cca03d60-47ae-4a11-b29d-81d749e24df9
title: Evento MESourcePaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac346e679eb3a82ca707a14f772f1a79e2a1e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880249"
---
# <a name="mesourcepaused-event"></a><span data-ttu-id="60d5f-103">Evento MESourcePaused</span><span class="sxs-lookup"><span data-stu-id="60d5f-103">MESourcePaused event</span></span>

<span data-ttu-id="60d5f-104">Generato da un'origine multimediale quando il metodo [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="60d5f-104">Raised by a media source when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="60d5f-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="60d5f-105">Event values</span></span>

<span data-ttu-id="60d5f-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="60d5f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="60d5f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="60d5f-107">VARTYPE</span></span>              | <span data-ttu-id="60d5f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60d5f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="60d5f-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="60d5f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="60d5f-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="60d5f-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="60d5f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60d5f-111">Requirements</span></span>



| <span data-ttu-id="60d5f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="60d5f-112">Requirement</span></span> | <span data-ttu-id="60d5f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="60d5f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60d5f-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60d5f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="60d5f-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60d5f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="60d5f-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60d5f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="60d5f-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60d5f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="60d5f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60d5f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="60d5f-119"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60d5f-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d5f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60d5f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d5f-121">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60d5f-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




