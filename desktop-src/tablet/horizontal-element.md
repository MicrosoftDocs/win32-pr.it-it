---
description: Contiene informazioni sulla formattazione per le linee orizzontali utilizzate per la cancelleria in una nota di Journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751895"
---
# <a name="horizontal-element"></a><span data-ttu-id="b7589-103">Elemento Horizontal</span><span class="sxs-lookup"><span data-stu-id="b7589-103">Horizontal Element</span></span>

<span data-ttu-id="b7589-104">Contiene informazioni sulla formattazione per le linee orizzontali utilizzate per la cancelleria in una nota di Journal.</span><span class="sxs-lookup"><span data-stu-id="b7589-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="b7589-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="b7589-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="b7589-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b7589-106">Parent Elements</span></span>

[<span data-ttu-id="b7589-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="b7589-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="b7589-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b7589-108">Child Elements</span></span>

<span data-ttu-id="b7589-109">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="b7589-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="b7589-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="b7589-110">Attributes</span></span>



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
<th><span data-ttu-id="b7589-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="b7589-111">Attribute</span></span></th>
<th><span data-ttu-id="b7589-112">Type</span><span class="sxs-lookup"><span data-stu-id="b7589-112">Type</span></span></th>
<th><span data-ttu-id="b7589-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b7589-113">Required</span></span></th>
<th><span data-ttu-id="b7589-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7589-114">Description</span></span></th>
<th><span data-ttu-id="b7589-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="b7589-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7589-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="b7589-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="b7589-117">SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7589-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="b7589-118">Necessario</span><span class="sxs-lookup"><span data-stu-id="b7589-118">Required</span></span></td>
<td><span data-ttu-id="b7589-119">Specifica il tipo di linea da disegnare.</span><span class="sxs-lookup"><span data-stu-id="b7589-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7589-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="b7589-120">None</span></span></li>
<li><span data-ttu-id="b7589-121">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="b7589-121">Solid</span></span></li>
<li><span data-ttu-id="b7589-122">Trattino</span><span class="sxs-lookup"><span data-stu-id="b7589-122">Dash</span></span></li>
<li><span data-ttu-id="b7589-123">Punto</span><span class="sxs-lookup"><span data-stu-id="b7589-123">Dot</span></span></li>
<li><span data-ttu-id="b7589-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="b7589-124">DashDot</span></span></li>
<li><span data-ttu-id="b7589-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="b7589-125">DashDotDot</span></span></li>
<li><span data-ttu-id="b7589-126">Double</span><span class="sxs-lookup"><span data-stu-id="b7589-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7589-127"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="b7589-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="b7589-128">SimpleType <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b7589-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="b7589-129">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b7589-129">Optional</span></span></td>
<td><span data-ttu-id="b7589-130">Colore dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b7589-130">Color of the element.</span></span></td>
<td><span data-ttu-id="b7589-131">Valore RGB esadecimale.</span><span class="sxs-lookup"><span data-stu-id="b7589-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="b7589-132">Corrisponde all'espressione regolare seguente: # [0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="b7589-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="b7589-133">Ad esempio, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="b7589-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7589-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="b7589-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="b7589-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="b7589-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="b7589-136">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b7589-136">Optional</span></span></td>
<td><span data-ttu-id="b7589-137">Spaziatura prima dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b7589-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="b7589-138">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="b7589-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7589-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="b7589-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="b7589-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="b7589-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="b7589-141">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b7589-141">Optional</span></span></td>
<td><span data-ttu-id="b7589-142">Spaziatura tra questo elemento e gli elementi circostanti.</span><span class="sxs-lookup"><span data-stu-id="b7589-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="b7589-143">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="b7589-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="b7589-144">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b7589-144">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="b7589-145">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b7589-145">Element type</span></span> | [<span data-ttu-id="b7589-146">**ComplexType HorizontalType**</span><span class="sxs-lookup"><span data-stu-id="b7589-146">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="b7589-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7589-147">Namespace</span></span>    | <span data-ttu-id="b7589-148">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="b7589-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="b7589-149">Nome schema</span><span class="sxs-lookup"><span data-stu-id="b7589-149">Schema name</span></span>  | <span data-ttu-id="b7589-150">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="b7589-150">Journal Reader</span></span>                                                    |



 

 

 




