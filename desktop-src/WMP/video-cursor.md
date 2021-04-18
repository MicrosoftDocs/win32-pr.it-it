---
title: VIDEO. Cursor
description: L'attributo Cursor specifica o Recupera il valore del cursore utilizzato quando il mouse è posizionato su un'area selezionabile del video.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- Media Player di Windows VIDEO. Cursor
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330453"
---
# <a name="videocursor"></a><span data-ttu-id="0218d-104">VIDEO. Cursor</span><span class="sxs-lookup"><span data-stu-id="0218d-104">VIDEO.cursor</span></span>

<span data-ttu-id="0218d-105">L'attributo **Cursor** specifica o Recupera il valore del cursore utilizzato quando il mouse è posizionato su un'area selezionabile del video.</span><span class="sxs-lookup"><span data-stu-id="0218d-105">The **cursor** attribute specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="0218d-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0218d-106">Possible Values</span></span>

<span data-ttu-id="0218d-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0218d-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="0218d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0218d-108">Value</span></span>            | <span data-ttu-id="0218d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0218d-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0218d-110">sistema</span><span class="sxs-lookup"><span data-stu-id="0218d-110">system</span></span>           | <span data-ttu-id="0218d-111">Cursore dipendente dalla piattaforma (in genere una freccia).</span><span class="sxs-lookup"><span data-stu-id="0218d-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="0218d-112">a sinistra</span><span class="sxs-lookup"><span data-stu-id="0218d-112">hand</span></span>             | <span data-ttu-id="0218d-113">A sinistra.</span><span class="sxs-lookup"><span data-stu-id="0218d-113">Hand.</span></span>                                                                                       |
| <span data-ttu-id="0218d-114">help</span><span class="sxs-lookup"><span data-stu-id="0218d-114">help</span></span>             | <span data-ttu-id="0218d-115">La freccia con il punto interrogativo che indica la guida è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0218d-115">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="0218d-116">sizeall</span><span class="sxs-lookup"><span data-stu-id="0218d-116">sizeall</span></span>          | <span data-ttu-id="0218d-117">Freccia a quattro punte che punta a nord, Sud, est e ovest.</span><span class="sxs-lookup"><span data-stu-id="0218d-117">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="0218d-118">sizenesw</span><span class="sxs-lookup"><span data-stu-id="0218d-118">sizenesw</span></span>         | <span data-ttu-id="0218d-119">Freccia a due punte che indica nordest e sud-ovest.</span><span class="sxs-lookup"><span data-stu-id="0218d-119">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="0218d-120">sizens</span><span class="sxs-lookup"><span data-stu-id="0218d-120">sizens</span></span>           | <span data-ttu-id="0218d-121">Freccia a due punte che punta verso nord e sud.</span><span class="sxs-lookup"><span data-stu-id="0218d-121">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="0218d-122">sizenwse</span><span class="sxs-lookup"><span data-stu-id="0218d-122">sizenwse</span></span>         | <span data-ttu-id="0218d-123">Freccia a due punte che indica nord-ovest e sud-est.</span><span class="sxs-lookup"><span data-stu-id="0218d-123">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="0218d-124">sizewe</span><span class="sxs-lookup"><span data-stu-id="0218d-124">sizewe</span></span>           | <span data-ttu-id="0218d-125">Freccia a due punte che indica ovest e est.</span><span class="sxs-lookup"><span data-stu-id="0218d-125">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="0218d-126">UpArrow</span><span class="sxs-lookup"><span data-stu-id="0218d-126">uparrow</span></span>          | <span data-ttu-id="0218d-127">Freccia verticale che punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="0218d-127">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="0218d-128">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="0218d-128">\*.ani or \*.cur</span></span> | <span data-ttu-id="0218d-129">Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ).</span><span class="sxs-lookup"><span data-stu-id="0218d-129">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0218d-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="0218d-130">Remarks</span></span>

<span data-ttu-id="0218d-131">A scopo di rendering, System è il cursore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0218d-131">For rendering purposes, system is the default cursor.</span></span> <span data-ttu-id="0218d-132">Il valore predefinito recuperato da questo attributo è "" (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="0218d-132">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="0218d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0218d-133">Requirements</span></span>



| <span data-ttu-id="0218d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0218d-134">Requirement</span></span> | <span data-ttu-id="0218d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0218d-135">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0218d-136">Versione</span><span class="sxs-lookup"><span data-stu-id="0218d-136">Version</span></span><br/> | <span data-ttu-id="0218d-137">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="0218d-137">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0218d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0218d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0218d-139">**Elemento VIDEO**</span><span class="sxs-lookup"><span data-stu-id="0218d-139">**VIDEO Element**</span></span>](video-element.md)
</dt> </dl>

 

 





