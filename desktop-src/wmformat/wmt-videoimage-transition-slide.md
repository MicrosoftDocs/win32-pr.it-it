---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl. h)
description: La transizione della diapositiva Mostra la nuova immagine spostando l'immagine precedente al di fuori del frame.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327692"
---
# <a name="wmt_videoimage_transition_slide"></a><span data-ttu-id="f63fe-104">\_diapositiva di \_ transizione \_ VIDEOIMAGE di WMT</span><span class="sxs-lookup"><span data-stu-id="f63fe-104">WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE</span></span>

<span data-ttu-id="f63fe-105">La transizione della diapositiva Mostra la nuova immagine spostando l'immagine precedente al di fuori del frame.</span><span class="sxs-lookup"><span data-stu-id="f63fe-105">The slide transition reveals the new image by sliding the old image out of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="f63fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f63fe-106">Parameters</span></span>

<span data-ttu-id="f63fe-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="f63fe-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f63fe-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="f63fe-108">Parameter</span></span></th>
<th><span data-ttu-id="f63fe-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="f63fe-109">Structure member</span></span></th>
<th><span data-ttu-id="f63fe-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f63fe-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f63fe-111">Distanza</span><span class="sxs-lookup"><span data-stu-id="f63fe-111">Distance</span></span></td>
<td><span data-ttu-id="f63fe-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="f63fe-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="f63fe-113">Distanza, in pixel, che l'immagine precedente scorre all'esterno del frame.</span><span class="sxs-lookup"><span data-stu-id="f63fe-113">Distance, in pixels, that the old image slides out of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f63fe-114">Direzione</span><span class="sxs-lookup"><span data-stu-id="f63fe-114">Direction</span></span></td>
<td><span data-ttu-id="f63fe-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="f63fe-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="f63fe-116">Direzione della diapositiva dell'immagine precedente. Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f63fe-116">Direction in which the old image slides.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="f63fe-117">0-scorrere a destra.</span><span class="sxs-lookup"><span data-stu-id="f63fe-117">0 - Slide to the right.</span></span></li>
<li><span data-ttu-id="f63fe-118">1-scorrere verso sinistra.</span><span class="sxs-lookup"><span data-stu-id="f63fe-118">1 - Slide to the left.</span></span></li>
<li><span data-ttu-id="f63fe-119">2-scorrere verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="f63fe-119">2 - Slide upward.</span></span></li>
<li><span data-ttu-id="f63fe-120">3-scorrere verso il basso.</span><span class="sxs-lookup"><span data-stu-id="f63fe-120">3 - Slide downward.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f63fe-121">Composizione</span><span class="sxs-lookup"><span data-stu-id="f63fe-121">Composition</span></span></td>
<td><span data-ttu-id="f63fe-122"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="f63fe-122"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="f63fe-123">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f63fe-123">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="f63fe-124">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="f63fe-124">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="f63fe-125">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="f63fe-125">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="f63fe-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f63fe-126">Requirements</span></span>



| <span data-ttu-id="f63fe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f63fe-127">Requirement</span></span> | <span data-ttu-id="f63fe-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f63fe-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f63fe-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f63fe-129">Header</span></span><br/> | <dl> <span data-ttu-id="f63fe-130"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f63fe-130"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f63fe-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f63fe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f63fe-132">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="f63fe-132">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





