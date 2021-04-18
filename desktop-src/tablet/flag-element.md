---
description: Contiene una bitmap con codifica Base64 di un flag associato alla sezione di una nota del journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307490"
---
# <a name="flag-element"></a><span data-ttu-id="d7a45-103">Flag (elemento)</span><span class="sxs-lookup"><span data-stu-id="d7a45-103">Flag Element</span></span>

<span data-ttu-id="d7a45-104">Contiene una bitmap con codifica Base64 di un flag associato alla sezione di una nota del journal.</span><span class="sxs-lookup"><span data-stu-id="d7a45-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="d7a45-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="d7a45-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="d7a45-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d7a45-106">Parent Elements</span></span>

[<span data-ttu-id="d7a45-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="d7a45-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="d7a45-108">**Nodo del gruppo**</span><span class="sxs-lookup"><span data-stu-id="d7a45-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="d7a45-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d7a45-109">Child Elements</span></span>

<span data-ttu-id="d7a45-110">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="d7a45-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="d7a45-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="d7a45-111">Attributes</span></span>



| <span data-ttu-id="d7a45-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="d7a45-112">Attribute</span></span>  | <span data-ttu-id="d7a45-113">Type</span><span class="sxs-lookup"><span data-stu-id="d7a45-113">Type</span></span>                      | <span data-ttu-id="d7a45-114">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="d7a45-114">Required</span></span> | <span data-ttu-id="d7a45-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7a45-115">Description</span></span>                                                                             | <span data-ttu-id="d7a45-116">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d7a45-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="d7a45-117">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="d7a45-117">**Left**</span></span>   | <span data-ttu-id="d7a45-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="d7a45-118">**xs:integer**</span></span>            | <span data-ttu-id="d7a45-119">Necessario</span><span class="sxs-lookup"><span data-stu-id="d7a45-119">Required</span></span> | <span data-ttu-id="d7a45-120">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d7a45-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="d7a45-121">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="d7a45-121">Any integer.</span></span>              |
| <span data-ttu-id="d7a45-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="d7a45-122">**Top**</span></span>    | <span data-ttu-id="d7a45-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="d7a45-123">**xs:integer**</span></span>            | <span data-ttu-id="d7a45-124">Necessario</span><span class="sxs-lookup"><span data-stu-id="d7a45-124">Required</span></span> | <span data-ttu-id="d7a45-125">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d7a45-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="d7a45-126">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="d7a45-126">Any integer.</span></span>              |
| <span data-ttu-id="d7a45-127">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="d7a45-127">**Width**</span></span>  | <span data-ttu-id="d7a45-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="d7a45-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="d7a45-129">Necessario</span><span class="sxs-lookup"><span data-stu-id="d7a45-129">Required</span></span> | <span data-ttu-id="d7a45-130">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d7a45-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="d7a45-131">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="d7a45-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="d7a45-132">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="d7a45-132">**Height**</span></span> | <span data-ttu-id="d7a45-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="d7a45-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="d7a45-134">Necessario</span><span class="sxs-lookup"><span data-stu-id="d7a45-134">Required</span></span> | <span data-ttu-id="d7a45-135">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d7a45-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="d7a45-136">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="d7a45-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="d7a45-137">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="d7a45-137">Element Information</span></span>



|              |                                                       |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="d7a45-138">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="d7a45-138">Element type</span></span> | <span data-ttu-id="d7a45-139">ComplexType [**FlagType**](flagtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="d7a45-139">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d7a45-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d7a45-140">Namespace</span></span>    | <span data-ttu-id="d7a45-141">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="d7a45-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="d7a45-142">Nome schema</span><span class="sxs-lookup"><span data-stu-id="d7a45-142">Schema name</span></span>  | <span data-ttu-id="d7a45-143">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="d7a45-143">Journal Reader</span></span>                                        |



 

 

 



