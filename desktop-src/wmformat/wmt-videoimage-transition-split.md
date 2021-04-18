---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl. h)
description: La transizione di divisione consente di rivelare la nuova immagine suddividendo l'immagine precedente. La divisione viene visualizzata lungo una linea retta orizzontale o verticale che inizia all'interno del frame.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327689"
---
# <a name="wmt_videoimage_transition_split"></a><span data-ttu-id="c96bf-105">\_ \_ divisione transizione VIDEOIMAGE di WMT \_</span><span class="sxs-lookup"><span data-stu-id="c96bf-105">WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT</span></span>

<span data-ttu-id="c96bf-106">La transizione di divisione consente di rivelare la nuova immagine suddividendo l'immagine precedente.</span><span class="sxs-lookup"><span data-stu-id="c96bf-106">The split transition reveals the new image by splitting the old image.</span></span> <span data-ttu-id="c96bf-107">La divisione viene visualizzata lungo una linea retta orizzontale o verticale che inizia all'interno del frame.</span><span class="sxs-lookup"><span data-stu-id="c96bf-107">The split appears along a straight horizontal or vertical line starting inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="c96bf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c96bf-108">Parameters</span></span>

<span data-ttu-id="c96bf-109">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="c96bf-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c96bf-110">Parametro</span><span class="sxs-lookup"><span data-stu-id="c96bf-110">Parameter</span></span></th>
<th><span data-ttu-id="c96bf-111">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="c96bf-111">Structure member</span></span></th>
<th><span data-ttu-id="c96bf-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c96bf-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c96bf-113">Centra X</span><span class="sxs-lookup"><span data-stu-id="c96bf-113">Center X</span></span></td>
<td><span data-ttu-id="c96bf-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="c96bf-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="c96bf-115">Coordinata X, relativa al frame video, della riga di origine della divisione.</span><span class="sxs-lookup"><span data-stu-id="c96bf-115">X-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c96bf-116">Centra Y</span><span class="sxs-lookup"><span data-stu-id="c96bf-116">Center Y</span></span></td>
<td><span data-ttu-id="c96bf-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="c96bf-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="c96bf-118">Coordinata Y, relativa al frame video, della riga di origine della divisione.</span><span class="sxs-lookup"><span data-stu-id="c96bf-118">Y-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c96bf-119">Distanza</span><span class="sxs-lookup"><span data-stu-id="c96bf-119">Distance</span></span></td>
<td><span data-ttu-id="c96bf-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="c96bf-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="c96bf-121">Larghezza della divisione in pixel.</span><span class="sxs-lookup"><span data-stu-id="c96bf-121">Width of the split in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c96bf-122">Direzione</span><span class="sxs-lookup"><span data-stu-id="c96bf-122">Direction</span></span></td>
<td><span data-ttu-id="c96bf-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="c96bf-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="c96bf-124">Orientamento della divisione. Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c96bf-124">Orientation of the split.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="c96bf-125">0: divide lungo una linea orizzontale.</span><span class="sxs-lookup"><span data-stu-id="c96bf-125">0 - Splits along a horizontal line.</span></span></li>
<li><span data-ttu-id="c96bf-126">1-divide lungo una linea verticale.</span><span class="sxs-lookup"><span data-stu-id="c96bf-126">1 - Splits along a vertical line.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c96bf-127">Composizione</span><span class="sxs-lookup"><span data-stu-id="c96bf-127">Composition</span></span></td>
<td><span data-ttu-id="c96bf-128"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="c96bf-128"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="c96bf-129">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c96bf-129">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="c96bf-130">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="c96bf-130">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="c96bf-131">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="c96bf-131">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c96bf-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c96bf-132">Requirements</span></span>



| <span data-ttu-id="c96bf-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c96bf-133">Requirement</span></span> | <span data-ttu-id="c96bf-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c96bf-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c96bf-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c96bf-135">Header</span></span><br/> | <dl> <span data-ttu-id="c96bf-136"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c96bf-136"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c96bf-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c96bf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c96bf-138">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="c96bf-138">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





