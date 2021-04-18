---
title: BUTTON. Cursor
description: L'attributo Cursor specifica o Recupera il cursore visualizzato quando il puntatore del mouse viene posizionato sul pulsante.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- BUTTON. Cursor Media Player Windows
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327073"
---
# <a name="buttoncursor"></a><span data-ttu-id="1d939-104">BUTTON. Cursor</span><span class="sxs-lookup"><span data-stu-id="1d939-104">BUTTON.cursor</span></span>

<span data-ttu-id="1d939-105">L'attributo **Cursor** specifica o Recupera il cursore visualizzato quando il puntatore del mouse viene posizionato sul **pulsante**.</span><span class="sxs-lookup"><span data-stu-id="1d939-105">The **cursor** attribute specifies or retrieves the cursor that appears when the mouse pointer hovers over the **BUTTON**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="1d939-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1d939-106">Possible Values</span></span>

<span data-ttu-id="1d939-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1d939-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="1d939-108">Valore</span><span class="sxs-lookup"><span data-stu-id="1d939-108">Value</span></span>            | <span data-ttu-id="1d939-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d939-109">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d939-110">sistema</span><span class="sxs-lookup"><span data-stu-id="1d939-110">system</span></span>           | <span data-ttu-id="1d939-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1d939-111">Default.</span></span> <span data-ttu-id="1d939-112">Cursore dipendente dalla piattaforma (in genere una freccia).</span><span class="sxs-lookup"><span data-stu-id="1d939-112">Platform-dependent cursor (usually an arrow).</span></span>                                     |
| <span data-ttu-id="1d939-113">a sinistra</span><span class="sxs-lookup"><span data-stu-id="1d939-113">hand</span></span>             | <span data-ttu-id="1d939-114">A sinistra.</span><span class="sxs-lookup"><span data-stu-id="1d939-114">Hand.</span></span>                                                                                      |
| <span data-ttu-id="1d939-115">help</span><span class="sxs-lookup"><span data-stu-id="1d939-115">help</span></span>             | <span data-ttu-id="1d939-116">La freccia con il punto interrogativo che indica la guida è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1d939-116">Arrow with question mark indicating Help is available.</span></span>                                     |
| <span data-ttu-id="1d939-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="1d939-117">sizeall</span></span>          | <span data-ttu-id="1d939-118">Freccia a quattro punte che punta a nord, Sud, est e ovest.</span><span class="sxs-lookup"><span data-stu-id="1d939-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                  |
| <span data-ttu-id="1d939-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="1d939-119">sizenesw</span></span>         | <span data-ttu-id="1d939-120">Freccia a due punte che indica nordest e sud-ovest.</span><span class="sxs-lookup"><span data-stu-id="1d939-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                     |
| <span data-ttu-id="1d939-121">sizens</span><span class="sxs-lookup"><span data-stu-id="1d939-121">sizens</span></span>           | <span data-ttu-id="1d939-122">Freccia a due punte che punta verso nord e sud.</span><span class="sxs-lookup"><span data-stu-id="1d939-122">Double-pointed arrow pointing north and south.</span></span>                                             |
| <span data-ttu-id="1d939-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="1d939-123">sizenwse</span></span>         | <span data-ttu-id="1d939-124">Freccia a due punte che indica nord-ovest e sud-est.</span><span class="sxs-lookup"><span data-stu-id="1d939-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                     |
| <span data-ttu-id="1d939-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="1d939-125">sizewe</span></span>           | <span data-ttu-id="1d939-126">Freccia a due punte che indica ovest e est.</span><span class="sxs-lookup"><span data-stu-id="1d939-126">Double-pointed arrow pointing west and east.</span></span>                                               |
| <span data-ttu-id="1d939-127">UpArrow</span><span class="sxs-lookup"><span data-stu-id="1d939-127">uparrow</span></span>          | <span data-ttu-id="1d939-128">Freccia verticale che punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="1d939-128">Vertical arrow pointing upward.</span></span>                                                            |
| <span data-ttu-id="1d939-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="1d939-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="1d939-130">Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ)</span><span class="sxs-lookup"><span data-stu-id="1d939-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1d939-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d939-131">Remarks</span></span>

<span data-ttu-id="1d939-132">Se il sistema non riconosce il valore del cursore specificato, il valore del cursore rimane in corrispondenza del valore impostato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1d939-132">If the system does not recognize the cursor value specified, the cursor value remains at the previously set value.</span></span>

<span data-ttu-id="1d939-133">I percorsi dei nomi di file di cursore vengono ignorati, pertanto il file di cursore deve trovarsi nella directory predefinita.</span><span class="sxs-lookup"><span data-stu-id="1d939-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d939-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d939-134">Requirements</span></span>



| <span data-ttu-id="1d939-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d939-135">Requirement</span></span> | <span data-ttu-id="1d939-136">Valore</span><span class="sxs-lookup"><span data-stu-id="1d939-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1d939-137">Versione</span><span class="sxs-lookup"><span data-stu-id="1d939-137">Version</span></span><br/> | <span data-ttu-id="1d939-138">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="1d939-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d939-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d939-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d939-140">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="1d939-140">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





