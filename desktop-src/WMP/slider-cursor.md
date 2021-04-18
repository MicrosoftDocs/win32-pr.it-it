---
title: SLIDER. Cursor
description: L'attributo Cursor specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse è posizionato sul controllo Slider.
ms.assetid: 5b96a20c-b3a6-4e08-95b2-32937bb15cc6
keywords:
- Media Player SLIDER. Cursor Windows
topic_type:
- apiref
api_name:
- SLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc8f581d7d087545e666565dd03f649112064d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325122"
---
# <a name="slidercursor"></a><span data-ttu-id="c8673-104">SLIDER. Cursor</span><span class="sxs-lookup"><span data-stu-id="c8673-104">SLIDER.cursor</span></span>

<span data-ttu-id="c8673-105">L'attributo **Cursor** specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse è posizionato sul controllo Slider.</span><span class="sxs-lookup"><span data-stu-id="c8673-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the slider control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="c8673-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c8673-106">Possible Values</span></span>

<span data-ttu-id="c8673-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c8673-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="c8673-108">Valore</span><span class="sxs-lookup"><span data-stu-id="c8673-108">Value</span></span>            | <span data-ttu-id="c8673-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8673-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8673-110">sistema</span><span class="sxs-lookup"><span data-stu-id="c8673-110">system</span></span>           | <span data-ttu-id="c8673-111">Cursore dipendente dalla piattaforma (in genere una freccia).</span><span class="sxs-lookup"><span data-stu-id="c8673-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="c8673-112">a sinistra</span><span class="sxs-lookup"><span data-stu-id="c8673-112">hand</span></span>             | <span data-ttu-id="c8673-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="c8673-113">Default.</span></span> <span data-ttu-id="c8673-114">A sinistra.</span><span class="sxs-lookup"><span data-stu-id="c8673-114">Hand.</span></span>                                                                              |
| <span data-ttu-id="c8673-115">help</span><span class="sxs-lookup"><span data-stu-id="c8673-115">help</span></span>             | <span data-ttu-id="c8673-116">La freccia con il punto interrogativo che indica la guida è disponibile.</span><span class="sxs-lookup"><span data-stu-id="c8673-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="c8673-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="c8673-117">sizeall</span></span>          | <span data-ttu-id="c8673-118">Freccia a quattro punte che punta a nord, Sud, est e ovest.</span><span class="sxs-lookup"><span data-stu-id="c8673-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="c8673-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="c8673-119">sizenesw</span></span>         | <span data-ttu-id="c8673-120">Freccia a due punte che indica nordest e sud-ovest.</span><span class="sxs-lookup"><span data-stu-id="c8673-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="c8673-121">sizens</span><span class="sxs-lookup"><span data-stu-id="c8673-121">sizens</span></span>           | <span data-ttu-id="c8673-122">Freccia a due punte che punta verso nord e sud.</span><span class="sxs-lookup"><span data-stu-id="c8673-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="c8673-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="c8673-123">sizenwse</span></span>         | <span data-ttu-id="c8673-124">Freccia a due punte che indica nord-ovest e sud-est.</span><span class="sxs-lookup"><span data-stu-id="c8673-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="c8673-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="c8673-125">sizewe</span></span>           | <span data-ttu-id="c8673-126">Freccia a due punte che indica ovest e est.</span><span class="sxs-lookup"><span data-stu-id="c8673-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="c8673-127">UpArrow</span><span class="sxs-lookup"><span data-stu-id="c8673-127">uparrow</span></span>          | <span data-ttu-id="c8673-128">Freccia verticale che punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="c8673-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="c8673-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="c8673-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="c8673-130">Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ).</span><span class="sxs-lookup"><span data-stu-id="c8673-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c8673-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8673-131">Requirements</span></span>



| <span data-ttu-id="c8673-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8673-132">Requirement</span></span> | <span data-ttu-id="c8673-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c8673-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c8673-134">Versione</span><span class="sxs-lookup"><span data-stu-id="c8673-134">Version</span></span><br/> | <span data-ttu-id="c8673-135">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="c8673-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8673-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8673-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8673-137">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="c8673-137">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





