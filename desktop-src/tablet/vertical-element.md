---
description: Contiene le informazioni che descrivono il componente verticale delle linee della cancelleria utilizzata dalla nota Journal. Utilizzato, ad esempio, quando la nota contiene linee della griglia.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento verticale
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191a9c5cb3190cff9b1e379a68dbfab49ddc25a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343271"
---
# <a name="vertical-element"></a><span data-ttu-id="46104-104">Elemento verticale</span><span class="sxs-lookup"><span data-stu-id="46104-104">Vertical Element</span></span>

<span data-ttu-id="46104-105">Contiene le informazioni che descrivono il componente verticale delle linee della cancelleria utilizzata dalla nota Journal.</span><span class="sxs-lookup"><span data-stu-id="46104-105">Contains the information that describes the vertical component of the lines in the stationery used by the Journal note.</span></span> <span data-ttu-id="46104-106">Utilizzato, ad esempio, quando la nota contiene linee della griglia.</span><span class="sxs-lookup"><span data-stu-id="46104-106">Used, for example, when the note has grid lines.</span></span>

## <a name="definition"></a><span data-ttu-id="46104-107">Definizione</span><span class="sxs-lookup"><span data-stu-id="46104-107">Definition</span></span>

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="46104-108">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="46104-108">Parent Elements</span></span>

[<span data-ttu-id="46104-109">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="46104-109">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="46104-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="46104-110">Child Elements</span></span>

<span data-ttu-id="46104-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="46104-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="46104-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="46104-112">Attributes</span></span>



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
<th><span data-ttu-id="46104-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="46104-113">Attribute</span></span></th>
<th><span data-ttu-id="46104-114">Type</span><span class="sxs-lookup"><span data-stu-id="46104-114">Type</span></span></th>
<th><span data-ttu-id="46104-115">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="46104-115">Required</span></span></th>
<th><span data-ttu-id="46104-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46104-116">Description</span></span></th>
<th><span data-ttu-id="46104-117">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="46104-117">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46104-118"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="46104-118"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="46104-119">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="46104-119"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="46104-120">Necessario</span><span class="sxs-lookup"><span data-stu-id="46104-120">Required</span></span></td>
<td><span data-ttu-id="46104-121">Specifica il tipo di linea da disegnare.</span><span class="sxs-lookup"><span data-stu-id="46104-121">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="46104-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="46104-122">None</span></span></li>
<li><span data-ttu-id="46104-123">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="46104-123">Solid</span></span></li>
<li><span data-ttu-id="46104-124">Trattino</span><span class="sxs-lookup"><span data-stu-id="46104-124">Dash</span></span></li>
<li><span data-ttu-id="46104-125">Punto</span><span class="sxs-lookup"><span data-stu-id="46104-125">Dot</span></span></li>
<li><span data-ttu-id="46104-126">DashDot</span><span class="sxs-lookup"><span data-stu-id="46104-126">DashDot</span></span></li>
<li><span data-ttu-id="46104-127">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="46104-127">DashDotDot</span></span></li>
<li><span data-ttu-id="46104-128">Double</span><span class="sxs-lookup"><span data-stu-id="46104-128">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46104-129"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="46104-129"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="46104-130">SimpleType <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="46104-130"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="46104-131">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46104-131">Optional</span></span></td>
<td><span data-ttu-id="46104-132">Colore dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="46104-132">Color of the element.</span></span></td>
<td><span data-ttu-id="46104-133">Valore RGB esadecimale.</span><span class="sxs-lookup"><span data-stu-id="46104-133">A hexadecimal RGB value.</span></span> <span data-ttu-id="46104-134">Corrisponde all'espressione regolare seguente: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="46104-134">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="46104-135">Ad esempio, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="46104-135">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46104-136"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="46104-136"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="46104-137"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="46104-137"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="46104-138">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46104-138">Optional</span></span></td>
<td><span data-ttu-id="46104-139">Spaziatura prima dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="46104-139">Spacing before the element.</span></span></td>
<td><span data-ttu-id="46104-140">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="46104-140">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46104-141"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="46104-141"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="46104-142"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="46104-142"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="46104-143">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46104-143">Optional</span></span></td>
<td><span data-ttu-id="46104-144">Spaziatura tra questo elemento e gli elementi circostanti.</span><span class="sxs-lookup"><span data-stu-id="46104-144">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="46104-145">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="46104-145">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="46104-146">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="46104-146">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="46104-147">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="46104-147">Element type</span></span> | <span data-ttu-id="46104-148">ComplexType [**VerticalType**](verticaltype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="46104-148">[**VerticalType**](verticaltype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="46104-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46104-149">Namespace</span></span>    | <span data-ttu-id="46104-150">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="46104-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="46104-151">Nome schema</span><span class="sxs-lookup"><span data-stu-id="46104-151">Schema name</span></span>  | <span data-ttu-id="46104-152">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="46104-152">Journal Reader</span></span>                                                |



 

 

 




