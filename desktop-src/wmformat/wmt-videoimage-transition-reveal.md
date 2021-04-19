---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: La transizione Reveal Mostra la nuova immagine lungo una linea retta originata da un lato del frame.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331688"
---
# <a name="wmt_videoimage_transition_reveal"></a><span data-ttu-id="54534-104">WMT \_ VIDEOIMAGE \_ transizione \_</span><span class="sxs-lookup"><span data-stu-id="54534-104">WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL</span></span>

<span data-ttu-id="54534-105">La transizione Reveal Mostra la nuova immagine lungo una linea retta originata da un lato del frame.</span><span class="sxs-lookup"><span data-stu-id="54534-105">The reveal transition reveals the new image along a straight line originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="54534-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="54534-106">Parameters</span></span>

<span data-ttu-id="54534-107">Nella tabella seguente vengono descritti i parametri utilizzati da questa transizione ed elencati i membri della struttura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) a cui sono assegnati.</span><span class="sxs-lookup"><span data-stu-id="54534-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54534-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="54534-108">Parameter</span></span></th>
<th><span data-ttu-id="54534-109">Membro della struttura</span><span class="sxs-lookup"><span data-stu-id="54534-109">Structure member</span></span></th>
<th><span data-ttu-id="54534-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54534-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54534-111">Distanza</span><span class="sxs-lookup"><span data-stu-id="54534-111">Distance</span></span></td>
<td><span data-ttu-id="54534-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="54534-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="54534-113">Quantità della nuova immagine rivelata, in pixel.</span><span class="sxs-lookup"><span data-stu-id="54534-113">Amount of the new image revealed, in pixels.</span></span> <span data-ttu-id="54534-114">Questo valore è relativo al lato di origine del frame.</span><span class="sxs-lookup"><span data-stu-id="54534-114">This value is relative to the originating side of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54534-115">Direzione</span><span class="sxs-lookup"><span data-stu-id="54534-115">Direction</span></span></td>
<td><span data-ttu-id="54534-116"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="54534-116"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="54534-117">Direzione della rivelazione. Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="54534-117">Direction of the revealing.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="54534-118">0: rivela a destra; originano dal lato sinistro del frame.</span><span class="sxs-lookup"><span data-stu-id="54534-118">0 - Reveal to the right; originate from the left side of the frame.</span></span></li>
<li><span data-ttu-id="54534-119">1: rivela a sinistra; ha origine dal lato destro del frame.</span><span class="sxs-lookup"><span data-stu-id="54534-119">1 - Reveal to the left; originate from the right side of the frame.</span></span></li>
<li><span data-ttu-id="54534-120">2-rivela verso l'alto; originano dalla parte inferiore del frame.</span><span class="sxs-lookup"><span data-stu-id="54534-120">2 - Reveal upward; originate from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="54534-121">3-rivelare verso il basso; originano dalla parte superiore del frame.</span><span class="sxs-lookup"><span data-stu-id="54534-121">3 - Reveal downward; originate from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54534-122">Composizione</span><span class="sxs-lookup"><span data-stu-id="54534-122">Composition</span></span></td>
<td><span data-ttu-id="54534-123"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="54534-123"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="54534-124">Impostare su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="54534-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="54534-125">0: specifica la composizione normale, in cui l'immagine precedente è lo sfondo e l'immagine corrente è il primo piano.</span><span class="sxs-lookup"><span data-stu-id="54534-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="54534-126">1-specifica la composizione invertita, in cui l'immagine corrente è l'immagine di sfondo e l'immagine precedente è il primo piano</span><span class="sxs-lookup"><span data-stu-id="54534-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="54534-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54534-127">Requirements</span></span>



| <span data-ttu-id="54534-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="54534-128">Requirement</span></span> | <span data-ttu-id="54534-129">Valore</span><span class="sxs-lookup"><span data-stu-id="54534-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54534-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54534-130">Header</span></span><br/> | <dl> <span data-ttu-id="54534-131"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54534-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54534-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54534-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54534-133">**Transizioni di immagini video**</span><span class="sxs-lookup"><span data-stu-id="54534-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





