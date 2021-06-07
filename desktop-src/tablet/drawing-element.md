---
description: Contiene contenuto classificato dall'analizzatore o dall'utente come disegno.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Elemento Drawing
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87c0a3d8879fb5f3146c46c9c88d83a6e658d8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432513"
---
# <a name="drawing-element"></a><span data-ttu-id="60844-103">Elemento Drawing</span><span class="sxs-lookup"><span data-stu-id="60844-103">Drawing Element</span></span>

<span data-ttu-id="60844-104">Contiene contenuto classificato dall'analizzatore o dall'utente come disegno.</span><span class="sxs-lookup"><span data-stu-id="60844-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="60844-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="60844-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="60844-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="60844-106">Parent Elements</span></span>

[<span data-ttu-id="60844-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="60844-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="60844-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="60844-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="60844-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="60844-109">Child Elements</span></span>

[<span data-ttu-id="60844-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="60844-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="60844-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="60844-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="60844-112">**Classe InkClass**</span><span class="sxs-lookup"><span data-stu-id="60844-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="60844-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="60844-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="60844-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="60844-114">Attributes</span></span>



| <span data-ttu-id="60844-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="60844-115">Attribute</span></span>  | <span data-ttu-id="60844-116">Type</span><span class="sxs-lookup"><span data-stu-id="60844-116">Type</span></span>                      | <span data-ttu-id="60844-117">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="60844-117">Required</span></span> | <span data-ttu-id="60844-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60844-118">Description</span></span>                                                                             | <span data-ttu-id="60844-119">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="60844-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="60844-120">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="60844-120">**Left**</span></span>   | <span data-ttu-id="60844-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="60844-121">**xs:integer**</span></span>            | <span data-ttu-id="60844-122">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="60844-122">Required</span></span> | <span data-ttu-id="60844-123">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="60844-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="60844-124">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="60844-124">Any integer.</span></span>              |
| <span data-ttu-id="60844-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="60844-125">**Top**</span></span>    | <span data-ttu-id="60844-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="60844-126">**xs:integer**</span></span>            | <span data-ttu-id="60844-127">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="60844-127">Required</span></span> | <span data-ttu-id="60844-128">Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="60844-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="60844-129">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="60844-129">Any integer.</span></span>              |
| <span data-ttu-id="60844-130">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="60844-130">**Width**</span></span>  | <span data-ttu-id="60844-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="60844-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="60844-132">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="60844-132">Required</span></span> | <span data-ttu-id="60844-133">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="60844-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="60844-134">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="60844-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="60844-135">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="60844-135">**Height**</span></span> | <span data-ttu-id="60844-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="60844-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="60844-137">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="60844-137">Required</span></span> | <span data-ttu-id="60844-138">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="60844-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="60844-139">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="60844-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="60844-140">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="60844-140">Element Information</span></span>



|  <span data-ttu-id="60844-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="60844-141">Element</span></span>     | <span data-ttu-id="60844-142">valore</span><span class="sxs-lookup"><span data-stu-id="60844-142">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="60844-143">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="60844-143">Element type</span></span> | <span data-ttu-id="60844-144">[**ComplexType DrawingType**](drawingtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="60844-144">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="60844-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="60844-145">Namespace</span></span>    | <span data-ttu-id="60844-146">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="60844-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="60844-147">Nome schema</span><span class="sxs-lookup"><span data-stu-id="60844-147">Schema name</span></span>  | <span data-ttu-id="60844-148">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="60844-148">Journal Reader</span></span>                                              |



 

 

 



