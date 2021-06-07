---
description: Contiene informazioni su una determinata parola di input penna nella nota Journal, tra cui posizione, alternative e i dati effettivi dell'input penna.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432393"
---
# <a name="inkword-element"></a><span data-ttu-id="18c91-103">Elemento InkWord</span><span class="sxs-lookup"><span data-stu-id="18c91-103">InkWord Element</span></span>

<span data-ttu-id="18c91-104">Contiene informazioni su una determinata parola di input penna nella nota Journal, tra cui posizione, alternative e i dati effettivi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="18c91-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="18c91-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="18c91-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="18c91-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="18c91-106">Parent Elements</span></span>

[<span data-ttu-id="18c91-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="18c91-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="18c91-108">**A linee**</span><span class="sxs-lookup"><span data-stu-id="18c91-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="18c91-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="18c91-109">Child Elements</span></span>

[<span data-ttu-id="18c91-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="18c91-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="18c91-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="18c91-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="18c91-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="18c91-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="18c91-113">**Attendibilità**</span><span class="sxs-lookup"><span data-stu-id="18c91-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="18c91-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="18c91-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="18c91-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="18c91-115">Attributes</span></span>



| <span data-ttu-id="18c91-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="18c91-116">Attribute</span></span>  | <span data-ttu-id="18c91-117">Type</span><span class="sxs-lookup"><span data-stu-id="18c91-117">Type</span></span>                      | <span data-ttu-id="18c91-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="18c91-118">Required</span></span> | <span data-ttu-id="18c91-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18c91-119">Description</span></span>                                                                             | <span data-ttu-id="18c91-120">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="18c91-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="18c91-121">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="18c91-121">**Left**</span></span>   | <span data-ttu-id="18c91-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="18c91-122">**xs:integer**</span></span>            | <span data-ttu-id="18c91-123">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="18c91-123">Required</span></span> | <span data-ttu-id="18c91-124">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="18c91-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="18c91-125">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="18c91-125">Any integer.</span></span>              |
| <span data-ttu-id="18c91-126">**Top**</span><span class="sxs-lookup"><span data-stu-id="18c91-126">**Top**</span></span>    | <span data-ttu-id="18c91-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="18c91-127">**xs:integer**</span></span>            | <span data-ttu-id="18c91-128">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="18c91-128">Required</span></span> | <span data-ttu-id="18c91-129">Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="18c91-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="18c91-130">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="18c91-130">Any integer.</span></span>              |
| <span data-ttu-id="18c91-131">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="18c91-131">**Width**</span></span>  | <span data-ttu-id="18c91-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="18c91-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="18c91-133">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="18c91-133">Required</span></span> | <span data-ttu-id="18c91-134">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="18c91-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="18c91-135">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="18c91-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="18c91-136">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="18c91-136">**Height**</span></span> | <span data-ttu-id="18c91-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="18c91-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="18c91-138">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="18c91-138">Required</span></span> | <span data-ttu-id="18c91-139">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="18c91-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="18c91-140">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="18c91-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="18c91-141">Il mapping delle coordinate interne della parola input penna è unità metriche inglese e un moltiplicatore di 2,54 dovrà essere usato dall'applicazione per convertire i valori Width e Height nelle unità HIMETRIC usate dalle API della piattaforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="18c91-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="18c91-142">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="18c91-142">Element Information</span></span>



|  <span data-ttu-id="18c91-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="18c91-143">Element</span></span>     | <span data-ttu-id="18c91-144">valore</span><span class="sxs-lookup"><span data-stu-id="18c91-144">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="18c91-145">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="18c91-145">Element type</span></span> | <span data-ttu-id="18c91-146">[**ComplexType InkWordType**](inkwordtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="18c91-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="18c91-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18c91-147">Namespace</span></span>    | <span data-ttu-id="18c91-148">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="18c91-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="18c91-149">Nome schema</span><span class="sxs-lookup"><span data-stu-id="18c91-149">Schema name</span></span>  | <span data-ttu-id="18c91-150">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="18c91-150">Journal Reader</span></span>                                              |



 

 

 



