---
title: AmbientAttributes. horizontalAlignment
description: L'attributo horizontalAlignment specifica o recupera un valore che indica la posizione orizzontale del controllo quando la visualizzazione o la Sottovisualizzazione padre viene ridimensionata.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Media Player di Windows AmbientAttributes. horizontalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324752"
---
# <a name="ambientattributeshorizontalalignment"></a><span data-ttu-id="288df-104">AmbientAttributes. horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="288df-104">AmbientAttributes.horizontalAlignment</span></span>

<span data-ttu-id="288df-105">L'attributo **HorizontalAlignment** specifica o recupera un valore che indica la posizione orizzontale del controllo quando la **visualizzazione** o la **Sottovisualizzazione** padre viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="288df-105">The **horizontalAlignment** attribute specifies or retrieves a value that indicates the horizontal placement of the control when the **VIEW** or parent **SUBVIEW** is resized.</span></span>

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="288df-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="288df-106">Possible Values</span></span>

<span data-ttu-id="288df-107">Questo attributo è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="288df-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="288df-108">Valore</span><span class="sxs-lookup"><span data-stu-id="288df-108">Value</span></span>   | <span data-ttu-id="288df-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="288df-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="288df-110">sinistro</span><span class="sxs-lookup"><span data-stu-id="288df-110">left</span></span>    | <span data-ttu-id="288df-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="288df-111">Default.</span></span> <span data-ttu-id="288df-112">Mantiene la posizione del controllo rispetto a sinistra della **visualizzazione** o della **Sottovisualizzazione** padre quando la vista viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="288df-112">Maintains the placement of the control relative to the left of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="288df-113">right</span><span class="sxs-lookup"><span data-stu-id="288df-113">right</span></span>   | <span data-ttu-id="288df-114">Mantiene la posizione del controllo rispetto a destra della visualizzazione o della **Sottovisualizzazione** padre quando **la vista viene** ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="288df-114">Maintains the placement of the control relative to the right of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="288df-115">center</span><span class="sxs-lookup"><span data-stu-id="288df-115">center</span></span>  | <span data-ttu-id="288df-116">Mantiene la posizione del controllo in relazione al centro orizzontale della **vista** o della **Sottovisualizzazione** padre quando la visualizzazione viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="288df-116">Maintains the placement of the control relative to the horizontal center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="288df-117">adattamento</span><span class="sxs-lookup"><span data-stu-id="288df-117">stretch</span></span> | <span data-ttu-id="288df-118">Mantiene il posizionamento del controllo in relazione ai margini sinistro e destro della **vista** o della **Sottovisualizzazione** padre quando viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="288df-118">Maintains the placement of the control relative to both the left and right margins of the **VIEW** or parent **SUBVIEW** when resized.</span></span> <span data-ttu-id="288df-119">Il controllo si adatta al momento in cui la **visualizzazione** o la **Sottovisualizzazione** è allungata.</span><span class="sxs-lookup"><span data-stu-id="288df-119">The control stretches to fit when the **VIEW** or **SUBVIEW** is stretched.</span></span> <span data-ttu-id="288df-120">L'immagine effettiva non aumenta o diminuisce a meno che non sia ridimensionabile, ma l'area selezionabile aumenta o diminuisce se non è vincolata da un **clippingImage**.</span><span class="sxs-lookup"><span data-stu-id="288df-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="288df-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="288df-121">Remarks</span></span>

<span data-ttu-id="288df-122">A meno che **HorizontalAlignment** non sia impostato su "Center", il controllo mantiene la distanza originale dal bordo specificato oppure da entrambi i bordi se si specifica "Stretch" e il controllo è ridimensionabile.</span><span class="sxs-lookup"><span data-stu-id="288df-122">Unless **horizontalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="288df-123">Se il controllo non è ridimensionabile e si specifica "Stretch", viene invece estesa l'area selezionabile.</span><span class="sxs-lookup"><span data-stu-id="288df-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="288df-124">È possibile impostare qualsiasi combinazione di **HorizontalAlignment** e **VerticalAlignment**.</span><span class="sxs-lookup"><span data-stu-id="288df-124">You can set any combination of **horizontalAlignment** and **verticalAlignment**.</span></span> <span data-ttu-id="288df-125">Ad esempio, se si desidera centrare un controllo sia orizzontalmente che verticalmente, impostare horizontalAlignment = "Center" verticalAlignment = "Center".</span><span class="sxs-lookup"><span data-stu-id="288df-125">For example, if you want to center a control both horizontally and vertically, set horizontalAlignment="center" verticalAlignment="center".</span></span>

## <a name="requirements"></a><span data-ttu-id="288df-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="288df-126">Requirements</span></span>



| <span data-ttu-id="288df-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="288df-127">Requirement</span></span> | <span data-ttu-id="288df-128">Valore</span><span class="sxs-lookup"><span data-stu-id="288df-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="288df-129">Versione</span><span class="sxs-lookup"><span data-stu-id="288df-129">Version</span></span><br/> | <span data-ttu-id="288df-130">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="288df-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="288df-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="288df-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="288df-132">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="288df-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="288df-133">**AmbientAttributes. verticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="288df-133">**AmbientAttributes.verticalAlignment**</span></span>](ambientattributes-verticalalignment.md)
</dt> <dt>

[<span data-ttu-id="288df-134">**AmbientAttributes.clippingImage**</span><span class="sxs-lookup"><span data-stu-id="288df-134">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





