---
description: Contiene i dati binari codificati per un'immagine nel documento Journal, se presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314926"
---
# <a name="image-element"></a><span data-ttu-id="aa382-103">Elemento immagine</span><span class="sxs-lookup"><span data-stu-id="aa382-103">Image Element</span></span>

<span data-ttu-id="aa382-104">Contiene i dati binari codificati per un'immagine nel documento Journal, se presente.</span><span class="sxs-lookup"><span data-stu-id="aa382-104">Contains encoded binary data for an image in the Journal document, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="aa382-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="aa382-105">Definition</span></span>

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a><span data-ttu-id="aa382-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="aa382-106">Parent Elements</span></span>

[<span data-ttu-id="aa382-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="aa382-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="aa382-108">**Nodo del gruppo**</span><span class="sxs-lookup"><span data-stu-id="aa382-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="aa382-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="aa382-109">Child Elements</span></span>

<span data-ttu-id="aa382-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="aa382-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="aa382-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="aa382-111">Attributes</span></span>



| <span data-ttu-id="aa382-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="aa382-112">Attribute</span></span>  | <span data-ttu-id="aa382-113">Type</span><span class="sxs-lookup"><span data-stu-id="aa382-113">Type</span></span>                      | <span data-ttu-id="aa382-114">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="aa382-114">Required</span></span> | <span data-ttu-id="aa382-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa382-115">Description</span></span>                                                                             | <span data-ttu-id="aa382-116">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="aa382-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="aa382-117">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="aa382-117">**Left**</span></span>   | <span data-ttu-id="aa382-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="aa382-118">**xs:integer**</span></span>            | <span data-ttu-id="aa382-119">Necessario</span><span class="sxs-lookup"><span data-stu-id="aa382-119">Required</span></span> | <span data-ttu-id="aa382-120">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="aa382-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="aa382-121">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="aa382-121">Any integer.</span></span>              |
| <span data-ttu-id="aa382-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="aa382-122">**Top**</span></span>    | <span data-ttu-id="aa382-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="aa382-123">**xs:integer**</span></span>            | <span data-ttu-id="aa382-124">Necessario</span><span class="sxs-lookup"><span data-stu-id="aa382-124">Required</span></span> | <span data-ttu-id="aa382-125">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="aa382-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="aa382-126">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="aa382-126">Any integer.</span></span>              |
| <span data-ttu-id="aa382-127">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="aa382-127">**Width**</span></span>  | <span data-ttu-id="aa382-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aa382-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aa382-129">Necessario</span><span class="sxs-lookup"><span data-stu-id="aa382-129">Required</span></span> | <span data-ttu-id="aa382-130">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="aa382-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="aa382-131">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="aa382-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="aa382-132">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="aa382-132">**Height**</span></span> | <span data-ttu-id="aa382-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="aa382-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="aa382-134">Necessario</span><span class="sxs-lookup"><span data-stu-id="aa382-134">Required</span></span> | <span data-ttu-id="aa382-135">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="aa382-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="aa382-136">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="aa382-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="aa382-137">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="aa382-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="aa382-138">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="aa382-138">Element type</span></span> | <span data-ttu-id="aa382-139">ComplexType [**ImageType**](imagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="aa382-139">[**ImageType**](imagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="aa382-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aa382-140">Namespace</span></span>    | <span data-ttu-id="aa382-141">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="aa382-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="aa382-142">Nome schema</span><span class="sxs-lookup"><span data-stu-id="aa382-142">Schema name</span></span>  | <span data-ttu-id="aa382-143">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="aa382-143">Journal Reader</span></span>                                          |



 

## <a name="see-also"></a><span data-ttu-id="aa382-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa382-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa382-145">**Sfondo**</span><span class="sxs-lookup"><span data-stu-id="aa382-145">**Background**</span></span>](background-element.md)
</dt> </dl>

 

 



