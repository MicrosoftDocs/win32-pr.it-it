---
description: Contiene un set di elementi&\# 8212; Paragraph, InkWord, Drawing, Text, Image o Flag&\# 8212; raggruppati nella nota Journal.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento GroupNode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432572"
---
# <a name="groupnode-element"></a><span data-ttu-id="66aa0-103">Elemento GroupNode</span><span class="sxs-lookup"><span data-stu-id="66aa0-103">GroupNode Element</span></span>

<span data-ttu-id="66aa0-104">Contiene un set di elementi,[**Paragraph,**](paragraph-element.md) [**InkWord,**](inkword-element.md) [**Drawing,**](drawing-element.md) [**Text,**](text-element.md) [**Image**](image-element.md)o [**Flag,**](flag-element.md)raggruppati nella nota Journal.</span><span class="sxs-lookup"><span data-stu-id="66aa0-104">Contains a set of elements—[**Paragraph**](paragraph-element.md), [**InkWord**](inkword-element.md), [**Drawing**](drawing-element.md), [**Text**](text-element.md), [**Image**](image-element.md), or [**Flag**](flag-element.md)—that are grouped together in the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="66aa0-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="66aa0-105">Definition</span></span>

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a><span data-ttu-id="66aa0-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="66aa0-106">Parent Elements</span></span>

[<span data-ttu-id="66aa0-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="66aa0-107">**Content**</span></span>](content-element--journal-reader.md)

## <a name="child-elements"></a><span data-ttu-id="66aa0-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="66aa0-108">Child Elements</span></span>

[<span data-ttu-id="66aa0-109">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="66aa0-109">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="66aa0-110">**Inkword**</span><span class="sxs-lookup"><span data-stu-id="66aa0-110">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="66aa0-111">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="66aa0-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="66aa0-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="66aa0-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="66aa0-113">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="66aa0-113">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="66aa0-114">**Bandiera**</span><span class="sxs-lookup"><span data-stu-id="66aa0-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="66aa0-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="66aa0-115">Attributes</span></span>



| <span data-ttu-id="66aa0-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="66aa0-116">Attribute</span></span>  | <span data-ttu-id="66aa0-117">Type</span><span class="sxs-lookup"><span data-stu-id="66aa0-117">Type</span></span>                      | <span data-ttu-id="66aa0-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="66aa0-118">Required</span></span> | <span data-ttu-id="66aa0-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66aa0-119">Description</span></span>                                                                             | <span data-ttu-id="66aa0-120">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="66aa0-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="66aa0-121">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="66aa0-121">**Left**</span></span>   | <span data-ttu-id="66aa0-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="66aa0-122">**xs:integer**</span></span>            | <span data-ttu-id="66aa0-123">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="66aa0-123">Required</span></span> | <span data-ttu-id="66aa0-124">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="66aa0-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="66aa0-125">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="66aa0-125">Any integer.</span></span>              |
| <span data-ttu-id="66aa0-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="66aa0-126">**Top**</span></span>    | <span data-ttu-id="66aa0-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="66aa0-127">**xs:integer**</span></span>            | <span data-ttu-id="66aa0-128">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="66aa0-128">Required</span></span> | <span data-ttu-id="66aa0-129">Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="66aa0-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="66aa0-130">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="66aa0-130">Any integer.</span></span>              |
| <span data-ttu-id="66aa0-131">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="66aa0-131">**Width**</span></span>  | <span data-ttu-id="66aa0-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="66aa0-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="66aa0-133">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="66aa0-133">Required</span></span> | <span data-ttu-id="66aa0-134">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="66aa0-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="66aa0-135">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="66aa0-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="66aa0-136">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="66aa0-136">**Height**</span></span> | <span data-ttu-id="66aa0-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="66aa0-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="66aa0-138">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="66aa0-138">Required</span></span> | <span data-ttu-id="66aa0-139">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="66aa0-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="66aa0-140">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="66aa0-140">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="66aa0-141">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="66aa0-141">Element Information</span></span>



|  <span data-ttu-id="66aa0-142">Elemento</span><span class="sxs-lookup"><span data-stu-id="66aa0-142">Element</span></span>     | <span data-ttu-id="66aa0-143">valore</span><span class="sxs-lookup"><span data-stu-id="66aa0-143">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="66aa0-144">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="66aa0-144">Element type</span></span> | <span data-ttu-id="66aa0-145">[**ComplexType GroupNodeType**](groupnodetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="66aa0-145">[**GroupNodeType**](groupnodetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="66aa0-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="66aa0-146">Namespace</span></span>    | <span data-ttu-id="66aa0-147">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="66aa0-147">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="66aa0-148">Nome schema</span><span class="sxs-lookup"><span data-stu-id="66aa0-148">Schema name</span></span>  | <span data-ttu-id="66aa0-149">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="66aa0-149">Journal Reader</span></span>                                                  |



 

 

 



