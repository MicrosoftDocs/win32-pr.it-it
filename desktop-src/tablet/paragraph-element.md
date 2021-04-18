---
description: Contiene un paragrafo.
ms.assetid: 60322907-3902-49a9-91a9-e00b0a714c00
title: Elemento Paragraph (Windows.ui.xaml.documents. h)
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
ms.openlocfilehash: bfe3752541bb54571e9802f557e83dcc7632f845
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324356"
---
# <a name="paragraph-element"></a><span data-ttu-id="801b2-103">Paragraph-elemento</span><span class="sxs-lookup"><span data-stu-id="801b2-103">Paragraph Element</span></span>

<span data-ttu-id="801b2-104">Contiene un paragrafo.</span><span class="sxs-lookup"><span data-stu-id="801b2-104">Contains a paragraph.</span></span>

## <a name="definition"></a><span data-ttu-id="801b2-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="801b2-105">Definition</span></span>

``` syntax
<xs:element name="Paragraph" type="ParagraphType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="801b2-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="801b2-106">Parent Elements</span></span>

[<span data-ttu-id="801b2-107">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="801b2-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="801b2-108">**Nodo del gruppo**</span><span class="sxs-lookup"><span data-stu-id="801b2-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="801b2-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="801b2-109">Child Elements</span></span>

[<span data-ttu-id="801b2-110">**Linea**</span><span class="sxs-lookup"><span data-stu-id="801b2-110">**Line**</span></span>](line-element.md)

[<span data-ttu-id="801b2-111">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="801b2-111">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="attributes"></a><span data-ttu-id="801b2-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="801b2-112">Attributes</span></span>



| <span data-ttu-id="801b2-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="801b2-113">Attribute</span></span>       | <span data-ttu-id="801b2-114">Type</span><span class="sxs-lookup"><span data-stu-id="801b2-114">Type</span></span>                      | <span data-ttu-id="801b2-115">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="801b2-115">Required</span></span> | <span data-ttu-id="801b2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="801b2-116">Description</span></span>                                                                             | <span data-ttu-id="801b2-117">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="801b2-117">Possible Values</span></span>           |
|-----------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="801b2-118">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="801b2-118">**Left**</span></span>        | <span data-ttu-id="801b2-119">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="801b2-119">**xs:integer**</span></span>            | <span data-ttu-id="801b2-120">Necessario</span><span class="sxs-lookup"><span data-stu-id="801b2-120">Required</span></span> | <span data-ttu-id="801b2-121">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="801b2-121">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="801b2-122">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="801b2-122">Any integer.</span></span>              |
| <span data-ttu-id="801b2-123">**Top**</span><span class="sxs-lookup"><span data-stu-id="801b2-123">**Top**</span></span>         | <span data-ttu-id="801b2-124">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="801b2-124">**xs:integer**</span></span>            | <span data-ttu-id="801b2-125">Necessario</span><span class="sxs-lookup"><span data-stu-id="801b2-125">Required</span></span> | <span data-ttu-id="801b2-126">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="801b2-126">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="801b2-127">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="801b2-127">Any integer.</span></span>              |
| <span data-ttu-id="801b2-128">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="801b2-128">**Width**</span></span>       | <span data-ttu-id="801b2-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="801b2-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="801b2-130">Necessario</span><span class="sxs-lookup"><span data-stu-id="801b2-130">Required</span></span> | <span data-ttu-id="801b2-131">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="801b2-131">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="801b2-132">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="801b2-132">Any non-negative integer.</span></span> |
| <span data-ttu-id="801b2-133">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="801b2-133">**Height**</span></span>      | <span data-ttu-id="801b2-134">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="801b2-134">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="801b2-135">Necessario</span><span class="sxs-lookup"><span data-stu-id="801b2-135">Required</span></span> | <span data-ttu-id="801b2-136">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="801b2-136">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="801b2-137">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="801b2-137">Any non-negative integer.</span></span> |
| <span data-ttu-id="801b2-138">**BlockNumber**</span><span class="sxs-lookup"><span data-stu-id="801b2-138">**BlockNumber**</span></span> | <span data-ttu-id="801b2-139">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="801b2-139">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="801b2-140">Necessario</span><span class="sxs-lookup"><span data-stu-id="801b2-140">Required</span></span> | <span data-ttu-id="801b2-141">Numero del blocco.</span><span class="sxs-lookup"><span data-stu-id="801b2-141">Block number.</span></span>                                                                           | <span data-ttu-id="801b2-142">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="801b2-142">Any non-negative integer.</span></span> |
| <span data-ttu-id="801b2-143">**LineNumber**</span><span class="sxs-lookup"><span data-stu-id="801b2-143">**LineNumber**</span></span>  | <span data-ttu-id="801b2-144">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="801b2-144">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="801b2-145">Necessario</span><span class="sxs-lookup"><span data-stu-id="801b2-145">Required</span></span> | <span data-ttu-id="801b2-146">Riga in cui inizia il paragrafo.</span><span class="sxs-lookup"><span data-stu-id="801b2-146">The line on which the paragraph begins.</span></span>                                                 | <span data-ttu-id="801b2-147">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="801b2-147">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="801b2-148">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="801b2-148">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="801b2-149">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="801b2-149">Element type</span></span> | <span data-ttu-id="801b2-150">ComplexType [**ParagraphType**](paragraphtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="801b2-150">[**ParagraphType**](paragraphtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="801b2-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="801b2-151">Namespace</span></span>    | <span data-ttu-id="801b2-152">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="801b2-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="801b2-153">Nome schema</span><span class="sxs-lookup"><span data-stu-id="801b2-153">Schema name</span></span>  | <span data-ttu-id="801b2-154">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="801b2-154">Journal Reader</span></span>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="801b2-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="801b2-155">Requirements</span></span>



| <span data-ttu-id="801b2-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="801b2-156">Requirement</span></span> | <span data-ttu-id="801b2-157">Valore</span><span class="sxs-lookup"><span data-stu-id="801b2-157">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="801b2-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="801b2-158">Header</span></span><br/> | <dl> <span data-ttu-id="801b2-159"><dt>Windows.ui.xaml.documents. h</dt></span><span class="sxs-lookup"><span data-stu-id="801b2-159"><dt>Windows.ui.xaml.documents.h</dt></span></span> </dl> |



 

 




