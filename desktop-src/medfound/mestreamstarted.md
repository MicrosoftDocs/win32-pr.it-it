---
description: Generato da un flusso multimediale quando l'origine viene avviata senza la ricerca. Un flusso multimediale genera questo evento quando l'origine multimediale genera l'evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309604"
---
# <a name="mestreamstarted-event"></a><span data-ttu-id="625a8-104">Evento MEStreamStarted</span><span class="sxs-lookup"><span data-stu-id="625a8-104">MEStreamStarted event</span></span>

<span data-ttu-id="625a8-105">Generato da un flusso multimediale quando l'origine viene avviata senza la ricerca.</span><span class="sxs-lookup"><span data-stu-id="625a8-105">Raised by a media stream when the source starts without seeking.</span></span> <span data-ttu-id="625a8-106">Un flusso multimediale genera questo evento quando l'origine multimediale genera l'evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="625a8-106">A media stream raises this event when the media source raises the [MESourceStarted](mesourcestarted.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="625a8-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="625a8-107">Event values</span></span>

<span data-ttu-id="625a8-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="625a8-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="625a8-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="625a8-109">VARTYPE</span></span>              | <span data-ttu-id="625a8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="625a8-110">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="625a8-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="625a8-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="625a8-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="625a8-112">No event data.</span></span><br/> <br/>                                                                          |
| <span data-ttu-id="625a8-113">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="625a8-113">VT\_I8</span></span><br/>    | <span data-ttu-id="625a8-114">Ora di inizio, in unità di 100 nanosecondi, relativa ai timestamp degli esempi.</span><span class="sxs-lookup"><span data-stu-id="625a8-114">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="625a8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="625a8-115">Requirements</span></span>



| <span data-ttu-id="625a8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="625a8-116">Requirement</span></span> | <span data-ttu-id="625a8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="625a8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="625a8-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="625a8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="625a8-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="625a8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="625a8-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="625a8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="625a8-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="625a8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="625a8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="625a8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="625a8-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="625a8-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="625a8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="625a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="625a8-125">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="625a8-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




