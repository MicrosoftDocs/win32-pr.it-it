---
description: Definisce un gruppo di attributi utilizzato da un'ampia gamma di elementi in un file journal XML. Contiene gli attributi utilizzati per definire i limiti (Left, top, Height e Width) di un elemento del documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Gruppo di attributi BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749106"
---
# <a name="boundstype-attribute-group"></a><span data-ttu-id="a22e7-104">Gruppo di attributi BoundsType</span><span class="sxs-lookup"><span data-stu-id="a22e7-104">BoundsType Attribute Group</span></span>

<span data-ttu-id="a22e7-105">Definisce un gruppo di attributi utilizzato da un'ampia gamma di elementi in un file journal XML.</span><span class="sxs-lookup"><span data-stu-id="a22e7-105">Defines an attribute group that is used by a variety of elements in a Journal XML file.</span></span> <span data-ttu-id="a22e7-106">Contiene gli attributi utilizzati per definire i limiti (Left, top, Height e Width) di un elemento del documento.</span><span class="sxs-lookup"><span data-stu-id="a22e7-106">It contains attributes used to define the bounds (left, top, height, and width) of an element in the document.</span></span>

## <a name="definition"></a><span data-ttu-id="a22e7-107">Definizione</span><span class="sxs-lookup"><span data-stu-id="a22e7-107">Definition</span></span>

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a><span data-ttu-id="a22e7-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a22e7-108">Child Elements</span></span>

<span data-ttu-id="a22e7-109">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="a22e7-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="a22e7-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="a22e7-110">Attributes</span></span>



| <span data-ttu-id="a22e7-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="a22e7-111">Attribute</span></span>  | <span data-ttu-id="a22e7-112">Type</span><span class="sxs-lookup"><span data-stu-id="a22e7-112">Type</span></span>                      | <span data-ttu-id="a22e7-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="a22e7-113">Required</span></span> | <span data-ttu-id="a22e7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a22e7-114">Description</span></span>                                                                                        | <span data-ttu-id="a22e7-115">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="a22e7-115">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="a22e7-116">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="a22e7-116">**Left**</span></span>   | <span data-ttu-id="a22e7-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a22e7-117">**xs:integer**</span></span>            | <span data-ttu-id="a22e7-118">Necessario</span><span class="sxs-lookup"><span data-stu-id="a22e7-118">Required</span></span> | <span data-ttu-id="a22e7-119">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a22e7-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="a22e7-120">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="a22e7-120">Any integer.</span></span><br/>              |
| <span data-ttu-id="a22e7-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="a22e7-121">**Top**</span></span>    | <span data-ttu-id="a22e7-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="a22e7-122">**xs:integer**</span></span>            | <span data-ttu-id="a22e7-123">Necessario</span><span class="sxs-lookup"><span data-stu-id="a22e7-123">Required</span></span> | <span data-ttu-id="a22e7-124">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a22e7-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="a22e7-125">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="a22e7-125">Any integer.</span></span><br/>              |
| <span data-ttu-id="a22e7-126">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="a22e7-126">**Width**</span></span>  | <span data-ttu-id="a22e7-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a22e7-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a22e7-128">Necessario</span><span class="sxs-lookup"><span data-stu-id="a22e7-128">Required</span></span> | <span data-ttu-id="a22e7-129">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a22e7-129">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="a22e7-130">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="a22e7-130">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="a22e7-131">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="a22e7-131">**Height**</span></span> | <span data-ttu-id="a22e7-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="a22e7-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="a22e7-133">Necessario</span><span class="sxs-lookup"><span data-stu-id="a22e7-133">Required</span></span> | <span data-ttu-id="a22e7-134">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="a22e7-134">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="a22e7-135">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="a22e7-135">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="a22e7-136">Informazioni sul tipo</span><span class="sxs-lookup"><span data-stu-id="a22e7-136">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="a22e7-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a22e7-137">Namespace</span></span>   | <span data-ttu-id="a22e7-138">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="a22e7-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="a22e7-139">Nome schema</span><span class="sxs-lookup"><span data-stu-id="a22e7-139">Schema name</span></span> | <span data-ttu-id="a22e7-140">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="a22e7-140">Journal Reader</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="a22e7-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="a22e7-141">Remarks</span></span>

<span data-ttu-id="a22e7-142">**Left** e **Top** possono essere negativi perché l'origine è definita dai margini e non dalla pagina.</span><span class="sxs-lookup"><span data-stu-id="a22e7-142">**Left** and **Top** can be negative because the origin is defined by the margins, not the page.</span></span>

 

 




