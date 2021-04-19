---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl. h)
description: La transizione diagonale rivela la nuova immagine lungo una linea diagonale che ha origine in un angolo del frame.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325948"
---
# <a name="wmt_videoimage_transition_diagonal"></a><span data-ttu-id="13b0e-104">\_ \_ diagonale transizione VIDEOIMAGE WMT \_</span><span class="sxs-lookup"><span data-stu-id="13b0e-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL</span></span>

<span data-ttu-id="13b0e-105">La transizione diagonale rivela la nuova immagine lungo una linea diagonale che ha origine in un angolo del frame.</span><span class="sxs-lookup"><span data-stu-id="13b0e-105">The diagonal transition reveals the new image along a diagonal line originating in one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="13b0e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="13b0e-106">Parameters</span></span>

<span data-ttu-id="13b0e-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="13b0e-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="13b0e-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="13b0e-108">Parameter</span></span></th>
<th><span data-ttu-id="13b0e-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="13b0e-109">Structure member</span></span></th>
<th><span data-ttu-id="13b0e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13b0e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="13b0e-111">Larghezza</span><span class="sxs-lookup"><span data-stu-id="13b0e-111">Width</span></span></td>
<td><span data-ttu-id="13b0e-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="13b0e-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="13b0e-113">Larghezza della sezione diagonale in pixel.</span><span class="sxs-lookup"><span data-stu-id="13b0e-113">Width of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13b0e-114">Altezza</span><span class="sxs-lookup"><span data-stu-id="13b0e-114">Height</span></span></td>
<td><span data-ttu-id="13b0e-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="13b0e-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="13b0e-116">Altezza della sezione diagonale in pixel.</span><span class="sxs-lookup"><span data-stu-id="13b0e-116">Height of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="13b0e-117">Direzione</span><span class="sxs-lookup"><span data-stu-id="13b0e-117">Direction</span></span></td>
<td><span data-ttu-id="13b0e-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="13b0e-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="13b0e-119">Determina l'angolo da cui ha origine la transizione. Impostare su uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="13b0e-119">Determines the corner from which the transition originates.Set to one of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="13b0e-120">0-in alto a destra</span><span class="sxs-lookup"><span data-stu-id="13b0e-120">0 - Upper right</span></span></li>
<li><span data-ttu-id="13b0e-121">1-in alto a sinistra</span><span class="sxs-lookup"><span data-stu-id="13b0e-121">1 - Upper left</span></span></li>
<li><span data-ttu-id="13b0e-122">2-in basso a destra</span><span class="sxs-lookup"><span data-stu-id="13b0e-122">2 - Lower right</span></span></li>
<li><span data-ttu-id="13b0e-123">3-in basso a sinistra</span><span class="sxs-lookup"><span data-stu-id="13b0e-123">3 - Lower left</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="13b0e-124">Composizione</span><span class="sxs-lookup"><span data-stu-id="13b0e-124">Composition</span></span></td>
<td><span data-ttu-id="13b0e-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="13b0e-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="13b0e-126">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="13b0e-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="13b0e-127">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="13b0e-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="13b0e-128">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="13b0e-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="13b0e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13b0e-129">Requirements</span></span>



| <span data-ttu-id="13b0e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="13b0e-130">Requirement</span></span> | <span data-ttu-id="13b0e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="13b0e-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13b0e-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13b0e-132">Header</span></span><br/> | <dl> <span data-ttu-id="13b0e-133"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="13b0e-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b0e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13b0e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b0e-135">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="13b0e-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





