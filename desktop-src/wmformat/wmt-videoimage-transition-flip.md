---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl. h)
description: La transizione Flip ruota l'immagine precedente su un asse y attraverso il centro del frame. La nuova immagine viene rivelata come parte posteriore dell'immagine precedente.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333529"
---
# <a name="wmt_videoimage_transition_flip"></a><span data-ttu-id="43e73-105">WMT \_ VIDEOIMAGE \_ transizione \_ Flip</span><span class="sxs-lookup"><span data-stu-id="43e73-105">WMT\_VIDEOIMAGE\_TRANSITION\_FLIP</span></span>

<span data-ttu-id="43e73-106">La transizione Flip ruota l'immagine precedente su un asse y attraverso il centro del frame.</span><span class="sxs-lookup"><span data-stu-id="43e73-106">The flip transition rotates the old image on a y-axis through the center of the frame.</span></span> <span data-ttu-id="43e73-107">La nuova immagine viene rivelata come parte posteriore dell'immagine precedente.</span><span class="sxs-lookup"><span data-stu-id="43e73-107">The new image is revealed as the back of the old image.</span></span>

## <a name="parameters"></a><span data-ttu-id="43e73-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="43e73-108">Parameters</span></span>

<span data-ttu-id="43e73-109">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="43e73-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43e73-110">Parametro</span><span class="sxs-lookup"><span data-stu-id="43e73-110">Parameter</span></span></th>
<th><span data-ttu-id="43e73-111">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="43e73-111">Structure member</span></span></th>
<th><span data-ttu-id="43e73-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43e73-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43e73-113">Angle</span><span class="sxs-lookup"><span data-stu-id="43e73-113">Angle</span></span></td>
<td><span data-ttu-id="43e73-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="43e73-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="43e73-115">Angolo della rotazione, da 0,0 a 180,0 gradi.</span><span class="sxs-lookup"><span data-stu-id="43e73-115">Angle of the rotation, from 0.0 to 180.0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43e73-116">Composizione</span><span class="sxs-lookup"><span data-stu-id="43e73-116">Composition</span></span></td>
<td><span data-ttu-id="43e73-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="43e73-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="43e73-118">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="43e73-118">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="43e73-119">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="43e73-119">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="43e73-120">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="43e73-120">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="43e73-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="43e73-121">Remarks</span></span>

<span data-ttu-id="43e73-122">È possibile visualizzare l'effetto di questa transizione come se entrambe le immagini fossero fotografie fisiche associate insieme a back-to-back.</span><span class="sxs-lookup"><span data-stu-id="43e73-122">You can visualize the effect of this transition as if both images were physical photographs glued together back-to-back.</span></span> <span data-ttu-id="43e73-123">La transizione ha lo stesso effetto di tenere due fotografie di questo tipo al centro del bordo inferiore e di ruotarle 180 gradi.</span><span class="sxs-lookup"><span data-stu-id="43e73-123">The transition has the same effect as holding two such photographs at the center of the bottom edge and rotating them 180 degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e73-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43e73-124">Requirements</span></span>



| <span data-ttu-id="43e73-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e73-125">Requirement</span></span> | <span data-ttu-id="43e73-126">Valore</span><span class="sxs-lookup"><span data-stu-id="43e73-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43e73-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43e73-127">Header</span></span><br/> | <dl> <span data-ttu-id="43e73-128"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43e73-128"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e73-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43e73-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e73-130">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="43e73-130">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





