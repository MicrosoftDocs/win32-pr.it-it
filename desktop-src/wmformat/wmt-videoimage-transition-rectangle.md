---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl. h)
description: La transizione del rettangolo rivela la nuova immagine in un rettangolo all'interno del frame.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331205"
---
# <a name="wmt_videoimage_transition_rectangle"></a><span data-ttu-id="ae660-104">\_rettangolo di \_ transizione \_ VIDEOIMAGE di WMT</span><span class="sxs-lookup"><span data-stu-id="ae660-104">WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE</span></span>

<span data-ttu-id="ae660-105">La transizione del rettangolo rivela la nuova immagine in un rettangolo all'interno del frame.</span><span class="sxs-lookup"><span data-stu-id="ae660-105">The rectangle transition reveals the new image in a rectangle within the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae660-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae660-106">Parameters</span></span>

<span data-ttu-id="ae660-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="ae660-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae660-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="ae660-108">Parameter</span></span></th>
<th><span data-ttu-id="ae660-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="ae660-109">Structure member</span></span></th>
<th><span data-ttu-id="ae660-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae660-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae660-111">Centra X</span><span class="sxs-lookup"><span data-stu-id="ae660-111">Center X</span></span></td>
<td><span data-ttu-id="ae660-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="ae660-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="ae660-113">Coordinata X, relativa al frame video, del centro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ae660-113">X-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae660-114">Centra Y</span><span class="sxs-lookup"><span data-stu-id="ae660-114">Center Y</span></span></td>
<td><span data-ttu-id="ae660-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="ae660-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="ae660-116">Coordinata Y, relativa al frame video, del centro del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ae660-116">Y-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae660-117">Larghezza</span><span class="sxs-lookup"><span data-stu-id="ae660-117">Width</span></span></td>
<td><span data-ttu-id="ae660-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="ae660-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="ae660-119">Larghezza del rettangolo in pixel.</span><span class="sxs-lookup"><span data-stu-id="ae660-119">Width of the rectangle in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae660-120">Altezza</span><span class="sxs-lookup"><span data-stu-id="ae660-120">Height</span></span></td>
<td><span data-ttu-id="ae660-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="ae660-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="ae660-122">Altezza del rettangolo in pixel.</span><span class="sxs-lookup"><span data-stu-id="ae660-122">Height of the rectangle in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae660-123">Composizione</span><span class="sxs-lookup"><span data-stu-id="ae660-123">Composition</span></span></td>
<td><span data-ttu-id="ae660-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="ae660-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="ae660-125">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae660-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="ae660-126">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="ae660-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="ae660-127">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="ae660-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="ae660-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae660-128">Requirements</span></span>



| <span data-ttu-id="ae660-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae660-129">Requirement</span></span> | <span data-ttu-id="ae660-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ae660-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae660-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae660-131">Header</span></span><br/> | <dl> <span data-ttu-id="ae660-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae660-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae660-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae660-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae660-134">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="ae660-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





