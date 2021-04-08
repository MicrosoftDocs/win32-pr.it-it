---
description: Contiene informazioni sul testo della nota Journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968416"
---
# <a name="text-element"></a><span data-ttu-id="69f07-103">Elemento Text</span><span class="sxs-lookup"><span data-stu-id="69f07-103">Text Element</span></span>

<span data-ttu-id="69f07-104">Contiene informazioni sul testo della nota Journal.</span><span class="sxs-lookup"><span data-stu-id="69f07-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="69f07-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="69f07-105">Definition</span></span>

<span data-ttu-id="69f07-106">Se usato con [**contenuto**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="69f07-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="69f07-107">In alternativa, se usato con [**TitleInfo**](titleinfo-element.md) e [**nodo del gruppo**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="69f07-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="69f07-108">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="69f07-108">Parent Elements</span></span>

[<span data-ttu-id="69f07-109">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="69f07-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="69f07-110">**Nodo del gruppo**</span><span class="sxs-lookup"><span data-stu-id="69f07-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="69f07-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="69f07-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="69f07-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="69f07-112">Child Elements</span></span>

<span data-ttu-id="69f07-113">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="69f07-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="69f07-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="69f07-114">Attributes</span></span>

<span data-ttu-id="69f07-115">Non sono presenti attributi se usati con [**TitleInfo**](titleinfo-element.md) e [**nodo del gruppo**](groupnode-element.md).</span><span class="sxs-lookup"><span data-stu-id="69f07-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="69f07-116">Quando viene usato con il [**contenuto**](content-element--journal-reader.md), gli attributi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="69f07-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="69f07-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="69f07-117">Attribute</span></span>  | <span data-ttu-id="69f07-118">Type</span><span class="sxs-lookup"><span data-stu-id="69f07-118">Type</span></span>                      | <span data-ttu-id="69f07-119">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="69f07-119">Required</span></span> | <span data-ttu-id="69f07-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69f07-120">Description</span></span>                                                                             | <span data-ttu-id="69f07-121">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="69f07-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="69f07-122">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="69f07-122">**Left**</span></span>   | <span data-ttu-id="69f07-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="69f07-123">**xs:integer**</span></span>            | <span data-ttu-id="69f07-124">Necessario</span><span class="sxs-lookup"><span data-stu-id="69f07-124">Required</span></span> | <span data-ttu-id="69f07-125">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="69f07-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="69f07-126">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="69f07-126">Any integer.</span></span>              |
| <span data-ttu-id="69f07-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="69f07-127">**Top**</span></span>    | <span data-ttu-id="69f07-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="69f07-128">**xs:integer**</span></span>            | <span data-ttu-id="69f07-129">Necessario</span><span class="sxs-lookup"><span data-stu-id="69f07-129">Required</span></span> | <span data-ttu-id="69f07-130">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="69f07-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="69f07-131">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="69f07-131">Any integer.</span></span>              |
| <span data-ttu-id="69f07-132">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="69f07-132">**Width**</span></span>  | <span data-ttu-id="69f07-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="69f07-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="69f07-134">Necessario</span><span class="sxs-lookup"><span data-stu-id="69f07-134">Required</span></span> | <span data-ttu-id="69f07-135">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="69f07-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="69f07-136">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="69f07-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="69f07-137">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="69f07-137">**Height**</span></span> | <span data-ttu-id="69f07-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="69f07-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="69f07-139">Necessario</span><span class="sxs-lookup"><span data-stu-id="69f07-139">Required</span></span> | <span data-ttu-id="69f07-140">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="69f07-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="69f07-141">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="69f07-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="69f07-142">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="69f07-142">Element Information</span></span>



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f07-143">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="69f07-143">Element type</span></span> | <span data-ttu-id="69f07-144">[**Texttype**](texttype-complex-type.md) ComplexType (con l'elemento Content) o **xs: String** (con elementi [**nodo del gruppo**](groupnode-element.md) e [**TitleInfo**](titleinfo-element.md) )</span><span class="sxs-lookup"><span data-stu-id="69f07-144">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="69f07-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="69f07-145">Namespace</span></span>    | <span data-ttu-id="69f07-146">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="69f07-146">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="69f07-147">Nome schema</span><span class="sxs-lookup"><span data-stu-id="69f07-147">Schema name</span></span>  | <span data-ttu-id="69f07-148">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="69f07-148">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




