---
description: Generato dalla sessione multimediale quando il formato viene modificato in un sink multimediale.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Evento MESessionStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed59b9600cbaf8cb942a42beb6bed46d62fc15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226657"
---
# <a name="mesessionstreamsinkformatchanged-event"></a><span data-ttu-id="ad1c1-103">Evento MESessionStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="ad1c1-103">MESessionStreamSinkFormatChanged event</span></span>

<span data-ttu-id="ad1c1-104">Generato dalla sessione multimediale quando il formato viene modificato in un sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-104">Raised by the Media Session when the format changes on a media sink.</span></span>

## <a name="event-values"></a><span data-ttu-id="ad1c1-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="ad1c1-105">Event values</span></span>

<span data-ttu-id="ad1c1-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ad1c1-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ad1c1-107">VARTYPE</span></span>              | <span data-ttu-id="ad1c1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad1c1-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ad1c1-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="ad1c1-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ad1c1-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="ad1c1-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="ad1c1-111">Attributes</span></span>

<span data-ttu-id="ad1c1-112">Per questo evento sono definiti gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="ad1c1-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="ad1c1-113">Attribute</span></span>                                                                    | <span data-ttu-id="ad1c1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad1c1-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad1c1-115">**\_nodo di \_ output \_ evento MF**</span><span class="sxs-lookup"><span data-stu-id="ad1c1-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="ad1c1-116">Identifica il nodo della topologia per il sink multimediale il cui formato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="ad1c1-116">Identifies the topology node for the media sink whose format changed.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ad1c1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad1c1-117">Requirements</span></span>



| <span data-ttu-id="ad1c1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad1c1-118">Requirement</span></span> | <span data-ttu-id="ad1c1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ad1c1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1c1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad1c1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ad1c1-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad1c1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad1c1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad1c1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ad1c1-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ad1c1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad1c1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad1c1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad1c1-125"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad1c1-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad1c1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad1c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad1c1-127">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad1c1-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




