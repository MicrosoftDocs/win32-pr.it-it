---
description: Contiene contenuto classificato dall'analizzatore o dall'utente come disegno.
ms.assetid: 566542f3-b824-442d-9d8b-0064ebcf9b68
title: Drawing-elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe516a4ba33e6e597b17ce8365d792f19468c3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319573"
---
# <a name="drawing-element"></a><span data-ttu-id="a91dc-103">Drawing-elemento</span><span class="sxs-lookup"><span data-stu-id="a91dc-103">Drawing Element</span></span>

<span data-ttu-id="a91dc-104">Contiene contenuto classificato dall'analizzatore o dall'utente come disegno.</span><span class="sxs-lookup"><span data-stu-id="a91dc-104">Contains content that has been classified by the analyzer or the user as a drawing.</span></span>

## <a name="definition"></a><span data-ttu-id="a91dc-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="a91dc-105">Definition</span></span>

``` syntax
<xs:element name="Drawing" type="DrawingType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="a91dc-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a91dc-106">Parent Elements</span></span>

[<span data-ttu-id="a91dc-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="a91dc-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="a91dc-108">**Nodo del gruppo**</span><span class="sxs-lookup"><span data-stu-id="a91dc-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="a91dc-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a91dc-109">Child Elements</span></span>

[<span data-ttu-id="a91dc-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="a91dc-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="a91dc-111">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="a91dc-111">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="a91dc-112">**InkClass**</span><span class="sxs-lookup"><span data-stu-id="a91dc-112">**InkClass**</span></span>](inkclass-element.md)

[<span data-ttu-id="a91dc-113">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="a91dc-113">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="a91dc-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="a91dc-114">Attributes</span></span>



| <span data-ttu-id="a91dc-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="a91dc-115">Attribute</span></span>  | <span data-ttu-id="a91dc-116">Type</span><span class="sxs-lookup"><span data-stu-id="a91dc-116">Type</span></span>                      | <span data-ttu-id="a91dc-117">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="a91dc-117">Required</span></span> | <span data-ttu-id="a91dc-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a91dc-118">Description</span></span>                                                                             | <span data-ttu-id="a91dc-119">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a91dc-119">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="a91dc-120">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="a91dc-120">**Left**</span></span>   | <span data-ttu-id="a91dc-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a91dc-121">**xs:integer**</span></span>            | <span data-ttu-id="a91dc-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="a91dc-122">Required</span></span> | <span data-ttu-id="a91dc-123">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a91dc-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="a91dc-124">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="a91dc-124">Any integer.</span></span>              |
| <span data-ttu-id="a91dc-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="a91dc-125">**Top**</span></span>    | <span data-ttu-id="a91dc-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a91dc-126">**xs:integer**</span></span>            | <span data-ttu-id="a91dc-127">Necessario</span><span class="sxs-lookup"><span data-stu-id="a91dc-127">Required</span></span> | <span data-ttu-id="a91dc-128">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a91dc-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="a91dc-129">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="a91dc-129">Any integer.</span></span>              |
| <span data-ttu-id="a91dc-130">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="a91dc-130">**Width**</span></span>  | <span data-ttu-id="a91dc-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a91dc-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a91dc-132">Necessario</span><span class="sxs-lookup"><span data-stu-id="a91dc-132">Required</span></span> | <span data-ttu-id="a91dc-133">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a91dc-133">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="a91dc-134">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="a91dc-134">Any non-negative integer.</span></span> |
| <span data-ttu-id="a91dc-135">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="a91dc-135">**Height**</span></span> | <span data-ttu-id="a91dc-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a91dc-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a91dc-137">Necessario</span><span class="sxs-lookup"><span data-stu-id="a91dc-137">Required</span></span> | <span data-ttu-id="a91dc-138">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a91dc-138">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="a91dc-139">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="a91dc-139">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="a91dc-140">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a91dc-140">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="a91dc-141">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a91dc-141">Element type</span></span> | <span data-ttu-id="a91dc-142">ComplexType [**DrawingType**](drawingtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="a91dc-142">[**DrawingType**](drawingtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a91dc-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a91dc-143">Namespace</span></span>    | <span data-ttu-id="a91dc-144">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="a91dc-144">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="a91dc-145">Nome schema</span><span class="sxs-lookup"><span data-stu-id="a91dc-145">Schema name</span></span>  | <span data-ttu-id="a91dc-146">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="a91dc-146">Journal Reader</span></span>                                              |



 

 

 



