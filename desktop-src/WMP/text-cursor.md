---
title: TEXT. Cursor
description: L'attributo Cursor specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse si trova sul controllo di testo.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- Media Player di Windows TEXT. Cursor
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325227"
---
# <a name="textcursor"></a><span data-ttu-id="d3cee-104">TEXT. Cursor</span><span class="sxs-lookup"><span data-stu-id="d3cee-104">TEXT.cursor</span></span>

<span data-ttu-id="d3cee-105">L'attributo **Cursor** specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse si trova sul controllo di testo.</span><span class="sxs-lookup"><span data-stu-id="d3cee-105">The **cursor** attribute specifies or retrieves a value indicating which cursor appears when the mouse is over the Text control.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="d3cee-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d3cee-106">Possible Values</span></span>

<span data-ttu-id="d3cee-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d3cee-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="d3cee-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d3cee-108">Value</span></span>            | <span data-ttu-id="d3cee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3cee-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3cee-110">sistema</span><span class="sxs-lookup"><span data-stu-id="d3cee-110">system</span></span>           | <span data-ttu-id="d3cee-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d3cee-111">Default.</span></span> <span data-ttu-id="d3cee-112">Cursore dipendente dalla piattaforma (in genere una freccia).</span><span class="sxs-lookup"><span data-stu-id="d3cee-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="d3cee-113">a sinistra</span><span class="sxs-lookup"><span data-stu-id="d3cee-113">hand</span></span>             | <span data-ttu-id="d3cee-114">A sinistra.</span><span class="sxs-lookup"><span data-stu-id="d3cee-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="d3cee-115">help</span><span class="sxs-lookup"><span data-stu-id="d3cee-115">help</span></span>             | <span data-ttu-id="d3cee-116">La freccia con il punto interrogativo che indica la guida è disponibile.</span><span class="sxs-lookup"><span data-stu-id="d3cee-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="d3cee-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="d3cee-117">sizeall</span></span>          | <span data-ttu-id="d3cee-118">Freccia a quattro punte che punta a nord, Sud, est e ovest.</span><span class="sxs-lookup"><span data-stu-id="d3cee-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="d3cee-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="d3cee-119">sizenesw</span></span>         | <span data-ttu-id="d3cee-120">Freccia a due punte che indica nordest e sud-ovest.</span><span class="sxs-lookup"><span data-stu-id="d3cee-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="d3cee-121">sizens</span><span class="sxs-lookup"><span data-stu-id="d3cee-121">sizens</span></span>           | <span data-ttu-id="d3cee-122">Freccia a due punte che punta verso nord e sud.</span><span class="sxs-lookup"><span data-stu-id="d3cee-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="d3cee-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="d3cee-123">sizenwse</span></span>         | <span data-ttu-id="d3cee-124">Freccia a due punte che indica nord-ovest e sud-est.</span><span class="sxs-lookup"><span data-stu-id="d3cee-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="d3cee-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="d3cee-125">sizewe</span></span>           | <span data-ttu-id="d3cee-126">Freccia a due punte che indica ovest e est.</span><span class="sxs-lookup"><span data-stu-id="d3cee-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="d3cee-127">UpArrow</span><span class="sxs-lookup"><span data-stu-id="d3cee-127">uparrow</span></span>          | <span data-ttu-id="d3cee-128">Freccia verticale che punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="d3cee-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="d3cee-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="d3cee-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="d3cee-130">Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ).</span><span class="sxs-lookup"><span data-stu-id="d3cee-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

<span data-ttu-id="d3cee-131">Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .</span><span class="sxs-lookup"><span data-stu-id="d3cee-131">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3cee-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3cee-132">Requirements</span></span>



| <span data-ttu-id="d3cee-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3cee-133">Requirement</span></span> | <span data-ttu-id="d3cee-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d3cee-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d3cee-135">Versione</span><span class="sxs-lookup"><span data-stu-id="d3cee-135">Version</span></span><br/> | <span data-ttu-id="d3cee-136">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="d3cee-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3cee-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3cee-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3cee-138">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="d3cee-138">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





