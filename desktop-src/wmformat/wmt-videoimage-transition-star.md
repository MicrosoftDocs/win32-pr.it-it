---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl. h)
description: La transizione a stella rivela la nuova immagine in una stella a cinque punte all'interno del frame.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327687"
---
# <a name="wmt_videoimage_transition_star"></a><span data-ttu-id="b7984-104">\_stella della \_ transizione \_ VIDEOIMAGE di WMT</span><span class="sxs-lookup"><span data-stu-id="b7984-104">WMT\_VIDEOIMAGE\_TRANSITION\_STAR</span></span>

<span data-ttu-id="b7984-105">La transizione a stella rivela la nuova immagine in una stella a cinque punte all'interno del frame.</span><span class="sxs-lookup"><span data-stu-id="b7984-105">The star transition reveals the new image in a five-pointed star inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7984-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7984-106">Parameters</span></span>

<span data-ttu-id="b7984-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="b7984-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7984-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="b7984-108">Parameter</span></span></th>
<th><span data-ttu-id="b7984-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="b7984-109">Structure member</span></span></th>
<th><span data-ttu-id="b7984-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7984-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7984-111">Centra X</span><span class="sxs-lookup"><span data-stu-id="b7984-111">Center X</span></span></td>
<td><span data-ttu-id="b7984-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="b7984-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="b7984-113">Coordinata X, relativa al frame video, del centro della stella.</span><span class="sxs-lookup"><span data-stu-id="b7984-113">X-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7984-114">Centra Y</span><span class="sxs-lookup"><span data-stu-id="b7984-114">Center Y</span></span></td>
<td><span data-ttu-id="b7984-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="b7984-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="b7984-116">Coordinata Y, relativa al frame video, del centro della stella.</span><span class="sxs-lookup"><span data-stu-id="b7984-116">Y-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7984-117">Radius</span><span class="sxs-lookup"><span data-stu-id="b7984-117">Radius</span></span></td>
<td><span data-ttu-id="b7984-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="b7984-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="b7984-119">Raggio, in pixel, del cerchio definito dai punti della stella.</span><span class="sxs-lookup"><span data-stu-id="b7984-119">Radius, in pixels, of the circle defined by the points of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7984-120">Composizione</span><span class="sxs-lookup"><span data-stu-id="b7984-120">Composition</span></span></td>
<td><span data-ttu-id="b7984-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="b7984-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="b7984-122">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7984-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="b7984-123">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="b7984-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="b7984-124">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="b7984-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b7984-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7984-125">Requirements</span></span>



| <span data-ttu-id="b7984-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7984-126">Requirement</span></span> | <span data-ttu-id="b7984-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b7984-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7984-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7984-128">Header</span></span><br/> | <dl> <span data-ttu-id="b7984-129"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7984-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7984-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7984-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7984-131">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="b7984-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





