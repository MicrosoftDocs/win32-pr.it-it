---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl. h)
description: La transizione Insert Mostra la nuova immagine in un rettangolo originato da un angolo del frame.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326871"
---
# <a name="wmt_videoimage_transition_inset"></a><span data-ttu-id="cc7a6-104">\_Insert WMT VIDEOIMAGE \_ Transition \_</span><span class="sxs-lookup"><span data-stu-id="cc7a6-104">WMT\_VIDEOIMAGE\_TRANSITION\_INSET</span></span>

<span data-ttu-id="cc7a6-105">La transizione Insert Mostra la nuova immagine in un rettangolo originato da un angolo del frame.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-105">The inset transition reveals the new image in a rectangle originating from one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc7a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc7a6-106">Parameters</span></span>

<span data-ttu-id="cc7a6-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc7a6-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="cc7a6-108">Parameter</span></span></th>
<th><span data-ttu-id="cc7a6-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="cc7a6-109">Structure member</span></span></th>
<th><span data-ttu-id="cc7a6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc7a6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc7a6-111">Larghezza</span><span class="sxs-lookup"><span data-stu-id="cc7a6-111">Width</span></span></td>
<td><span data-ttu-id="cc7a6-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="cc7a6-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="cc7a6-113">Larghezza dell'inserto in pixel.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-113">Width of the inset in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc7a6-114">Altezza</span><span class="sxs-lookup"><span data-stu-id="cc7a6-114">Height</span></span></td>
<td><span data-ttu-id="cc7a6-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="cc7a6-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="cc7a6-116">Altezza dell'inserto in pixel.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-116">Height of the inset in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc7a6-117">Direzione</span><span class="sxs-lookup"><span data-stu-id="cc7a6-117">Direction</span></span></td>
<td><span data-ttu-id="cc7a6-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="cc7a6-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="cc7a6-119">Angolo da cui ha origine l'inserimento. Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc7a6-119">Corner from which the inset originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="cc7a6-120">0-in basso a sinistra</span><span class="sxs-lookup"><span data-stu-id="cc7a6-120">0 - Lower left</span></span></li>
<li><span data-ttu-id="cc7a6-121">1-in basso a destra</span><span class="sxs-lookup"><span data-stu-id="cc7a6-121">1 - Lower right</span></span></li>
<li><span data-ttu-id="cc7a6-122">2-in alto a sinistra</span><span class="sxs-lookup"><span data-stu-id="cc7a6-122">2 - Upper left</span></span></li>
<li><span data-ttu-id="cc7a6-123">3-in alto a destra</span><span class="sxs-lookup"><span data-stu-id="cc7a6-123">3 - Upper right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc7a6-124">Composizione</span><span class="sxs-lookup"><span data-stu-id="cc7a6-124">Composition</span></span></td>
<td><span data-ttu-id="cc7a6-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="cc7a6-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="cc7a6-126">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc7a6-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="cc7a6-127">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="cc7a6-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="cc7a6-128">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="cc7a6-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="cc7a6-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc7a6-129">Requirements</span></span>



| <span data-ttu-id="cc7a6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc7a6-130">Requirement</span></span> | <span data-ttu-id="cc7a6-131">Valore</span><span class="sxs-lookup"><span data-stu-id="cc7a6-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7a6-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc7a6-132">Header</span></span><br/> | <dl> <span data-ttu-id="cc7a6-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc7a6-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc7a6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc7a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc7a6-135">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="cc7a6-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





