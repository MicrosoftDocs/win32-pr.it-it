---
description: Contiene un paragrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Paragraph
api_type:
- HeaderDef
api_location:
- windows.ui.xaml.documents.h
ms.openlocfilehash: 2f246294c80814ec809c0a1ca035fcb4741c30c5
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432233"
---
# <a name="paragraph-element"></a><span data-ttu-id="abb78-103">Elemento Paragraph</span><span class="sxs-lookup"><span data-stu-id="abb78-103">Paragraph Element</span></span>

<span data-ttu-id="abb78-104">Contiene un paragrafo.</span><span class="sxs-lookup"><span data-stu-id="abb78-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="abb78-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="abb78-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="abb78-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="abb78-106">Parent Elements</span></span>

[<span data-ttu-id="abb78-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="abb78-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="abb78-108">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="abb78-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="abb78-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="abb78-109">Child Elements</span></span>

[<span data-ttu-id="abb78-110">**A linee**</span><span class="sxs-lookup"><span data-stu-id="abb78-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="abb78-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="abb78-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="abb78-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="abb78-112">Attributes</span></span>



| <span data-ttu-id="abb78-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="abb78-113">Attribute</span></span>       | <span data-ttu-id="abb78-114">Type</span><span class="sxs-lookup"><span data-stu-id="abb78-114">Type</span></span>                      | <span data-ttu-id="abb78-115">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="abb78-115">Required</span></span> | <span data-ttu-id="abb78-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abb78-116">Description</span></span>                                                                             | <span data-ttu-id="abb78-117">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="abb78-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="abb78-118">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="abb78-118">**Left**</span></span>        | <span data-ttu-id="abb78-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="abb78-119">**xs:integer**</span></span>            | <span data-ttu-id="abb78-120">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="abb78-120">Required</span></span> | <span data-ttu-id="abb78-121">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="abb78-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="abb78-122">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="abb78-122">Any integer.</span></span>              |
| <span data-ttu-id="abb78-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="abb78-123">**Top**</span></span>         | <span data-ttu-id="abb78-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="abb78-124">**xs:integer**</span></span>            | <span data-ttu-id="abb78-125">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="abb78-125">Required</span></span> | <span data-ttu-id="abb78-126">Distanza tra l'origine e il punto in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="abb78-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="abb78-127">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="abb78-127">Any integer.</span></span>              |
| <span data-ttu-id="abb78-128">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="abb78-128">**Width**</span></span>       | <span data-ttu-id="abb78-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="abb78-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="abb78-130">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="abb78-130">Required</span></span> | <span data-ttu-id="abb78-131">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="abb78-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="abb78-132">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="abb78-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="abb78-133">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="abb78-133">**Height**</span></span>      | <span data-ttu-id="abb78-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="abb78-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="abb78-135">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="abb78-135">Required</span></span> | <span data-ttu-id="abb78-136">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="abb78-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="abb78-137">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="abb78-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="abb78-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="abb78-138">**BlockNumber**</span></span> | <span data-ttu-id="abb78-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="abb78-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="abb78-140">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="abb78-140">Required</span></span> | <span data-ttu-id="abb78-141">Numero di blocco.</span><span class="sxs-lookup"><span data-stu-id="abb78-141">Block number.</span></span>                                                                           | <span data-ttu-id="abb78-142">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="abb78-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="abb78-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="abb78-143">**LineNumber**</span></span>  | <span data-ttu-id="abb78-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="abb78-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="abb78-145">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="abb78-145">Required</span></span> | <span data-ttu-id="abb78-146">Riga in cui inizia il paragrafo.</span><span class="sxs-lookup"><span data-stu-id="abb78-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="abb78-147">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="abb78-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="abb78-148">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="abb78-148">Element Information</span></span>



|  <span data-ttu-id="abb78-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="abb78-149">Element</span></span>     | <span data-ttu-id="abb78-150">valore</span><span class="sxs-lookup"><span data-stu-id="abb78-150">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="abb78-151">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="abb78-151">Element type</span></span> | <span data-ttu-id="abb78-152">[**complexType ParagraphType**](paragraphtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="abb78-152">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="abb78-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="abb78-153">Namespace</span></span>    | <span data-ttu-id="abb78-154">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="abb78-154">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="abb78-155">Nome schema</span><span class="sxs-lookup"><span data-stu-id="abb78-155">Schema name</span></span>  | <span data-ttu-id="abb78-156">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="abb78-156">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="abb78-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abb78-157">Requirements</span></span>



| <span data-ttu-id="abb78-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="abb78-158">Requirement</span></span> | <span data-ttu-id="abb78-159">Valore</span><span class="sxs-lookup"><span data-stu-id="abb78-159">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb78-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abb78-160">Header</span></span><br/> | <dl> <span data-ttu-id="abb78-161"><dt>Windows.ui.xaml.documents.h</dt></span><span class="sxs-lookup"><span data-stu-id="abb78-161"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




