---
description: Contiene informazioni sul titolo relative alla nota Journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318685"
---
# <a name="title-element"></a><span data-ttu-id="b8734-103">Elemento Title</span><span class="sxs-lookup"><span data-stu-id="b8734-103">Title Element</span></span>

<span data-ttu-id="b8734-104">Contiene informazioni sul titolo relative alla nota Journal.</span><span class="sxs-lookup"><span data-stu-id="b8734-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="b8734-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="b8734-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="b8734-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b8734-106">Parent Elements</span></span>

[<span data-ttu-id="b8734-107">**Cancelleria**</span><span class="sxs-lookup"><span data-stu-id="b8734-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="b8734-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b8734-108">Child Elements</span></span>

[<span data-ttu-id="b8734-109">**Elemento titlearea**</span><span class="sxs-lookup"><span data-stu-id="b8734-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="b8734-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="b8734-110">Attributes</span></span>



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
<th><span data-ttu-id="b8734-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="b8734-111">Attribute</span></span></th>
<th><span data-ttu-id="b8734-112">Type</span><span class="sxs-lookup"><span data-stu-id="b8734-112">Type</span></span></th>
<th><span data-ttu-id="b8734-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b8734-113">Required</span></span></th>
<th><span data-ttu-id="b8734-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8734-114">Description</span></span></th>
<th><span data-ttu-id="b8734-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="b8734-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8734-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="b8734-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="b8734-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="b8734-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="b8734-118">Necessario</span><span class="sxs-lookup"><span data-stu-id="b8734-118">Required</span></span></td>
<td><span data-ttu-id="b8734-119">Specifica il tipo di bordo che circonda il titolo della nota.</span><span class="sxs-lookup"><span data-stu-id="b8734-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="b8734-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="b8734-120">None</span></span></li>
<li><span data-ttu-id="b8734-121">SolidSquare</span><span class="sxs-lookup"><span data-stu-id="b8734-121">SolidSquare</span></span></li>
<li><span data-ttu-id="b8734-122">OutlineSquare</span><span class="sxs-lookup"><span data-stu-id="b8734-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="b8734-123">SolidRoundRect</span><span class="sxs-lookup"><span data-stu-id="b8734-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="b8734-124">OutlineRoundRect</span><span class="sxs-lookup"><span data-stu-id="b8734-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="b8734-125">SolidRoundRectDottedBaseline</span><span class="sxs-lookup"><span data-stu-id="b8734-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8734-126"><strong>DateStyle</strong></span><span class="sxs-lookup"><span data-stu-id="b8734-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="b8734-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="b8734-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="b8734-128">Necessario</span><span class="sxs-lookup"><span data-stu-id="b8734-128">Required</span></span></td>
<td><span data-ttu-id="b8734-129">Definisce se il titolo include o meno una data.</span><span class="sxs-lookup"><span data-stu-id="b8734-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="b8734-130">nessuno</span><span class="sxs-lookup"><span data-stu-id="b8734-130">None</span></span></li>
<li><span data-ttu-id="b8734-131">Short</span><span class="sxs-lookup"><span data-stu-id="b8734-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8734-132"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="b8734-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="b8734-133"><a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b8734-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="b8734-134">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b8734-134">Optional</span></span></td>
<td><span data-ttu-id="b8734-135">Specifica il colore dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="b8734-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="b8734-136">Vedere <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b8734-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="b8734-137">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b8734-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="b8734-138">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b8734-138">Element type</span></span> | <span data-ttu-id="b8734-139">ComplexType [**TitleType**](titletype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="b8734-139">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b8734-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8734-140">Namespace</span></span>    | <span data-ttu-id="b8734-141">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="b8734-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="b8734-142">Nome schema</span><span class="sxs-lookup"><span data-stu-id="b8734-142">Schema name</span></span>  | <span data-ttu-id="b8734-143">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="b8734-143">Journal Reader</span></span>                                          |



 

 

 



