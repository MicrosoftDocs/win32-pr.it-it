---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl. h)
description: La transizione della rotellina rivela la nuova immagine ruotando quattro linee intorno a un punto di perno comune, ad esempio i spoke di una rotellina.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333962"
---
# <a name="wmt_videoimage_transition_wheel"></a><span data-ttu-id="bb22d-104">\_ \_ rotellina di transizione VIDEOIMAGE di WMT \_</span><span class="sxs-lookup"><span data-stu-id="bb22d-104">WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL</span></span>

<span data-ttu-id="bb22d-105">La transizione della rotellina rivela la nuova immagine ruotando quattro linee intorno a un punto di perno comune, ad esempio i spoke di una rotellina.</span><span class="sxs-lookup"><span data-stu-id="bb22d-105">The wheel transition reveals the new image by rotating four lines around a common pivot point, like the spokes of a wheel.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb22d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb22d-106">Parameters</span></span>

<span data-ttu-id="bb22d-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="bb22d-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb22d-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="bb22d-108">Parameter</span></span></th>
<th><span data-ttu-id="bb22d-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="bb22d-109">Structure member</span></span></th>
<th><span data-ttu-id="bb22d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb22d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb22d-111">Centra X</span><span class="sxs-lookup"><span data-stu-id="bb22d-111">Center X</span></span></td>
<td><span data-ttu-id="bb22d-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="bb22d-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="bb22d-113">Coordinata X, relativa al frame video, del centro dell'effetto della rotellina.</span><span class="sxs-lookup"><span data-stu-id="bb22d-113">X-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb22d-114">Centra Y</span><span class="sxs-lookup"><span data-stu-id="bb22d-114">Center Y</span></span></td>
<td><span data-ttu-id="bb22d-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="bb22d-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="bb22d-116">Coordinata Y, relativa al frame video, del centro dell'effetto della rotellina.</span><span class="sxs-lookup"><span data-stu-id="bb22d-116">Y-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb22d-117">Angle</span><span class="sxs-lookup"><span data-stu-id="bb22d-117">Angle</span></span></td>
<td><span data-ttu-id="bb22d-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="bb22d-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="bb22d-119">Angolo di rotazione, in gradi, dei raggi dell'effetto della rotellina.</span><span class="sxs-lookup"><span data-stu-id="bb22d-119">Angle of rotation, in degrees, of the spokes of the wheel effect.</span></span> <span data-ttu-id="bb22d-120">Il valore 0,0 indica l'immagine precedente senza la nuova immagine rivelata.</span><span class="sxs-lookup"><span data-stu-id="bb22d-120">A value of 0.0 indicates the old image without any of the new image revealed.</span></span> <span data-ttu-id="bb22d-121">Il valore 90,0 indica che la nuova immagine è stata rivelata completamente. Lo spostamento da 0,0 a 90,0 viene visualizzato come rotazione in senso orario dei raggi.</span><span class="sxs-lookup"><span data-stu-id="bb22d-121">A value of 90.0 indicates the new image fully revealed.Movement from 0.0 to 90.0 appears as clockwise rotation of the spokes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb22d-122">Composizione</span><span class="sxs-lookup"><span data-stu-id="bb22d-122">Composition</span></span></td>
<td><span data-ttu-id="bb22d-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="bb22d-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="bb22d-124">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb22d-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="bb22d-125">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="bb22d-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="bb22d-126">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="bb22d-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="bb22d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb22d-127">Requirements</span></span>



| <span data-ttu-id="bb22d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb22d-128">Requirement</span></span> | <span data-ttu-id="bb22d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="bb22d-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb22d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb22d-130">Header</span></span><br/> | <dl> <span data-ttu-id="bb22d-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb22d-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb22d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb22d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb22d-133">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="bb22d-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





