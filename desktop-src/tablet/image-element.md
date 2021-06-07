---
description: Contiene dati binari codificati per un'immagine nel documento Journal, se presenti.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9dd3b37a39ce45ee0294f46922fbab376523b64
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432583"
---
# <a name="image-element"></a><span data-ttu-id="fe634-103">Elemento immagine</span><span class="sxs-lookup"><span data-stu-id="fe634-103">Image Element</span></span>

<span data-ttu-id="fe634-104">Contiene dati binari codificati per un'immagine nel documento Journal, se presenti.</span><span class="sxs-lookup"><span data-stu-id="fe634-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="fe634-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="fe634-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="fe634-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="fe634-106">Parent Elements</span></span>

[<span data-ttu-id="fe634-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="fe634-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="fe634-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="fe634-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="fe634-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="fe634-109">Child Elements</span></span>

<span data-ttu-id="fe634-110">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="fe634-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="fe634-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="fe634-111">Attributes</span></span>



| <span data-ttu-id="fe634-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="fe634-112">Attribute</span></span>  | <span data-ttu-id="fe634-113">Type</span><span class="sxs-lookup"><span data-stu-id="fe634-113">Type</span></span>                      | <span data-ttu-id="fe634-114">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="fe634-114">Required</span></span> | <span data-ttu-id="fe634-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe634-115">Description</span></span>                                                                             | <span data-ttu-id="fe634-116">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="fe634-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="fe634-117">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="fe634-117">**Left**</span></span>   | <span data-ttu-id="fe634-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="fe634-118">**xs:integer**</span></span>            | <span data-ttu-id="fe634-119">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="fe634-119">Required</span></span> | <span data-ttu-id="fe634-120">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="fe634-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="fe634-121">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="fe634-121">Any integer.</span></span>              |
| <span data-ttu-id="fe634-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="fe634-122">**Top**</span></span>    | <span data-ttu-id="fe634-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="fe634-123">**xs:integer**</span></span>            | <span data-ttu-id="fe634-124">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="fe634-124">Required</span></span> | <span data-ttu-id="fe634-125">Distanza tra l'origine e il punto in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="fe634-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="fe634-126">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="fe634-126">Any integer.</span></span>              |
| <span data-ttu-id="fe634-127">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="fe634-127">**Width**</span></span>  | <span data-ttu-id="fe634-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fe634-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fe634-129">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="fe634-129">Required</span></span> | <span data-ttu-id="fe634-130">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="fe634-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="fe634-131">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="fe634-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="fe634-132">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="fe634-132">**Height**</span></span> | <span data-ttu-id="fe634-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="fe634-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="fe634-134">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="fe634-134">Required</span></span> | <span data-ttu-id="fe634-135">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="fe634-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="fe634-136">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="fe634-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="fe634-137">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="fe634-137">Element Information</span></span>



|  <span data-ttu-id="fe634-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="fe634-138">Element</span></span>     | <span data-ttu-id="fe634-139">valore</span><span class="sxs-lookup"><span data-stu-id="fe634-139">Value</span></span>                                                     |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="fe634-140">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="fe634-140">Element type</span></span> | <span data-ttu-id="fe634-141">[**complexType ImageType**](imagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="fe634-141">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="fe634-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe634-142">Namespace</span></span>    | <span data-ttu-id="fe634-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="fe634-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="fe634-144">Nome schema</span><span class="sxs-lookup"><span data-stu-id="fe634-144">Schema name</span></span>  | <span data-ttu-id="fe634-145">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="fe634-145">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="fe634-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe634-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe634-147">**Sfondo**</span><span class="sxs-lookup"><span data-stu-id="fe634-147">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



