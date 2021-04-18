---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl. h)
description: La transizione Iris rivela la nuova immagine lungo un asse x e un asse y. L'effetto visivo di questa transizione consiste nel fatto che la nuova immagine viene visualizzata in un incrocio incrociato che raggiunge tutti i lati del frame.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329897"
---
# <a name="wmt_videoimage_transition_iris"></a><span data-ttu-id="15e15-105">\_ \_ Iris transizione VIDEOIMAGE \_ WMT</span><span class="sxs-lookup"><span data-stu-id="15e15-105">WMT\_VIDEOIMAGE\_TRANSITION\_IRIS</span></span>

<span data-ttu-id="15e15-106">La transizione Iris rivela la nuova immagine lungo un asse x e un asse y.</span><span class="sxs-lookup"><span data-stu-id="15e15-106">The iris transition reveals the new image along an x-axis and a y-axis.</span></span> <span data-ttu-id="15e15-107">L'effetto visivo di questa transizione consiste nel fatto che la nuova immagine viene visualizzata in un incrocio incrociato che raggiunge tutti i lati del frame.</span><span class="sxs-lookup"><span data-stu-id="15e15-107">The visual effect of this transition is that the new image appears in a widening cross reaching to all sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="15e15-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="15e15-108">Parameters</span></span>

<span data-ttu-id="15e15-109">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="15e15-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15e15-110">Parametro</span><span class="sxs-lookup"><span data-stu-id="15e15-110">Parameter</span></span></th>
<th><span data-ttu-id="15e15-111">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="15e15-111">Structure member</span></span></th>
<th><span data-ttu-id="15e15-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15e15-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15e15-113">Centra X</span><span class="sxs-lookup"><span data-stu-id="15e15-113">Center X</span></span></td>
<td><span data-ttu-id="15e15-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="15e15-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="15e15-115">Coordinata X, relativa al frame video, del centro dell'effetto Iris.</span><span class="sxs-lookup"><span data-stu-id="15e15-115">X-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15e15-116">Centra Y</span><span class="sxs-lookup"><span data-stu-id="15e15-116">Center Y</span></span></td>
<td><span data-ttu-id="15e15-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="15e15-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="15e15-118">Coordinata Y, relativa al frame video, del centro dell'effetto Iris.</span><span class="sxs-lookup"><span data-stu-id="15e15-118">Y-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15e15-119">Larghezza</span><span class="sxs-lookup"><span data-stu-id="15e15-119">Width</span></span></td>
<td><span data-ttu-id="15e15-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="15e15-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="15e15-121">Larghezza della linea verticale che rivela la nuova immagine, in pixel.</span><span class="sxs-lookup"><span data-stu-id="15e15-121">Width of the vertical line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15e15-122">Altezza</span><span class="sxs-lookup"><span data-stu-id="15e15-122">Height</span></span></td>
<td><span data-ttu-id="15e15-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="15e15-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="15e15-124">Altezza della linea orizzontale che rivela la nuova immagine, in pixel.</span><span class="sxs-lookup"><span data-stu-id="15e15-124">Height of the horizontal line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15e15-125">Composizione</span><span class="sxs-lookup"><span data-stu-id="15e15-125">Composition</span></span></td>
<td><span data-ttu-id="15e15-126"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="15e15-126"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="15e15-127">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="15e15-127">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="15e15-128">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="15e15-128">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="15e15-129">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="15e15-129">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="15e15-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15e15-130">Requirements</span></span>



| <span data-ttu-id="15e15-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="15e15-131">Requirement</span></span> | <span data-ttu-id="15e15-132">Valore</span><span class="sxs-lookup"><span data-stu-id="15e15-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15e15-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15e15-133">Header</span></span><br/> | <dl> <span data-ttu-id="15e15-134"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15e15-134"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15e15-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15e15-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e15-136">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="15e15-136">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





