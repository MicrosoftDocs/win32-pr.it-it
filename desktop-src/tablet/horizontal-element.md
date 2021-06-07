---
description: Contiene informazioni di formattazione per le linee orizzontali utilizzate per gli elementi decorativi in una nota del journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432378"
---
# <a name="horizontal-element"></a><span data-ttu-id="3dc8c-103">Elemento Horizontal</span><span class="sxs-lookup"><span data-stu-id="3dc8c-103">Horizontal Element</span></span>

<span data-ttu-id="3dc8c-104">Contiene informazioni di formattazione per le linee orizzontali utilizzate per gli elementi decorativi in una nota del journal.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-104">Contains formatting information for the horizontal lines used for the stationery in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="3dc8c-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="3dc8c-105">Definition</span></span>

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="3dc8c-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3dc8c-106">Parent Elements</span></span>

[<span data-ttu-id="3dc8c-107">**LineLayout**</span><span class="sxs-lookup"><span data-stu-id="3dc8c-107">**LineLayout**</span></span>](linelayout-element.md)

## <a name="child-elements"></a><span data-ttu-id="3dc8c-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3dc8c-108">Child Elements</span></span>

<span data-ttu-id="3dc8c-109">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="3dc8c-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="3dc8c-110">Attributes</span></span>



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
<th><span data-ttu-id="3dc8c-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="3dc8c-111">Attribute</span></span></th>
<th><span data-ttu-id="3dc8c-112">Type</span><span class="sxs-lookup"><span data-stu-id="3dc8c-112">Type</span></span></th>
<th><span data-ttu-id="3dc8c-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="3dc8c-113">Required</span></span></th>
<th><span data-ttu-id="3dc8c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dc8c-114">Description</span></span></th>
<th><span data-ttu-id="3dc8c-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3dc8c-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3dc8c-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="3dc8c-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="3dc8c-117"><a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="3dc8c-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="3dc8c-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="3dc8c-118">Required</span></span></td>
<td><span data-ttu-id="3dc8c-119">Specifica il tipo di linea da disegnare.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="3dc8c-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3dc8c-120">None</span></span></li>
<li><span data-ttu-id="3dc8c-121">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="3dc8c-121">Solid</span></span></li>
<li><span data-ttu-id="3dc8c-122">Trattino</span><span class="sxs-lookup"><span data-stu-id="3dc8c-122">Dash</span></span></li>
<li><span data-ttu-id="3dc8c-123">Punto</span><span class="sxs-lookup"><span data-stu-id="3dc8c-123">Dot</span></span></li>
<li><span data-ttu-id="3dc8c-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="3dc8c-124">DashDot</span></span></li>
<li><span data-ttu-id="3dc8c-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="3dc8c-125">DashDotDot</span></span></li>
<li><span data-ttu-id="3dc8c-126">Double</span><span class="sxs-lookup"><span data-stu-id="3dc8c-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc8c-127"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="3dc8c-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="3dc8c-128"><a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="3dc8c-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="3dc8c-129">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="3dc8c-129">Optional</span></span></td>
<td><span data-ttu-id="3dc8c-130">Colore dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-130">Color of the element.</span></span></td>
<td><span data-ttu-id="3dc8c-131">Valore RGB esadecimale.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="3dc8c-132">Corrisponde all'espressione regolare seguente: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="3dc8c-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="3dc8c-133">Ad esempio, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dc8c-134"><strong>SpacingBefore</strong></span><span class="sxs-lookup"><span data-stu-id="3dc8c-134"><strong>SpacingBefore</strong></span></span></td>
<td><span data-ttu-id="3dc8c-135"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="3dc8c-135"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="3dc8c-136">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="3dc8c-136">Optional</span></span></td>
<td><span data-ttu-id="3dc8c-137">Spaziatura prima dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-137">Spacing before the element.</span></span></td>
<td><span data-ttu-id="3dc8c-138">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-138">Any non-negative integer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dc8c-139"><strong>SpacingBetween</strong></span><span class="sxs-lookup"><span data-stu-id="3dc8c-139"><strong>SpacingBetween</strong></span></span></td>
<td><span data-ttu-id="3dc8c-140"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="3dc8c-140"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="3dc8c-141">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="3dc8c-141">Optional</span></span></td>
<td><span data-ttu-id="3dc8c-142">Spaziatura tra questo elemento e gli elementi circostanti.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-142">Spacing between this element and surrounding elements.</span></span></td>
<td><span data-ttu-id="3dc8c-143">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="3dc8c-143">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="3dc8c-144">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3dc8c-144">Element Information</span></span>



|  <span data-ttu-id="3dc8c-145">Elemento</span><span class="sxs-lookup"><span data-stu-id="3dc8c-145">Element</span></span>     | <span data-ttu-id="3dc8c-146">valore</span><span class="sxs-lookup"><span data-stu-id="3dc8c-146">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="3dc8c-147">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="3dc8c-147">Element type</span></span> | [<span data-ttu-id="3dc8c-148">**ComplexType HorizontalType**</span><span class="sxs-lookup"><span data-stu-id="3dc8c-148">**HorizontalType complexType**</span></span>](horizontaltype-complex-type.md) |
| <span data-ttu-id="3dc8c-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3dc8c-149">Namespace</span></span>    | <span data-ttu-id="3dc8c-150">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="3dc8c-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="3dc8c-151">Nome schema</span><span class="sxs-lookup"><span data-stu-id="3dc8c-151">Schema name</span></span>  | <span data-ttu-id="3dc8c-152">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="3dc8c-152">Journal Reader</span></span>                                                    |



 

 

 




