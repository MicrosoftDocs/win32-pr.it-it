---
description: Definisce un gruppo che contiene un set di contenuto raggruppato in una nota del journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Gruppo ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057894"
---
# <a name="contentgroup-group"></a><span data-ttu-id="1f87c-103">Gruppo ContentGroup</span><span class="sxs-lookup"><span data-stu-id="1f87c-103">ContentGroup Group</span></span>

<span data-ttu-id="1f87c-104">Definisce un gruppo che contiene un set di contenuto raggruppato in una nota del journal.</span><span class="sxs-lookup"><span data-stu-id="1f87c-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="1f87c-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="1f87c-105">Definition</span></span>

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a><span data-ttu-id="1f87c-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1f87c-106">Child Elements</span></span>

[<span data-ttu-id="1f87c-107">**Nodo del gruppo**</span><span class="sxs-lookup"><span data-stu-id="1f87c-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="1f87c-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="1f87c-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="1f87c-109">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="1f87c-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="1f87c-110">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="1f87c-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="1f87c-111">**Text**</span><span class="sxs-lookup"><span data-stu-id="1f87c-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="1f87c-112">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="1f87c-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="1f87c-113">**Contrassegno**</span><span class="sxs-lookup"><span data-stu-id="1f87c-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="1f87c-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="1f87c-114">Attributes</span></span>



| <span data-ttu-id="1f87c-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="1f87c-115">Attribute</span></span>  | <span data-ttu-id="1f87c-116">Type</span><span class="sxs-lookup"><span data-stu-id="1f87c-116">Type</span></span>                      | <span data-ttu-id="1f87c-117">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="1f87c-117">Required</span></span> | <span data-ttu-id="1f87c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f87c-118">Description</span></span>                                                                                        | <span data-ttu-id="1f87c-119">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="1f87c-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="1f87c-120">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="1f87c-120">**Left**</span></span>   | <span data-ttu-id="1f87c-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="1f87c-121">**xs:integer**</span></span>            | <span data-ttu-id="1f87c-122">Necessario</span><span class="sxs-lookup"><span data-stu-id="1f87c-122">Required</span></span> | <span data-ttu-id="1f87c-123">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1f87c-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="1f87c-124">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="1f87c-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="1f87c-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="1f87c-125">**Top**</span></span>    | <span data-ttu-id="1f87c-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="1f87c-126">**xs:integer**</span></span>            | <span data-ttu-id="1f87c-127">Necessario</span><span class="sxs-lookup"><span data-stu-id="1f87c-127">Required</span></span> | <span data-ttu-id="1f87c-128">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1f87c-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="1f87c-129">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="1f87c-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="1f87c-130">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="1f87c-130">**Width**</span></span>  | <span data-ttu-id="1f87c-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="1f87c-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="1f87c-132">Necessario</span><span class="sxs-lookup"><span data-stu-id="1f87c-132">Required</span></span> | <span data-ttu-id="1f87c-133">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1f87c-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="1f87c-134">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="1f87c-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="1f87c-135">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="1f87c-135">**Height**</span></span> | <span data-ttu-id="1f87c-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="1f87c-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="1f87c-137">Necessario</span><span class="sxs-lookup"><span data-stu-id="1f87c-137">Required</span></span> | <span data-ttu-id="1f87c-138">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1f87c-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="1f87c-139">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="1f87c-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="1f87c-140">Informazioni sul tipo</span><span class="sxs-lookup"><span data-stu-id="1f87c-140">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="1f87c-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1f87c-141">Namespace</span></span>   | <span data-ttu-id="1f87c-142">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="1f87c-142">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="1f87c-143">Nome schema</span><span class="sxs-lookup"><span data-stu-id="1f87c-143">Schema name</span></span> | <span data-ttu-id="1f87c-144">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="1f87c-144">Journal Reader</span></span>                             |



 

 

 




