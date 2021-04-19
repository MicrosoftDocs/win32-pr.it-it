---
title: CUSTOMSLIDER. Cursor
description: L'attributo Cursor specifica o Recupera il valore del cursore del controllo dispositivo di scorrimento visualizzato quando il mouse è posizionato sul dispositivo di scorrimento.
ms.assetid: 965c21ab-18a0-4459-9d5b-0a35ea2c212f
keywords:
- Media Player di Windows CUSTOMSLIDER. Cursor
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e836dc7ec6efececf81789efe43d8b19d0df1783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332686"
---
# <a name="customslidercursor"></a><span data-ttu-id="b48d9-104">CUSTOMSLIDER. Cursor</span><span class="sxs-lookup"><span data-stu-id="b48d9-104">CUSTOMSLIDER.cursor</span></span>

<span data-ttu-id="b48d9-105">L'attributo **Cursor** specifica o Recupera il valore del cursore del controllo dispositivo di scorrimento visualizzato quando il mouse è posizionato sul dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="b48d9-105">The **cursor** attribute specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="b48d9-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="b48d9-106">Possible Values</span></span>

<span data-ttu-id="b48d9-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b48d9-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="b48d9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b48d9-108">Value</span></span>            | <span data-ttu-id="b48d9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b48d9-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b48d9-110">sistema</span><span class="sxs-lookup"><span data-stu-id="b48d9-110">system</span></span>           | <span data-ttu-id="b48d9-111">Cursore dipendente dalla piattaforma (in genere una freccia).</span><span class="sxs-lookup"><span data-stu-id="b48d9-111">Platform-dependent cursor (usually an arrow).</span></span>                                               |
| <span data-ttu-id="b48d9-112">a sinistra</span><span class="sxs-lookup"><span data-stu-id="b48d9-112">hand</span></span>             | <span data-ttu-id="b48d9-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b48d9-113">Default.</span></span> <span data-ttu-id="b48d9-114">Il cursore è una mano.</span><span class="sxs-lookup"><span data-stu-id="b48d9-114">Cursor is a hand.</span></span>                                                                  |
| <span data-ttu-id="b48d9-115">help</span><span class="sxs-lookup"><span data-stu-id="b48d9-115">help</span></span>             | <span data-ttu-id="b48d9-116">La freccia con il punto interrogativo che indica la guida è disponibile.</span><span class="sxs-lookup"><span data-stu-id="b48d9-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="b48d9-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="b48d9-117">sizeall</span></span>          | <span data-ttu-id="b48d9-118">Freccia a quattro punte che punta a nord, Sud, est e ovest.</span><span class="sxs-lookup"><span data-stu-id="b48d9-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="b48d9-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="b48d9-119">sizenesw</span></span>         | <span data-ttu-id="b48d9-120">Freccia a due punte che indica nordest e sud-ovest.</span><span class="sxs-lookup"><span data-stu-id="b48d9-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="b48d9-121">sizens</span><span class="sxs-lookup"><span data-stu-id="b48d9-121">sizens</span></span>           | <span data-ttu-id="b48d9-122">Freccia a due punte che punta verso nord e sud.</span><span class="sxs-lookup"><span data-stu-id="b48d9-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="b48d9-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="b48d9-123">sizenwse</span></span>         | <span data-ttu-id="b48d9-124">Freccia a due punte che indica nord-ovest e sud-est.</span><span class="sxs-lookup"><span data-stu-id="b48d9-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="b48d9-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="b48d9-125">sizewe</span></span>           | <span data-ttu-id="b48d9-126">Freccia a due punte che indica ovest e est.</span><span class="sxs-lookup"><span data-stu-id="b48d9-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="b48d9-127">UpArrow</span><span class="sxs-lookup"><span data-stu-id="b48d9-127">uparrow</span></span>          | <span data-ttu-id="b48d9-128">Freccia verticale che punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="b48d9-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="b48d9-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="b48d9-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="b48d9-130">Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ).</span><span class="sxs-lookup"><span data-stu-id="b48d9-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b48d9-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b48d9-131">Requirements</span></span>



| <span data-ttu-id="b48d9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b48d9-132">Requirement</span></span> | <span data-ttu-id="b48d9-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b48d9-133">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b48d9-134">Versione</span><span class="sxs-lookup"><span data-stu-id="b48d9-134">Version</span></span><br/> | <span data-ttu-id="b48d9-135">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="b48d9-135">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b48d9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b48d9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48d9-137">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="b48d9-137">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





