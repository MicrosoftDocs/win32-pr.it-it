---
description: Contiene una bitmap con codifica Base64 di un flag associato alla sezione di una nota journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432330"
---
# <a name="flag-element"></a><span data-ttu-id="79adf-103">Elemento Flag</span><span class="sxs-lookup"><span data-stu-id="79adf-103">Flag Element</span></span>

<span data-ttu-id="79adf-104">Contiene una bitmap con codifica Base64 di un flag associato alla sezione di una nota journal.</span><span class="sxs-lookup"><span data-stu-id="79adf-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="79adf-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="79adf-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="79adf-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="79adf-106">Parent Elements</span></span>

[<span data-ttu-id="79adf-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="79adf-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="79adf-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="79adf-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="79adf-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="79adf-109">Child Elements</span></span>

<span data-ttu-id="79adf-110">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="79adf-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="79adf-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="79adf-111">Attributes</span></span>



| <span data-ttu-id="79adf-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="79adf-112">Attribute</span></span>  | <span data-ttu-id="79adf-113">Type</span><span class="sxs-lookup"><span data-stu-id="79adf-113">Type</span></span>                      | <span data-ttu-id="79adf-114">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="79adf-114">Required</span></span> | <span data-ttu-id="79adf-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79adf-115">Description</span></span>                                                                             | <span data-ttu-id="79adf-116">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="79adf-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="79adf-117">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="79adf-117">**Left**</span></span>   | <span data-ttu-id="79adf-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="79adf-118">**xs:integer**</span></span>            | <span data-ttu-id="79adf-119">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="79adf-119">Required</span></span> | <span data-ttu-id="79adf-120">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="79adf-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="79adf-121">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="79adf-121">Any integer.</span></span>              |
| <span data-ttu-id="79adf-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="79adf-122">**Top**</span></span>    | <span data-ttu-id="79adf-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="79adf-123">**xs:integer**</span></span>            | <span data-ttu-id="79adf-124">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="79adf-124">Required</span></span> | <span data-ttu-id="79adf-125">Distanza tra l'origine e il punto in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="79adf-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="79adf-126">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="79adf-126">Any integer.</span></span>              |
| <span data-ttu-id="79adf-127">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="79adf-127">**Width**</span></span>  | <span data-ttu-id="79adf-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="79adf-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="79adf-129">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="79adf-129">Required</span></span> | <span data-ttu-id="79adf-130">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="79adf-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="79adf-131">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="79adf-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="79adf-132">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="79adf-132">**Height**</span></span> | <span data-ttu-id="79adf-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="79adf-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="79adf-134">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="79adf-134">Required</span></span> | <span data-ttu-id="79adf-135">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="79adf-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="79adf-136">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="79adf-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="79adf-137">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="79adf-137">Element Information</span></span>



|  <span data-ttu-id="79adf-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="79adf-138">Element</span></span>     | <span data-ttu-id="79adf-139">valore</span><span class="sxs-lookup"><span data-stu-id="79adf-139">Value</span></span>                                                     |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="79adf-140">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="79adf-140">Element type</span></span> | <span data-ttu-id="79adf-141">[**complexType FlagType**](flagtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="79adf-141">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="79adf-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="79adf-142">Namespace</span></span>    | <span data-ttu-id="79adf-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="79adf-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="79adf-144">Nome schema</span><span class="sxs-lookup"><span data-stu-id="79adf-144">Schema name</span></span>  | <span data-ttu-id="79adf-145">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="79adf-145">Journal Reader</span></span>                                        |



 

 

 



