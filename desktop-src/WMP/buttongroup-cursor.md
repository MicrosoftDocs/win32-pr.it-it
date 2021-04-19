---
title: BUTTONGROUP. Cursor
description: L'attributo Cursor specifica o Recupera il tipo di cursore visualizzato quando il mouse è posizionato su un pulsante in BUTTONGROUP.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- Media Player di Windows BUTTONGROUP. Cursor
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329203"
---
# <a name="buttongroupcursor"></a><span data-ttu-id="2bcbc-104">BUTTONGROUP. Cursor</span><span class="sxs-lookup"><span data-stu-id="2bcbc-104">BUTTONGROUP.cursor</span></span>

<span data-ttu-id="2bcbc-105">L'attributo **Cursor** specifica o Recupera il tipo di cursore visualizzato quando il mouse è posizionato su un pulsante in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-105">The **cursor** attribute specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="2bcbc-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="2bcbc-106">Possible Values</span></span>

<span data-ttu-id="2bcbc-107">Questo attributo è una **stringa** di lettura/scrittura contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="2bcbc-108">Valore</span><span class="sxs-lookup"><span data-stu-id="2bcbc-108">Value</span></span>            | <span data-ttu-id="2bcbc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bcbc-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcbc-110">sistema</span><span class="sxs-lookup"><span data-stu-id="2bcbc-110">system</span></span>           | <span data-ttu-id="2bcbc-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-111">Default.</span></span> <span data-ttu-id="2bcbc-112">Cursore dipendente dalla piattaforma (in genere una freccia).</span><span class="sxs-lookup"><span data-stu-id="2bcbc-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="2bcbc-113">a sinistra</span><span class="sxs-lookup"><span data-stu-id="2bcbc-113">hand</span></span>             | <span data-ttu-id="2bcbc-114">A sinistra.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="2bcbc-115">help</span><span class="sxs-lookup"><span data-stu-id="2bcbc-115">help</span></span>             | <span data-ttu-id="2bcbc-116">La freccia con il punto interrogativo che indica la guida è disponibile.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="2bcbc-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="2bcbc-117">sizeall</span></span>          | <span data-ttu-id="2bcbc-118">Freccia a quattro punte che punta a nord, Sud, est e ovest.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="2bcbc-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="2bcbc-119">sizenesw</span></span>         | <span data-ttu-id="2bcbc-120">Freccia a due punte che indica nordest e sud-ovest.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="2bcbc-121">sizens</span><span class="sxs-lookup"><span data-stu-id="2bcbc-121">sizens</span></span>           | <span data-ttu-id="2bcbc-122">Freccia a due punte che punta verso nord e sud.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="2bcbc-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="2bcbc-123">sizenwse</span></span>         | <span data-ttu-id="2bcbc-124">Freccia a due punte che indica nord-ovest e sud-est.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="2bcbc-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="2bcbc-125">sizewe</span></span>           | <span data-ttu-id="2bcbc-126">Freccia a due punte che indica ovest e est.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="2bcbc-127">UpArrow</span><span class="sxs-lookup"><span data-stu-id="2bcbc-127">uparrow</span></span>          | <span data-ttu-id="2bcbc-128">Freccia verticale che punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="2bcbc-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="2bcbc-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="2bcbc-130">Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ).</span><span class="sxs-lookup"><span data-stu-id="2bcbc-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2bcbc-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bcbc-131">Remarks</span></span>

<span data-ttu-id="2bcbc-132">Il cursore specificato si applica a tutti i pulsanti presenti in **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-132">The cursor specified applies to all buttons in the **BUTTONGROUP**.</span></span>

<span data-ttu-id="2bcbc-133">Se si specifica un valore di cursore non valido, rimane in corrispondenza del valore impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-133">If you specify an invalid cursor value, it remains at the previously set value.</span></span>

<span data-ttu-id="2bcbc-134">I percorsi dei nomi di file di cursore vengono ignorati, pertanto il file di cursore deve trovarsi nella directory predefinita.</span><span class="sxs-lookup"><span data-stu-id="2bcbc-134">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bcbc-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bcbc-135">Requirements</span></span>



| <span data-ttu-id="2bcbc-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bcbc-136">Requirement</span></span> | <span data-ttu-id="2bcbc-137">Valore</span><span class="sxs-lookup"><span data-stu-id="2bcbc-137">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2bcbc-138">Versione</span><span class="sxs-lookup"><span data-stu-id="2bcbc-138">Version</span></span><br/> | <span data-ttu-id="2bcbc-139">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="2bcbc-139">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bcbc-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bcbc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcbc-141">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="2bcbc-141">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





