---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl. h)
description: La transizione V riempita rivela la nuova immagine in un triangolo originato da un lato del frame.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324866"
---
# <a name="wmt_videoimage_transition_filled_v"></a><span data-ttu-id="f9d12-104">WMT \_ VIDEOIMAGE \_ - \_ riempimento della transizione \_</span><span class="sxs-lookup"><span data-stu-id="f9d12-104">WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V</span></span>

<span data-ttu-id="f9d12-105">La transizione V riempita rivela la nuova immagine in un triangolo originato da un lato del frame.</span><span class="sxs-lookup"><span data-stu-id="f9d12-105">The filled V transition reveals the new image in a triangle originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9d12-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9d12-106">Parameters</span></span>

<span data-ttu-id="f9d12-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="f9d12-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9d12-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="f9d12-108">Parameter</span></span></th>
<th><span data-ttu-id="f9d12-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="f9d12-109">Structure member</span></span></th>
<th><span data-ttu-id="f9d12-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9d12-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9d12-111">Larghezza</span><span class="sxs-lookup"><span data-stu-id="f9d12-111">Width</span></span></td>
<td><span data-ttu-id="f9d12-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="f9d12-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="f9d12-113">Larghezza della V piena in pixel.</span><span class="sxs-lookup"><span data-stu-id="f9d12-113">Width of the filled V in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9d12-114">Altezza</span><span class="sxs-lookup"><span data-stu-id="f9d12-114">Height</span></span></td>
<td><span data-ttu-id="f9d12-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="f9d12-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="f9d12-116">Altezza della V riempita in pixel.</span><span class="sxs-lookup"><span data-stu-id="f9d12-116">Height of the filled V in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9d12-117">Direzione</span><span class="sxs-lookup"><span data-stu-id="f9d12-117">Direction</span></span></td>
<td><span data-ttu-id="f9d12-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="f9d12-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="f9d12-119">Direzione da cui ha origine la V piena. Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9d12-119">Direction from which the filled V originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="f9d12-120">0: immette dal lato sinistro del frame.</span><span class="sxs-lookup"><span data-stu-id="f9d12-120">0 - Enters from the left side of the frame.</span></span></li>
<li><span data-ttu-id="f9d12-121">1: immette dal lato destro del frame.</span><span class="sxs-lookup"><span data-stu-id="f9d12-121">1 - Enters from the right side of the frame.</span></span></li>
<li><span data-ttu-id="f9d12-122">2: immette dalla parte inferiore del frame.</span><span class="sxs-lookup"><span data-stu-id="f9d12-122">2 - Enters from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="f9d12-123">3-immette dalla parte superiore del frame.</span><span class="sxs-lookup"><span data-stu-id="f9d12-123">3 - Enters from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9d12-124">Composizione</span><span class="sxs-lookup"><span data-stu-id="f9d12-124">Composition</span></span></td>
<td><span data-ttu-id="f9d12-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="f9d12-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="f9d12-126">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9d12-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="f9d12-127">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="f9d12-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="f9d12-128">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="f9d12-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="f9d12-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9d12-129">Requirements</span></span>



| <span data-ttu-id="f9d12-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9d12-130">Requirement</span></span> | <span data-ttu-id="f9d12-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f9d12-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d12-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9d12-132">Header</span></span><br/> | <dl> <span data-ttu-id="f9d12-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d12-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9d12-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9d12-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d12-135">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="f9d12-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





