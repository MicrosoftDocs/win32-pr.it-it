---
description: Contiene un set di elementi&\# 8212; Paragraph, InkWord, Drawing, text, image o flag&\# 8212; raggruppati nella nota Journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento nodo del gruppo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307485"
---
# <a name="groupnode-element"></a><span data-ttu-id="d816b-103">Elemento nodo del gruppo</span><span class="sxs-lookup"><span data-stu-id="d816b-103">GroupNode Element</span></span>

<span data-ttu-id="d816b-104">Contiene un set di elementi, ovvero [**paragrafi**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md)o [**flag**](flag-element.md), raggruppati nella nota Journal.</span><span class="sxs-lookup"><span data-stu-id="d816b-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="d816b-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="d816b-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="d816b-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d816b-106">Parent Elements</span></span>

[<span data-ttu-id="d816b-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="d816b-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="d816b-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d816b-108">Child Elements</span></span>

[<span data-ttu-id="d816b-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="d816b-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="d816b-110">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="d816b-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="d816b-111">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="d816b-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="d816b-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="d816b-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="d816b-113">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="d816b-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="d816b-114">**Contrassegno**</span><span class="sxs-lookup"><span data-stu-id="d816b-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="d816b-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="d816b-115">Attributes</span></span>



| <span data-ttu-id="d816b-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="d816b-116">Attribute</span></span>  | <span data-ttu-id="d816b-117">Type</span><span class="sxs-lookup"><span data-stu-id="d816b-117">Type</span></span>                      | <span data-ttu-id="d816b-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="d816b-118">Required</span></span> | <span data-ttu-id="d816b-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d816b-119">Description</span></span>                                                                             | <span data-ttu-id="d816b-120">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d816b-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="d816b-121">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="d816b-121">**Left**</span></span>   | <span data-ttu-id="d816b-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="d816b-122">**xs:integer**</span></span>            | <span data-ttu-id="d816b-123">Necessario</span><span class="sxs-lookup"><span data-stu-id="d816b-123">Required</span></span> | <span data-ttu-id="d816b-124">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d816b-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="d816b-125">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="d816b-125">Any integer.</span></span>              |
| <span data-ttu-id="d816b-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="d816b-126">**Top**</span></span>    | <span data-ttu-id="d816b-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="d816b-127">**xs:integer**</span></span>            | <span data-ttu-id="d816b-128">Necessario</span><span class="sxs-lookup"><span data-stu-id="d816b-128">Required</span></span> | <span data-ttu-id="d816b-129">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d816b-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="d816b-130">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="d816b-130">Any integer.</span></span>              |
| <span data-ttu-id="d816b-131">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="d816b-131">**Width**</span></span>  | <span data-ttu-id="d816b-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="d816b-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="d816b-133">Necessario</span><span class="sxs-lookup"><span data-stu-id="d816b-133">Required</span></span> | <span data-ttu-id="d816b-134">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d816b-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="d816b-135">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="d816b-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="d816b-136">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="d816b-136">**Height**</span></span> | <span data-ttu-id="d816b-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="d816b-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="d816b-138">Necessario</span><span class="sxs-lookup"><span data-stu-id="d816b-138">Required</span></span> | <span data-ttu-id="d816b-139">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d816b-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="d816b-140">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="d816b-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="d816b-141">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d816b-141">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="d816b-142">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="d816b-142">Element type</span></span> | <span data-ttu-id="d816b-143">ComplexType [**GroupNodeType**](groupnodetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="d816b-143">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d816b-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d816b-144">Namespace</span></span>    | <span data-ttu-id="d816b-145">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="d816b-145">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="d816b-146">Nome schema</span><span class="sxs-lookup"><span data-stu-id="d816b-146">Schema name</span></span>  | <span data-ttu-id="d816b-147">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="d816b-147">Journal Reader</span></span>                                                  |



 

 

 



