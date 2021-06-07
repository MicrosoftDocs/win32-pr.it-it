---
description: Contiene le informazioni che descrivono il componente verticale delle linee nella postazione utilizzata dalla nota Journal. Usato, ad esempio, quando la nota contiene linee griglia.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento Vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42565e6f2828c4ef27d1b28830502303a03e6f13
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432123"
---
# <a name="vertical-element"></a><span data-ttu-id="8bc70-104">Elemento Vertical</span><span class="sxs-lookup"><span data-stu-id="8bc70-104">Vertical Element</span></span>

<span data-ttu-id="8bc70-105">Contiene le informazioni che descrivono il componente verticale delle linee nella postazione utilizzata dalla nota Journal.</span><span class="sxs-lookup"><span data-stu-id="8bc70-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="8bc70-106">Usato, ad esempio, quando la nota contiene linee griglia.</span><span class="sxs-lookup"><span data-stu-id="8bc70-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="8bc70-107">Definizione</span><span class="sxs-lookup"><span data-stu-id="8bc70-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="8bc70-108">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8bc70-108">Parent Elements</span></span>

[<span data-ttu-id="8bc70-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="8bc70-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="8bc70-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8bc70-110">Child Elements</span></span>

<span data-ttu-id="8bc70-111">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="8bc70-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="8bc70-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="8bc70-112">Attributes</span></span>



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
<th><span data-ttu-id="8bc70-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="8bc70-113">Attribute</span></span></th>
<th><span data-ttu-id="8bc70-114">Type</span><span class="sxs-lookup"><span data-stu-id="8bc70-114">Type</span></span></th>
<th><span data-ttu-id="8bc70-115">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="8bc70-115">Required</span></span></th>
<th><span data-ttu-id="8bc70-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bc70-116">Description</span></span></th>
<th><span data-ttu-id="8bc70-117">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="8bc70-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8bc70-118"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="8bc70-119"><a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bc70-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="8bc70-120">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="8bc70-120">Required</span></span></td>
<td><span data-ttu-id="8bc70-121">Specifica il tipo di linea da disegnare.</span><span class="sxs-lookup"><span data-stu-id="8bc70-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="8bc70-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8bc70-122">None</span></span></li>
<li><span data-ttu-id="8bc70-123">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="8bc70-123">Solid</span></span></li>
<li><span data-ttu-id="8bc70-124">Trattino</span><span class="sxs-lookup"><span data-stu-id="8bc70-124">Dash</span></span></li>
<li><span data-ttu-id="8bc70-125">Punto</span><span class="sxs-lookup"><span data-stu-id="8bc70-125">Dot</span></span></li>
<li><span data-ttu-id="8bc70-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="8bc70-126">DashDot</span></span></li>
<li><span data-ttu-id="8bc70-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="8bc70-127">DashDotDot</span></span></li>
<li><span data-ttu-id="8bc70-128">Double</span><span class="sxs-lookup"><span data-stu-id="8bc70-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bc70-129"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="8bc70-130"><a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="8bc70-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="8bc70-131">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="8bc70-131">Optional</span></span></td>
<td><span data-ttu-id="8bc70-132">Colore dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8bc70-132">Color of the element.</span></span></td>
<td><span data-ttu-id="8bc70-133">Valore RGB esadecimale.</span><span class="sxs-lookup"><span data-stu-id="8bc70-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="8bc70-134">Corrisponde all'espressione regolare seguente: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="8bc70-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="8bc70-135">Ad esempio, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="8bc70-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8bc70-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="8bc70-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="8bc70-138">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="8bc70-138">Optional</span></span></td>
<td><span data-ttu-id="8bc70-139">Spaziatura prima dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8bc70-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="8bc70-140">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="8bc70-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8bc70-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="8bc70-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="8bc70-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="8bc70-143">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="8bc70-143">Optional</span></span></td>
<td><span data-ttu-id="8bc70-144">Spaziatura tra questo elemento e gli elementi circostante.</span><span class="sxs-lookup"><span data-stu-id="8bc70-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="8bc70-145">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="8bc70-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="8bc70-146">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8bc70-146">Element Information</span></span>



|  <span data-ttu-id="8bc70-147">Elemento</span><span class="sxs-lookup"><span data-stu-id="8bc70-147">Element</span></span>     | <span data-ttu-id="8bc70-148">valore</span><span class="sxs-lookup"><span data-stu-id="8bc70-148">Value</span></span>                                                         |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="8bc70-149">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="8bc70-149">Element type</span></span> | <span data-ttu-id="8bc70-150">[**complexType VerticalType**](verticaltype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="8bc70-150">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="8bc70-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8bc70-151">Namespace</span></span>    | <span data-ttu-id="8bc70-152">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="8bc70-152">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="8bc70-153">Nome schema</span><span class="sxs-lookup"><span data-stu-id="8bc70-153">Schema name</span></span>  | <span data-ttu-id="8bc70-154">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="8bc70-154">Journal Reader</span></span>                                                |



 

 

 




