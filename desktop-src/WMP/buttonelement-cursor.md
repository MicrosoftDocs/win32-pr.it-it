---
title: BUTTONelement. Cursor
description: L'attributo Cursor specifica o Recupera il valore del cursore BUTTONelement visualizzato quando il mouse è posizionato sul pulsante.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- Media Player di Windows BUTTONelement. Cursor
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333759"
---
# <a name="buttonelementcursor"></a><span data-ttu-id="b546f-104">BUTTONelement. Cursor</span><span class="sxs-lookup"><span data-stu-id="b546f-104">BUTTONELEMENT.cursor</span></span>

<span data-ttu-id="b546f-105">L'attributo **Cursor** specifica o Recupera il valore del cursore **ButtonElement** visualizzato quando il mouse è posizionato sul **pulsante**.</span><span class="sxs-lookup"><span data-stu-id="b546f-105">The **cursor** attribute specifies or retrieves the value of the **BUTTONELEMENT** cursor that appears when the mouse is over the **BUTTONELEMENT**.</span></span>

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a><span data-ttu-id="b546f-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="b546f-106">Possible Values</span></span>

<span data-ttu-id="b546f-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b546f-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="b546f-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b546f-108">Value</span></span>            | <span data-ttu-id="b546f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b546f-109">Description</span></span>                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b546f-110">sistema</span><span class="sxs-lookup"><span data-stu-id="b546f-110">system</span></span>           | <span data-ttu-id="b546f-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b546f-111">Default.</span></span> <span data-ttu-id="b546f-112">Cursore dipendente dalla piattaforma (in genere una freccia).</span><span class="sxs-lookup"><span data-stu-id="b546f-112">Platform-dependent cursor (usually an arrow).</span></span>                                      |
| <span data-ttu-id="b546f-113">a sinistra</span><span class="sxs-lookup"><span data-stu-id="b546f-113">hand</span></span>             | <span data-ttu-id="b546f-114">A sinistra.</span><span class="sxs-lookup"><span data-stu-id="b546f-114">Hand.</span></span>                                                                                       |
| <span data-ttu-id="b546f-115">help</span><span class="sxs-lookup"><span data-stu-id="b546f-115">help</span></span>             | <span data-ttu-id="b546f-116">La freccia con il punto interrogativo che indica la guida è disponibile.</span><span class="sxs-lookup"><span data-stu-id="b546f-116">Arrow with question mark indicating Help is available.</span></span>                                      |
| <span data-ttu-id="b546f-117">sizeall</span><span class="sxs-lookup"><span data-stu-id="b546f-117">sizeall</span></span>          | <span data-ttu-id="b546f-118">Freccia a quattro punte che punta a nord, Sud, est e ovest.</span><span class="sxs-lookup"><span data-stu-id="b546f-118">Four-pointed arrow pointing north, south, east, and west.</span></span>                                   |
| <span data-ttu-id="b546f-119">sizenesw</span><span class="sxs-lookup"><span data-stu-id="b546f-119">sizenesw</span></span>         | <span data-ttu-id="b546f-120">Freccia a due punte che indica nordest e sud-ovest.</span><span class="sxs-lookup"><span data-stu-id="b546f-120">Double-pointed arrow pointing northeast and southwest.</span></span>                                      |
| <span data-ttu-id="b546f-121">sizens</span><span class="sxs-lookup"><span data-stu-id="b546f-121">sizens</span></span>           | <span data-ttu-id="b546f-122">Freccia a due punte che punta verso nord e sud.</span><span class="sxs-lookup"><span data-stu-id="b546f-122">Double-pointed arrow pointing north and south.</span></span>                                              |
| <span data-ttu-id="b546f-123">sizenwse</span><span class="sxs-lookup"><span data-stu-id="b546f-123">sizenwse</span></span>         | <span data-ttu-id="b546f-124">Freccia a due punte che indica nord-ovest e sud-est.</span><span class="sxs-lookup"><span data-stu-id="b546f-124">Double-pointed arrow pointing northwest and southeast.</span></span>                                      |
| <span data-ttu-id="b546f-125">sizewe</span><span class="sxs-lookup"><span data-stu-id="b546f-125">sizewe</span></span>           | <span data-ttu-id="b546f-126">Freccia a due punte che indica ovest e est.</span><span class="sxs-lookup"><span data-stu-id="b546f-126">Double-pointed arrow pointing west and east.</span></span>                                                |
| <span data-ttu-id="b546f-127">UpArrow</span><span class="sxs-lookup"><span data-stu-id="b546f-127">uparrow</span></span>          | <span data-ttu-id="b546f-128">Freccia verticale che punta verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="b546f-128">Vertical arrow pointing upward.</span></span>                                                             |
| <span data-ttu-id="b546f-129">\*. ani o \* . cur</span><span class="sxs-lookup"><span data-stu-id="b546f-129">\*.ani or \*.cur</span></span> | <span data-ttu-id="b546f-130">Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ).</span><span class="sxs-lookup"><span data-stu-id="b546f-130">Any .ani or .cur file (must be in the same directory as the .wms file or in the .wmz file).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b546f-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b546f-131">Remarks</span></span>

<span data-ttu-id="b546f-132">Se viene specificato un valore non valido, viene mantenuto il valore precedente.</span><span class="sxs-lookup"><span data-stu-id="b546f-132">If an invalid value is specified, the previous value is maintained.</span></span>

<span data-ttu-id="b546f-133">I percorsi dei nomi di file di cursore vengono ignorati, pertanto il file di cursore deve trovarsi nella directory predefinita.</span><span class="sxs-lookup"><span data-stu-id="b546f-133">Cursor file name paths are ignored, so the cursor file must reside in the default directory.</span></span>

## <a name="requirements"></a><span data-ttu-id="b546f-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b546f-134">Requirements</span></span>



| <span data-ttu-id="b546f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b546f-135">Requirement</span></span> | <span data-ttu-id="b546f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b546f-136">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b546f-137">Versione</span><span class="sxs-lookup"><span data-stu-id="b546f-137">Version</span></span><br/> | <span data-ttu-id="b546f-138">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="b546f-138">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b546f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b546f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b546f-140">**BUTTONelement (elemento)**</span><span class="sxs-lookup"><span data-stu-id="b546f-140">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> </dl>

 

 





