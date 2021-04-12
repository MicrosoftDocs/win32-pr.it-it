---
description: Definisce le linee dei margini disegnate nella pagina.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0500d4db165012393cb600c1e118089b68c76695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233865"
---
# <a name="margin-element"></a><span data-ttu-id="a37dc-103">Elemento Margin</span><span class="sxs-lookup"><span data-stu-id="a37dc-103">Margin Element</span></span>

<span data-ttu-id="a37dc-104">Definisce le linee dei margini disegnate nella pagina.</span><span class="sxs-lookup"><span data-stu-id="a37dc-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="a37dc-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="a37dc-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="a37dc-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a37dc-106">Parent Elements</span></span>

<span data-ttu-id="a37dc-107">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="a37dc-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a37dc-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a37dc-108">Child Elements</span></span>

<span data-ttu-id="a37dc-109">Nessuno..</span><span class="sxs-lookup"><span data-stu-id="a37dc-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="a37dc-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="a37dc-110">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a37dc-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="a37dc-111">Attribute</span></span></th>
<th><span data-ttu-id="a37dc-112">Type</span><span class="sxs-lookup"><span data-stu-id="a37dc-112">Type</span></span></th>
<th><span data-ttu-id="a37dc-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="a37dc-113">Required</span></span></th>
<th><span data-ttu-id="a37dc-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a37dc-114">Description</span></span></th>
<th><span data-ttu-id="a37dc-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a37dc-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a37dc-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="a37dc-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="a37dc-117">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="a37dc-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="a37dc-118">Necessario</span><span class="sxs-lookup"><span data-stu-id="a37dc-118">Required</span></span></td>
<td><span data-ttu-id="a37dc-119">Specifica il tipo di linea da disegnare.</span><span class="sxs-lookup"><span data-stu-id="a37dc-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="a37dc-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="a37dc-120">None</span></span></li>
<li><span data-ttu-id="a37dc-121">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="a37dc-121">Solid</span></span></li>
<li><span data-ttu-id="a37dc-122">Trattino</span><span class="sxs-lookup"><span data-stu-id="a37dc-122">Dash</span></span></li>
<li><span data-ttu-id="a37dc-123">Punto</span><span class="sxs-lookup"><span data-stu-id="a37dc-123">Dot</span></span></li>
<li><span data-ttu-id="a37dc-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="a37dc-124">DashDot</span></span></li>
<li><span data-ttu-id="a37dc-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="a37dc-125">DashDotDot</span></span></li>
<li><span data-ttu-id="a37dc-126">Double</span><span class="sxs-lookup"><span data-stu-id="a37dc-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a37dc-127"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="a37dc-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="a37dc-128">SimpleType <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="a37dc-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="a37dc-129">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a37dc-129">Optional</span></span></td>
<td><span data-ttu-id="a37dc-130">Colore dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a37dc-130">Color of the element.</span></span></td>
<td><span data-ttu-id="a37dc-131">Valore RGB esadecimale.</span><span class="sxs-lookup"><span data-stu-id="a37dc-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="a37dc-132">Corrisponde all'espressione regolare seguente: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="a37dc-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="a37dc-133">Ad esempio, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="a37dc-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a37dc-134"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="a37dc-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="a37dc-135">SimpleType <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a></span><span class="sxs-lookup"><span data-stu-id="a37dc-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="a37dc-136">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a37dc-136">Optional</span></span></td>
<td><span data-ttu-id="a37dc-137">Indica il margine sinistro o destro.</span><span class="sxs-lookup"><span data-stu-id="a37dc-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="a37dc-138">Sinistra</span><span class="sxs-lookup"><span data-stu-id="a37dc-138">Left</span></span></li>
<li><span data-ttu-id="a37dc-139">Destra</span><span class="sxs-lookup"><span data-stu-id="a37dc-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a37dc-140"><strong>Spaziatura</strong></span><span class="sxs-lookup"><span data-stu-id="a37dc-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="a37dc-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="a37dc-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="a37dc-142">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a37dc-142">Optional</span></span></td>
<td><span data-ttu-id="a37dc-143">Spaziatura tra il bordo della pagina e il margine.</span><span class="sxs-lookup"><span data-stu-id="a37dc-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="a37dc-144">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="a37dc-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="a37dc-145">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="a37dc-145">Element Information</span></span>



|              |                                                           |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="a37dc-146">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="a37dc-146">Element type</span></span> | <span data-ttu-id="a37dc-147">ComplexType [**MarginType**](margintype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="a37dc-147">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="a37dc-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a37dc-148">Namespace</span></span>    | <span data-ttu-id="a37dc-149">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="a37dc-149">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="a37dc-150">Nome schema</span><span class="sxs-lookup"><span data-stu-id="a37dc-150">Schema name</span></span>  | <span data-ttu-id="a37dc-151">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="a37dc-151">Journal Reader</span></span>                                            |



 

 

 




