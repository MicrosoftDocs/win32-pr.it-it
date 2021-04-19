---
description: Generato da un flusso multimediale quando inizia o smette di assottigliare il flusso. Per informazioni sull'assottigliamento, vedere informazioni sul controllo della frequenza.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Evento MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309602"
---
# <a name="mestreamthinmode-event"></a><span data-ttu-id="bfd34-104">Evento MEStreamThinMode</span><span class="sxs-lookup"><span data-stu-id="bfd34-104">MEStreamThinMode event</span></span>

<span data-ttu-id="bfd34-105">Generato da un flusso multimediale quando inizia o smette di assottigliare il flusso.</span><span class="sxs-lookup"><span data-stu-id="bfd34-105">Raised by a media stream when it starts or stops thinning the stream.</span></span> <span data-ttu-id="bfd34-106">Per informazioni sull' *assottigliamento*, vedere [informazioni sul controllo della frequenza](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="bfd34-106">For information about *thinning*, see [About Rate Control](about-rate-control.md).</span></span>

<span data-ttu-id="bfd34-107">Questo evento può essere inviato in risposta al metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue o al metodo [**IMFQualityAdvise:: SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .</span><span class="sxs-lookup"><span data-stu-id="bfd34-107">This event can be sent in response to the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method or the [**IMFQualityAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="bfd34-108">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="bfd34-108">Event values</span></span>

<span data-ttu-id="bfd34-109">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfd34-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bfd34-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bfd34-110">VARTYPE</span></span></th>
<th><span data-ttu-id="bfd34-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfd34-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bfd34-112">VT_BOOL</span><span class="sxs-lookup"><span data-stu-id="bfd34-112">VT_BOOL</span></span><br/></td>
<td><span data-ttu-id="bfd34-113">Indica se l'assottigliamento è stato avviato o arrestato.</span><span class="sxs-lookup"><span data-stu-id="bfd34-113">Indicates whether thinning has started or stopped.</span></span><br/>
<ul>
<li><span data-ttu-id="bfd34-114">VARIANT_TRUE: gli esempi recapitati dopo questo evento sono diluiti.</span><span class="sxs-lookup"><span data-stu-id="bfd34-114">VARIANT_TRUE: Samples delivered after this event are thinned.</span></span></li>
<li><span data-ttu-id="bfd34-115">VARIANT_FALSE: gli esempi recapitati dopo questo evento non vengono diluiti.</span><span class="sxs-lookup"><span data-stu-id="bfd34-115">VARIANT_FALSE: Samples delivered after this event are not thinned.</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="bfd34-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfd34-116">Requirements</span></span>



| <span data-ttu-id="bfd34-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfd34-117">Requirement</span></span> | <span data-ttu-id="bfd34-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bfd34-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd34-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfd34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd34-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfd34-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bfd34-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfd34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd34-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bfd34-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bfd34-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfd34-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfd34-124"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfd34-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd34-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfd34-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd34-126">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bfd34-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




