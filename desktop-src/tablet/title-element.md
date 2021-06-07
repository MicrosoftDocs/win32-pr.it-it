---
description: Contiene informazioni sul titolo della nota journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432223"
---
# <a name="title-element"></a><span data-ttu-id="02bfc-103">Elemento Title</span><span class="sxs-lookup"><span data-stu-id="02bfc-103">Title Element</span></span>

<span data-ttu-id="02bfc-104">Contiene informazioni sul titolo della nota journal.</span><span class="sxs-lookup"><span data-stu-id="02bfc-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="02bfc-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="02bfc-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="02bfc-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="02bfc-106">Parent Elements</span></span>

[<span data-ttu-id="02bfc-107">**Cancelleria**</span><span class="sxs-lookup"><span data-stu-id="02bfc-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="02bfc-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="02bfc-108">Child Elements</span></span>

[<span data-ttu-id="02bfc-109">**TitleArea**</span><span class="sxs-lookup"><span data-stu-id="02bfc-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="02bfc-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="02bfc-110">Attributes</span></span>



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
<th><span data-ttu-id="02bfc-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="02bfc-111">Attribute</span></span></th>
<th><span data-ttu-id="02bfc-112">Type</span><span class="sxs-lookup"><span data-stu-id="02bfc-112">Type</span></span></th>
<th><span data-ttu-id="02bfc-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="02bfc-113">Required</span></span></th>
<th><span data-ttu-id="02bfc-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02bfc-114">Description</span></span></th>
<th><span data-ttu-id="02bfc-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="02bfc-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02bfc-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="02bfc-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="02bfc-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="02bfc-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="02bfc-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="02bfc-118">Required</span></span></td>
<td><span data-ttu-id="02bfc-119">Specifica il tipo di bordo che circonda il titolo della nota.</span><span class="sxs-lookup"><span data-stu-id="02bfc-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="02bfc-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="02bfc-120">None</span></span></li>
<li><span data-ttu-id="02bfc-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="02bfc-121">SolidSquare</span></span></li>
<li><span data-ttu-id="02bfc-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="02bfc-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="02bfc-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="02bfc-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="02bfc-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="02bfc-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="02bfc-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="02bfc-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02bfc-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="02bfc-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="02bfc-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="02bfc-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="02bfc-128">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="02bfc-128">Required</span></span></td>
<td><span data-ttu-id="02bfc-129">Definisce se il titolo include o meno una data.</span><span class="sxs-lookup"><span data-stu-id="02bfc-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="02bfc-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="02bfc-130">None</span></span></li>
<li><span data-ttu-id="02bfc-131">Short</span><span class="sxs-lookup"><span data-stu-id="02bfc-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02bfc-132"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="02bfc-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="02bfc-133"><a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="02bfc-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="02bfc-134">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="02bfc-134">Optional</span></span></td>
<td><span data-ttu-id="02bfc-135">Specifica il colore dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="02bfc-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="02bfc-136">Vedere <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="02bfc-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="02bfc-137">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="02bfc-137">Element Information</span></span>



| <span data-ttu-id="02bfc-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="02bfc-138">Element</span></span>      | <span data-ttu-id="02bfc-139">valore</span><span class="sxs-lookup"><span data-stu-id="02bfc-139">Value</span></span>                                                   |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="02bfc-140">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="02bfc-140">Element type</span></span> | <span data-ttu-id="02bfc-141">[**ComplexType TitleType**](titletype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="02bfc-141">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="02bfc-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02bfc-142">Namespace</span></span>    | <span data-ttu-id="02bfc-143">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="02bfc-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="02bfc-144">Nome schema</span><span class="sxs-lookup"><span data-stu-id="02bfc-144">Schema name</span></span>  | <span data-ttu-id="02bfc-145">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="02bfc-145">Journal Reader</span></span>                                          |



 

 

 



