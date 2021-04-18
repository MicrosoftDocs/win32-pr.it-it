---
title: WMT_VIDEOIMAGE_TRANSITION_CIRCLE (Wmsdkidl. h)
description: La transizione del cerchio rivela la nuova immagine in un cerchio.
ms.assetid: ba3bcf46-1254-4aad-a958-0f9ddb2f40dc
keywords:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf3a8eff2ca5a5069fa01c4e61bc0735808fd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333737"
---
# <a name="wmt_videoimage_transition_circle"></a><span data-ttu-id="9b99e-104">\_cerchio di \_ transizione \_ VIDEOIMAGE di WMT</span><span class="sxs-lookup"><span data-stu-id="9b99e-104">WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE</span></span>

<span data-ttu-id="9b99e-105">La transizione del cerchio rivela la nuova immagine in un cerchio.</span><span class="sxs-lookup"><span data-stu-id="9b99e-105">The circle transition reveals the new image in a circle.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b99e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b99e-106">Parameters</span></span>

<span data-ttu-id="9b99e-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="9b99e-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b99e-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="9b99e-108">Parameter</span></span></th>
<th><span data-ttu-id="9b99e-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="9b99e-109">Structure member</span></span></th>
<th><span data-ttu-id="9b99e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b99e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b99e-111">Centra X</span><span class="sxs-lookup"><span data-stu-id="9b99e-111">Center X</span></span></td>
<td><span data-ttu-id="9b99e-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="9b99e-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="9b99e-113">Coordinata X, relativa al frame video, del centro del cerchio.</span><span class="sxs-lookup"><span data-stu-id="9b99e-113">X-coordinate, relative to the video frame, of the center of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b99e-114">Centra Y</span><span class="sxs-lookup"><span data-stu-id="9b99e-114">Center Y</span></span></td>
<td><span data-ttu-id="9b99e-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="9b99e-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="9b99e-116">Coordinata Y, relativa al frame video, del centro del cerchio.</span><span class="sxs-lookup"><span data-stu-id="9b99e-116">Y-coordinate, relative to the video frame, of center of the circle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b99e-117">Radius</span><span class="sxs-lookup"><span data-stu-id="9b99e-117">Radius</span></span></td>
<td><span data-ttu-id="9b99e-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="9b99e-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="9b99e-119">Raggio, in pixel, del cerchio.</span><span class="sxs-lookup"><span data-stu-id="9b99e-119">Radius, in pixels, of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b99e-120">Composizione</span><span class="sxs-lookup"><span data-stu-id="9b99e-120">Composition</span></span></td>
<td><span data-ttu-id="9b99e-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="9b99e-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="9b99e-122">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b99e-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="9b99e-123">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="9b99e-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="9b99e-124">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="9b99e-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9b99e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b99e-125">Requirements</span></span>



| <span data-ttu-id="9b99e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b99e-126">Requirement</span></span> | <span data-ttu-id="9b99e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9b99e-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b99e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b99e-128">Header</span></span><br/> | <dl> <span data-ttu-id="9b99e-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b99e-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b99e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b99e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b99e-131">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="9b99e-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





