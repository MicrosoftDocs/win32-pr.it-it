---
description: Definisce un gruppo che contiene un set di contenuto raggruppato in una nota journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Gruppo ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432613"
---
# <a name="contentgroup-group"></a><span data-ttu-id="bce86-103">Gruppo ContentGroup</span><span class="sxs-lookup"><span data-stu-id="bce86-103">ContentGroup Group</span></span>

<span data-ttu-id="bce86-104">Definisce un gruppo che contiene un set di contenuto raggruppato in una nota journal.</span><span class="sxs-lookup"><span data-stu-id="bce86-104">Defines a group that contains a set of grouped content in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="bce86-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="bce86-105">Definition</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="bce86-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bce86-106">Child Elements</span></span>

[<span data-ttu-id="bce86-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="bce86-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="bce86-108">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="bce86-108">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="bce86-109">**Inkword**</span><span class="sxs-lookup"><span data-stu-id="bce86-109">**InkWord**</span></span>](inkword-element.md)

[<span data-ttu-id="bce86-110">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="bce86-110">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="bce86-111">**Text**</span><span class="sxs-lookup"><span data-stu-id="bce86-111">**Text**</span></span>](text-element.md)

[<span data-ttu-id="bce86-112">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="bce86-112">**Image**</span></span>](docimage-element.md)

[<span data-ttu-id="bce86-113">**Bandiera**</span><span class="sxs-lookup"><span data-stu-id="bce86-113">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="bce86-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="bce86-114">Attributes</span></span>



| <span data-ttu-id="bce86-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="bce86-115">Attribute</span></span>  | <span data-ttu-id="bce86-116">Type</span><span class="sxs-lookup"><span data-stu-id="bce86-116">Type</span></span>                      | <span data-ttu-id="bce86-117">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="bce86-117">Required</span></span> | <span data-ttu-id="bce86-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bce86-118">Description</span></span>                                                                                        | <span data-ttu-id="bce86-119">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="bce86-119">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="bce86-120">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="bce86-120">**Left**</span></span>   | <span data-ttu-id="bce86-121">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="bce86-121">**xs:integer**</span></span>            | <span data-ttu-id="bce86-122">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="bce86-122">Required</span></span> | <span data-ttu-id="bce86-123">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="bce86-123">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="bce86-124">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="bce86-124">Any integer.</span></span><br/>              |
| <span data-ttu-id="bce86-125">**Top**</span><span class="sxs-lookup"><span data-stu-id="bce86-125">**Top**</span></span>    | <span data-ttu-id="bce86-126">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="bce86-126">**xs:integer**</span></span>            | <span data-ttu-id="bce86-127">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="bce86-127">Required</span></span> | <span data-ttu-id="bce86-128">Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="bce86-128">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="bce86-129">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="bce86-129">Any integer.</span></span><br/>              |
| <span data-ttu-id="bce86-130">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="bce86-130">**Width**</span></span>  | <span data-ttu-id="bce86-131">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="bce86-131">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="bce86-132">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="bce86-132">Required</span></span> | <span data-ttu-id="bce86-133">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="bce86-133">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="bce86-134">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="bce86-134">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="bce86-135">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="bce86-135">**Height**</span></span> | <span data-ttu-id="bce86-136">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="bce86-136">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="bce86-137">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="bce86-137">Required</span></span> | <span data-ttu-id="bce86-138">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="bce86-138">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="bce86-139">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="bce86-139">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="bce86-140">Informazioni sul tipo</span><span class="sxs-lookup"><span data-stu-id="bce86-140">Type Information</span></span>



|  <span data-ttu-id="bce86-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="bce86-141">Element</span></span>     | <span data-ttu-id="bce86-142">valore</span><span class="sxs-lookup"><span data-stu-id="bce86-142">Value</span></span>                                                     |
|-------------|--------------------------------------------|
| <span data-ttu-id="bce86-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bce86-143">Namespace</span></span>   | <span data-ttu-id="bce86-144">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="bce86-144">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="bce86-145">Nome schema</span><span class="sxs-lookup"><span data-stu-id="bce86-145">Schema name</span></span> | <span data-ttu-id="bce86-146">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="bce86-146">Journal Reader</span></span>                             |



 

 

 




