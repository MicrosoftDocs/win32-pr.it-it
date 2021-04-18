---
title: AmbientAttributes. verticalAlignment
description: L'attributo verticalAlignment specifica o recupera un valore che indica la posizione verticale del controllo quando la visualizzazione o la Sottovisualizzazione padre è allungata.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Media Player Windows AmbientAttributes. verticalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332142"
---
# <a name="ambientattributesverticalalignment"></a><span data-ttu-id="8f3fb-104">AmbientAttributes. verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="8f3fb-104">AmbientAttributes.verticalAlignment</span></span>

<span data-ttu-id="8f3fb-105">L'attributo **VerticalAlignment** specifica o recupera un valore che indica la posizione verticale del controllo quando la **visualizzazione** o la **Sottovisualizzazione** padre è allungata.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-105">The **verticalAlignment** attribute specifies or retrieves a value indicating the vertical placement of the control when the **VIEW** or parent **SUBVIEW** is stretched.</span></span>

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="8f3fb-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="8f3fb-106">Possible Values</span></span>

<span data-ttu-id="8f3fb-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="8f3fb-108">Valore</span><span class="sxs-lookup"><span data-stu-id="8f3fb-108">Value</span></span>   | <span data-ttu-id="8f3fb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f3fb-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3fb-110">top</span><span class="sxs-lookup"><span data-stu-id="8f3fb-110">top</span></span>     | <span data-ttu-id="8f3fb-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-111">Default.</span></span> <span data-ttu-id="8f3fb-112">Mantiene la posizione del controllo rispetto alla parte superiore della **visualizzazione** o della **Sottovisualizzazione** padre quando la vista viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-112">Maintains the placement of the control relative to the top of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="8f3fb-113">bottom</span><span class="sxs-lookup"><span data-stu-id="8f3fb-113">bottom</span></span>  | <span data-ttu-id="8f3fb-114">Mantiene la posizione del controllo rispetto alla parte inferiore della **visualizzazione** o della **Sottovisualizzazione** padre quando la vista viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-114">Maintains the placement of the control relative to the bottom of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="8f3fb-115">center</span><span class="sxs-lookup"><span data-stu-id="8f3fb-115">center</span></span>  | <span data-ttu-id="8f3fb-116">Mantiene il posizionamento del controllo in relazione al centro verticale della **visualizzazione** o della **Sottovisualizzazione** padre quando la visualizzazione viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-116">Maintains the placement of the control relative to the vertical center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="8f3fb-117">adattamento</span><span class="sxs-lookup"><span data-stu-id="8f3fb-117">stretch</span></span> | <span data-ttu-id="8f3fb-118">Mantiene la posizione del controllo rispetto ai margini superiore e inferiore della visualizzazione quando viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-118">Maintains the placement of the control relative to both the top and bottom margins of the View when resized.</span></span> <span data-ttu-id="8f3fb-119">Il controllo si adatta al momento in cui la **visualizzazione** o la **Sottovisualizzazione** padre è allungata.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-119">The control stretches to fit when the **VIEW** or parent **SUBVIEW** is stretched.</span></span> <span data-ttu-id="8f3fb-120">L'immagine effettiva non aumenta o diminuisce a meno che non sia ridimensionabile, ma l'area selezionabile aumenta o diminuisce se non è vincolata da un **clippingImage**.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8f3fb-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f3fb-121">Remarks</span></span>

<span data-ttu-id="8f3fb-122">A meno che **VerticalAlignment** non sia impostato su "Center", il controllo mantiene la distanza originale dal bordo specificato oppure da entrambi i bordi se viene specificato "Stretch" e il controllo è ridimensionabile.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-122">Unless **verticalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="8f3fb-123">Se il controllo non è ridimensionabile e si specifica "Stretch", viene invece estesa l'area selezionabile.</span><span class="sxs-lookup"><span data-stu-id="8f3fb-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="8f3fb-124">È possibile impostare qualsiasi combinazione degli attributi **HorizontalAlignment** e **VerticalAlignment** .</span><span class="sxs-lookup"><span data-stu-id="8f3fb-124">You can set any combination of the **horizontalAlignment** and **verticalAlignment** attributes.</span></span> <span data-ttu-id="8f3fb-125">Se ad esempio si desidera che un controllo sia centrato orizzontalmente e verticalmente, impostare **HorizontalAlignment** su "Center" e **VerticalAlignment** su "Center".</span><span class="sxs-lookup"><span data-stu-id="8f3fb-125">For example, if you want a control to be centered both horizontally and vertically, set **horizontalAlignment** to "center" and **verticalAlignment** to "center".</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3fb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f3fb-126">Requirements</span></span>



| <span data-ttu-id="8f3fb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f3fb-127">Requirement</span></span> | <span data-ttu-id="8f3fb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8f3fb-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8f3fb-129">Versione</span><span class="sxs-lookup"><span data-stu-id="8f3fb-129">Version</span></span><br/> | <span data-ttu-id="8f3fb-130">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="8f3fb-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f3fb-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f3fb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3fb-132">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="8f3fb-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f3fb-133">**AmbientAttributes. horizontalAlignment**</span><span class="sxs-lookup"><span data-stu-id="8f3fb-133">**AmbientAttributes.horizontalAlignment**</span></span>](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





