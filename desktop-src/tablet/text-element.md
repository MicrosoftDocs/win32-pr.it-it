---
description: Contiene informazioni di testo dalla nota journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432320"
---
# <a name="text-element"></a><span data-ttu-id="31518-103">Elemento Text</span><span class="sxs-lookup"><span data-stu-id="31518-103">Text Element</span></span>

<span data-ttu-id="31518-104">Contiene informazioni di testo dalla nota journal.</span><span class="sxs-lookup"><span data-stu-id="31518-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="31518-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="31518-105">Definition</span></span>

<span data-ttu-id="31518-106">Se usato con [**Content**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="31518-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="31518-107">Oppure, se usato con [**TitleInfo**](titleinfo-element.md) e [**GroupNode**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="31518-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="31518-108">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="31518-108">Parent Elements</span></span>

[<span data-ttu-id="31518-109">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="31518-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="31518-110">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="31518-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="31518-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="31518-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="31518-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="31518-112">Child Elements</span></span>

<span data-ttu-id="31518-113">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="31518-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="31518-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="31518-114">Attributes</span></span>

<span data-ttu-id="31518-115">Non sono presenti attributi quando vengono usati [**con TitleInfo**](titleinfo-element.md) e [**GroupNode.**](groupnode-element.md)</span><span class="sxs-lookup"><span data-stu-id="31518-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="31518-116">Se usati con [**Content,**](content-element--journal-reader.md)gli attributi sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="31518-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="31518-117">Attributo</span><span class="sxs-lookup"><span data-stu-id="31518-117">Attribute</span></span>  | <span data-ttu-id="31518-118">Type</span><span class="sxs-lookup"><span data-stu-id="31518-118">Type</span></span>                      | <span data-ttu-id="31518-119">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="31518-119">Required</span></span> | <span data-ttu-id="31518-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31518-120">Description</span></span>                                                                             | <span data-ttu-id="31518-121">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="31518-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="31518-122">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="31518-122">**Left**</span></span>   | <span data-ttu-id="31518-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="31518-123">**xs:integer**</span></span>            | <span data-ttu-id="31518-124">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="31518-124">Required</span></span> | <span data-ttu-id="31518-125">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="31518-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="31518-126">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="31518-126">Any integer.</span></span>              |
| <span data-ttu-id="31518-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="31518-127">**Top**</span></span>    | <span data-ttu-id="31518-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="31518-128">**xs:integer**</span></span>            | <span data-ttu-id="31518-129">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="31518-129">Required</span></span> | <span data-ttu-id="31518-130">Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="31518-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="31518-131">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="31518-131">Any integer.</span></span>              |
| <span data-ttu-id="31518-132">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="31518-132">**Width**</span></span>  | <span data-ttu-id="31518-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="31518-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="31518-134">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="31518-134">Required</span></span> | <span data-ttu-id="31518-135">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="31518-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="31518-136">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="31518-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="31518-137">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="31518-137">**Height**</span></span> | <span data-ttu-id="31518-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="31518-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="31518-139">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="31518-139">Required</span></span> | <span data-ttu-id="31518-140">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="31518-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="31518-141">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="31518-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="31518-142">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="31518-142">Element Information</span></span>



|   <span data-ttu-id="31518-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="31518-143">Element</span></span>           |   <span data-ttu-id="31518-144">valore</span><span class="sxs-lookup"><span data-stu-id="31518-144">Value</span></span>                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31518-145">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="31518-145">Element type</span></span> | <span data-ttu-id="31518-146">[**ComplexType**](texttype-complex-type.md) TextType (con l'elemento Content) o **xs:string** (con [**elementi GroupNode**](groupnode-element.md) [**e TitleInfo)**](titleinfo-element.md)</span><span class="sxs-lookup"><span data-stu-id="31518-146">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="31518-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31518-147">Namespace</span></span>    | <span data-ttu-id="31518-148">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="31518-148">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="31518-149">Nome schema</span><span class="sxs-lookup"><span data-stu-id="31518-149">Schema name</span></span>  | <span data-ttu-id="31518-150">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="31518-150">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




