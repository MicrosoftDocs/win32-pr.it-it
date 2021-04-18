---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl. h)
description: La transizione del Papillon Mostra la nuova immagine in un set di triangoli sui lati opposti del frame.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324449"
---
# <a name="wmt_videoimage_transition_bow_tie"></a><span data-ttu-id="390b9-104">WMT \_ VIDEOIMAGE \_ Transition \_ Papillon \_</span><span class="sxs-lookup"><span data-stu-id="390b9-104">WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE</span></span>

<span data-ttu-id="390b9-105">La transizione del Papillon Mostra la nuova immagine in un set di triangoli sui lati opposti del frame.</span><span class="sxs-lookup"><span data-stu-id="390b9-105">The bow tie transition reveals the new image in a set of triangles on opposite sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="390b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="390b9-106">Parameters</span></span>

<span data-ttu-id="390b9-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="390b9-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="390b9-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="390b9-108">Parameter</span></span></th>
<th><span data-ttu-id="390b9-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="390b9-109">Structure member</span></span></th>
<th><span data-ttu-id="390b9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="390b9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="390b9-111">Larghezza</span><span class="sxs-lookup"><span data-stu-id="390b9-111">Width</span></span></td>
<td><span data-ttu-id="390b9-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="390b9-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="390b9-113">Larghezza di ogni lato triangolare del Papillon.</span><span class="sxs-lookup"><span data-stu-id="390b9-113">Width of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="390b9-114">Altezza</span><span class="sxs-lookup"><span data-stu-id="390b9-114">Height</span></span></td>
<td><span data-ttu-id="390b9-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="390b9-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="390b9-116">Altezza di ogni lato triangolare del Papillon.</span><span class="sxs-lookup"><span data-stu-id="390b9-116">Height of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="390b9-117">Direzione</span><span class="sxs-lookup"><span data-stu-id="390b9-117">Direction</span></span></td>
<td><span data-ttu-id="390b9-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="390b9-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="390b9-119">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="390b9-119">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="390b9-120">0: specifica l'effetto di curvatura orizzontale, in cui i triangoli vengono immessi dai lati destro e sinistro del frame.</span><span class="sxs-lookup"><span data-stu-id="390b9-120">0 - Specifies horizontal bow tie effect, in which the triangles enter from the right and left sides of the frame.</span></span></li>
<li><span data-ttu-id="390b9-121">1-specifica l'effetto di curvatura verticale, in cui i triangoli vengono immessi dalla parte superiore e inferiore del frame.</span><span class="sxs-lookup"><span data-stu-id="390b9-121">1 - Specifies vertical bow tie effect, in which the triangles enter from the top and bottom of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="390b9-122">Composizione</span><span class="sxs-lookup"><span data-stu-id="390b9-122">Composition</span></span></td>
<td><span data-ttu-id="390b9-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="390b9-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="390b9-124">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="390b9-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="390b9-125">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="390b9-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="390b9-126">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="390b9-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="390b9-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="390b9-127">Requirements</span></span>



| <span data-ttu-id="390b9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="390b9-128">Requirement</span></span> | <span data-ttu-id="390b9-129">Valore</span><span class="sxs-lookup"><span data-stu-id="390b9-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="390b9-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="390b9-130">Header</span></span><br/> | <dl> <span data-ttu-id="390b9-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="390b9-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="390b9-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="390b9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390b9-133">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="390b9-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





