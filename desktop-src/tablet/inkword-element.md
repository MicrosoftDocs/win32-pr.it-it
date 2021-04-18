---
description: Contiene informazioni su una parola input penna specificata nella nota Journal, incluse la posizione, le alternative e i dati effettivi sull'input penna.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313459"
---
# <a name="inkword-element"></a><span data-ttu-id="d9661-103">Elemento InkWord</span><span class="sxs-lookup"><span data-stu-id="d9661-103">InkWord Element</span></span>

<span data-ttu-id="d9661-104">Contiene informazioni su una parola input penna specificata nella nota Journal, incluse la posizione, le alternative e i dati effettivi sull'input penna.</span><span class="sxs-lookup"><span data-stu-id="d9661-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="d9661-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="d9661-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="d9661-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d9661-106">Parent Elements</span></span>

[<span data-ttu-id="d9661-107">**Nodo del gruppo**</span><span class="sxs-lookup"><span data-stu-id="d9661-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="d9661-108">**Linea**</span><span class="sxs-lookup"><span data-stu-id="d9661-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="d9661-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d9661-109">Child Elements</span></span>

[<span data-ttu-id="d9661-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="d9661-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="d9661-111">**Alternativa**</span><span class="sxs-lookup"><span data-stu-id="d9661-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="d9661-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="d9661-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="d9661-113">**Attendibilità**</span><span class="sxs-lookup"><span data-stu-id="d9661-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="d9661-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="d9661-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="d9661-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="d9661-115">Attributes</span></span>



| <span data-ttu-id="d9661-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="d9661-116">Attribute</span></span>  | <span data-ttu-id="d9661-117">Type</span><span class="sxs-lookup"><span data-stu-id="d9661-117">Type</span></span>                      | <span data-ttu-id="d9661-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="d9661-118">Required</span></span> | <span data-ttu-id="d9661-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9661-119">Description</span></span>                                                                             | <span data-ttu-id="d9661-120">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d9661-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="d9661-121">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="d9661-121">**Left**</span></span>   | <span data-ttu-id="d9661-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="d9661-122">**xs:integer**</span></span>            | <span data-ttu-id="d9661-123">Necessario</span><span class="sxs-lookup"><span data-stu-id="d9661-123">Required</span></span> | <span data-ttu-id="d9661-124">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d9661-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="d9661-125">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="d9661-125">Any integer.</span></span>              |
| <span data-ttu-id="d9661-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="d9661-126">**Top**</span></span>    | <span data-ttu-id="d9661-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="d9661-127">**xs:integer**</span></span>            | <span data-ttu-id="d9661-128">Necessario</span><span class="sxs-lookup"><span data-stu-id="d9661-128">Required</span></span> | <span data-ttu-id="d9661-129">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d9661-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="d9661-130">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="d9661-130">Any integer.</span></span>              |
| <span data-ttu-id="d9661-131">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="d9661-131">**Width**</span></span>  | <span data-ttu-id="d9661-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="d9661-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="d9661-133">Necessario</span><span class="sxs-lookup"><span data-stu-id="d9661-133">Required</span></span> | <span data-ttu-id="d9661-134">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d9661-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="d9661-135">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="d9661-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="d9661-136">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="d9661-136">**Height**</span></span> | <span data-ttu-id="d9661-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="d9661-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="d9661-138">Necessario</span><span class="sxs-lookup"><span data-stu-id="d9661-138">Required</span></span> | <span data-ttu-id="d9661-139">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d9661-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="d9661-140">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="d9661-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="d9661-141">Il mapping delle coordinate interne di Word Ink è costituito da unità metriche inglesi e un moltiplicatore di 2,54 deve essere usato dall'applicazione per convertire i valori di larghezza e altezza nelle unità HIMETRIC usate dalle API della piattaforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="d9661-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="d9661-142">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d9661-142">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="d9661-143">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="d9661-143">Element type</span></span> | <span data-ttu-id="d9661-144">ComplexType [**InkWordType**](inkwordtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="d9661-144">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d9661-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d9661-145">Namespace</span></span>    | <span data-ttu-id="d9661-146">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="d9661-146">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="d9661-147">Nome schema</span><span class="sxs-lookup"><span data-stu-id="d9661-147">Schema name</span></span>  | <span data-ttu-id="d9661-148">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="d9661-148">Journal Reader</span></span>                                              |



 

 

 



