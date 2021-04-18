---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl. h)
description: La transizione del rullo di pagina trasforma l'immagine precedente con un effetto di capovolgimento della pagina, mostrando la nuova immagine sotto.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325527"
---
# <a name="wmt_videoimage_transition_page_roll"></a><span data-ttu-id="06c09-104">\_ \_ \_ Roll pagina transizione VIDEOIMAGE \_ di WMT</span><span class="sxs-lookup"><span data-stu-id="06c09-104">WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL</span></span>

<span data-ttu-id="06c09-105">La transizione del rullo di pagina trasforma l'immagine precedente con un effetto di capovolgimento della pagina, mostrando la nuova immagine sotto.</span><span class="sxs-lookup"><span data-stu-id="06c09-105">The page roll transition transforms the old image with a page-flipping effect, revealing the new image underneath.</span></span>

## <a name="parameters"></a><span data-ttu-id="06c09-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06c09-106">Parameters</span></span>

<span data-ttu-id="06c09-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="06c09-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06c09-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="06c09-108">Parameter</span></span></th>
<th><span data-ttu-id="06c09-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="06c09-109">Structure member</span></span></th>
<th><span data-ttu-id="06c09-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06c09-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06c09-111">Radius</span><span class="sxs-lookup"><span data-stu-id="06c09-111">Radius</span></span></td>
<td><span data-ttu-id="06c09-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="06c09-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="06c09-113">Raggio del rullo nell'effetto del rullo della pagina.</span><span class="sxs-lookup"><span data-stu-id="06c09-113">Radius of the roll in the page roll effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06c09-114">Distanza</span><span class="sxs-lookup"><span data-stu-id="06c09-114">Distance</span></span></td>
<td><span data-ttu-id="06c09-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="06c09-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="06c09-116">Quantità della nuova immagine rivelata dall'effetto di roll page, in pixel.</span><span class="sxs-lookup"><span data-stu-id="06c09-116">Amount of the new image that is revealed by the page roll effect, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06c09-117">Direzione</span><span class="sxs-lookup"><span data-stu-id="06c09-117">Direction</span></span></td>
<td><span data-ttu-id="06c09-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="06c09-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="06c09-119">Angolo o lato del fotogramma video da cui ha origine il rullo di pagina. Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="06c09-119">Corner or side of the video frame, from which the page roll originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="06c09-120">0-lato sinistro</span><span class="sxs-lookup"><span data-stu-id="06c09-120">0 - Left side</span></span></li>
<li><span data-ttu-id="06c09-121">1-lato destro</span><span class="sxs-lookup"><span data-stu-id="06c09-121">1 - Right side</span></span></li>
<li><span data-ttu-id="06c09-122">2-inferiore</span><span class="sxs-lookup"><span data-stu-id="06c09-122">2 - Bottom</span></span></li>
<li><span data-ttu-id="06c09-123">3-inizio</span><span class="sxs-lookup"><span data-stu-id="06c09-123">3 - Top</span></span></li>
<li><span data-ttu-id="06c09-124">4-angolo inferiore sinistro</span><span class="sxs-lookup"><span data-stu-id="06c09-124">4 - Bottom left corner</span></span></li>
<li><span data-ttu-id="06c09-125">5-angolo inferiore destro</span><span class="sxs-lookup"><span data-stu-id="06c09-125">5 - Bottom right corner</span></span></li>
<li><span data-ttu-id="06c09-126">6-angolo superiore sinistro</span><span class="sxs-lookup"><span data-stu-id="06c09-126">6 - Upper left corner</span></span></li>
<li><span data-ttu-id="06c09-127">7-angolo superiore destro</span><span class="sxs-lookup"><span data-stu-id="06c09-127">7 - Upper right corner</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06c09-128">Composizione</span><span class="sxs-lookup"><span data-stu-id="06c09-128">Composition</span></span></td>
<td><span data-ttu-id="06c09-129"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="06c09-129"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="06c09-130">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="06c09-130">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="06c09-131">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="06c09-131">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="06c09-132">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="06c09-132">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="06c09-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06c09-133">Requirements</span></span>



| <span data-ttu-id="06c09-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c09-134">Requirement</span></span> | <span data-ttu-id="06c09-135">Valore</span><span class="sxs-lookup"><span data-stu-id="06c09-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06c09-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06c09-136">Header</span></span><br/> | <dl> <span data-ttu-id="06c09-137"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c09-137"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c09-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06c09-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c09-139">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="06c09-139">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





