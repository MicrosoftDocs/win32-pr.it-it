---
description: Definisce le linee dei margini disegnate nella pagina.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547177a10fc3724f3b9bf3dde65f857d03f0f2a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432133"
---
# <a name="margin-element"></a><span data-ttu-id="3ca0e-103">Elemento Margin</span><span class="sxs-lookup"><span data-stu-id="3ca0e-103">Margin Element</span></span>

<span data-ttu-id="3ca0e-104">Definisce le linee dei margini disegnate nella pagina.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-104">Defines the margin lines drawn on the page.</span></span>

## <a name="definition"></a><span data-ttu-id="3ca0e-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="3ca0e-105">Definition</span></span>

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a><span data-ttu-id="3ca0e-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="3ca0e-106">Parent Elements</span></span>

<span data-ttu-id="3ca0e-107">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3ca0e-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3ca0e-108">Child Elements</span></span>

<span data-ttu-id="3ca0e-109">Nessuno..</span><span class="sxs-lookup"><span data-stu-id="3ca0e-109">None..</span></span>

## <a name="attributes"></a><span data-ttu-id="3ca0e-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="3ca0e-110">Attributes</span></span>



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
<th><span data-ttu-id="3ca0e-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="3ca0e-111">Attribute</span></span></th>
<th><span data-ttu-id="3ca0e-112">Type</span><span class="sxs-lookup"><span data-stu-id="3ca0e-112">Type</span></span></th>
<th><span data-ttu-id="3ca0e-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="3ca0e-113">Required</span></span></th>
<th><span data-ttu-id="3ca0e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ca0e-114">Description</span></span></th>
<th><span data-ttu-id="3ca0e-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3ca0e-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ca0e-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="3ca0e-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="3ca0e-117"><a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ca0e-117"><a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="3ca0e-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="3ca0e-118">Required</span></span></td>
<td><span data-ttu-id="3ca0e-119">Specifica il tipo di linea da disegnare.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-119">Specifies the type of line to be drawn.</span></span></td>
<td><ul>
<li><span data-ttu-id="3ca0e-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ca0e-120">None</span></span></li>
<li><span data-ttu-id="3ca0e-121">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="3ca0e-121">Solid</span></span></li>
<li><span data-ttu-id="3ca0e-122">Trattino</span><span class="sxs-lookup"><span data-stu-id="3ca0e-122">Dash</span></span></li>
<li><span data-ttu-id="3ca0e-123">Punto</span><span class="sxs-lookup"><span data-stu-id="3ca0e-123">Dot</span></span></li>
<li><span data-ttu-id="3ca0e-124">DashDot</span><span class="sxs-lookup"><span data-stu-id="3ca0e-124">DashDot</span></span></li>
<li><span data-ttu-id="3ca0e-125">DashDotDot</span><span class="sxs-lookup"><span data-stu-id="3ca0e-125">DashDotDot</span></span></li>
<li><span data-ttu-id="3ca0e-126">Double</span><span class="sxs-lookup"><span data-stu-id="3ca0e-126">Double</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca0e-127"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="3ca0e-127"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="3ca0e-128"><a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ca0e-128"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="3ca0e-129">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="3ca0e-129">Optional</span></span></td>
<td><span data-ttu-id="3ca0e-130">Colore dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-130">Color of the element.</span></span></td>
<td><span data-ttu-id="3ca0e-131">Valore RGB esadecimale.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-131">A hexadecimal RGB value.</span></span> <span data-ttu-id="3ca0e-132">Corrisponde all'espressione regolare seguente: #[0-9a-zA-Z] {6} .</span><span class="sxs-lookup"><span data-stu-id="3ca0e-132">Matches the following regular expression: #[0-9a-zA-Z]{6}.</span></span> <span data-ttu-id="3ca0e-133">Ad esempio, #4a79B5.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-133">For example, #4a79B5.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ca0e-134"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="3ca0e-134"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="3ca0e-135"><a href="margintypetype-simple-type.md"><strong>SimpleType MarginTypeType</strong></a></span><span class="sxs-lookup"><span data-stu-id="3ca0e-135"><a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="3ca0e-136">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="3ca0e-136">Optional</span></span></td>
<td><span data-ttu-id="3ca0e-137">Indica il margine sinistro o destro.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-137">Indicates Left or Right margin.</span></span></td>
<td><ul>
<li><span data-ttu-id="3ca0e-138">Sinistra</span><span class="sxs-lookup"><span data-stu-id="3ca0e-138">Left</span></span></li>
<li><span data-ttu-id="3ca0e-139">Destra</span><span class="sxs-lookup"><span data-stu-id="3ca0e-139">Right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ca0e-140"><strong>Spaziatura</strong></span><span class="sxs-lookup"><span data-stu-id="3ca0e-140"><strong>Spacing</strong></span></span></td>
<td><span data-ttu-id="3ca0e-141"><strong>xs:nonNegativeInteger</strong></span><span class="sxs-lookup"><span data-stu-id="3ca0e-141"><strong>xs:nonNegativeInteger</strong></span></span></td>
<td><span data-ttu-id="3ca0e-142">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="3ca0e-142">Optional</span></span></td>
<td><span data-ttu-id="3ca0e-143">Spaziatura tra il bordo della pagina e il margine.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-143">Spacing between edge of page and margin.</span></span></td>
<td><span data-ttu-id="3ca0e-144">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="3ca0e-144">Any non-negative integer.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="3ca0e-145">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="3ca0e-145">Element Information</span></span>



|  <span data-ttu-id="3ca0e-146">Elemento</span><span class="sxs-lookup"><span data-stu-id="3ca0e-146">Element</span></span>     | <span data-ttu-id="3ca0e-147">valore</span><span class="sxs-lookup"><span data-stu-id="3ca0e-147">Value</span></span>                                                     |
|--------------|-----------------------------------------------------------|
| <span data-ttu-id="3ca0e-148">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="3ca0e-148">Element type</span></span> | <span data-ttu-id="3ca0e-149">[**ComplexType MarginType**](margintype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="3ca0e-149">[**MarginType**](margintype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="3ca0e-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3ca0e-150">Namespace</span></span>    | <span data-ttu-id="3ca0e-151">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="3ca0e-151">urn:schemas-microsoft-com:tabletpc:richink</span></span>                |
| <span data-ttu-id="3ca0e-152">Nome schema</span><span class="sxs-lookup"><span data-stu-id="3ca0e-152">Schema name</span></span>  | <span data-ttu-id="3ca0e-153">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="3ca0e-153">Journal Reader</span></span>                                            |



 

 

 




