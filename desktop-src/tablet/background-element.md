---
description: Contiene lo sfondo per un elemento JournalDocument o JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Elemento background
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315573"
---
# <a name="background-element"></a><span data-ttu-id="06e6d-103">Elemento background</span><span class="sxs-lookup"><span data-stu-id="06e6d-103">Background Element</span></span>

<span data-ttu-id="06e6d-104">Contiene lo sfondo per un elemento [**JournalDocument**](journaldocument-element.md) o [**JournalPage**](journalpage-element.md) .</span><span class="sxs-lookup"><span data-stu-id="06e6d-104">Contains the background for a [**JournalDocument**](journaldocument-element.md) element or [**JournalPage**](journalpage-element.md) element.</span></span>

## <a name="definition"></a><span data-ttu-id="06e6d-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="06e6d-105">Definition</span></span>

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="06e6d-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="06e6d-106">Parent Elements</span></span>

[<span data-ttu-id="06e6d-107">**Cancelleria**</span><span class="sxs-lookup"><span data-stu-id="06e6d-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="06e6d-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="06e6d-108">Child Elements</span></span>

[<span data-ttu-id="06e6d-109">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="06e6d-109">**Image**</span></span>](image-element.md)

## <a name="attributes"></a><span data-ttu-id="06e6d-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="06e6d-110">Attributes</span></span>



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
<th><span data-ttu-id="06e6d-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="06e6d-111">Attribute</span></span></th>
<th><span data-ttu-id="06e6d-112">Type</span><span class="sxs-lookup"><span data-stu-id="06e6d-112">Type</span></span></th>
<th><span data-ttu-id="06e6d-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="06e6d-113">Required</span></span></th>
<th><span data-ttu-id="06e6d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06e6d-114">Description</span></span></th>
<th><span data-ttu-id="06e6d-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="06e6d-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06e6d-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="06e6d-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="06e6d-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="06e6d-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="06e6d-118">Necessario</span><span class="sxs-lookup"><span data-stu-id="06e6d-118">Required</span></span></td>
<td><span data-ttu-id="06e6d-119">Specifica lo stile dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="06e6d-119">Specifies the style of the background.</span></span></td>
<td><ul>
<li><span data-ttu-id="06e6d-120">nessuno</span><span class="sxs-lookup"><span data-stu-id="06e6d-120">None</span></span></li>
<li><span data-ttu-id="06e6d-121">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="06e6d-121">Solid</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06e6d-122"><strong>Colore</strong></span><span class="sxs-lookup"><span data-stu-id="06e6d-122"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="06e6d-123">SimpleType <a href="colortype-simple-type.md"><strong>ColorType</strong></a></span><span class="sxs-lookup"><span data-stu-id="06e6d-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="06e6d-124">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="06e6d-124">Optional</span></span></td>
<td><span data-ttu-id="06e6d-125">Specifica il colore dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="06e6d-125">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="06e6d-126">Vedere <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span><span class="sxs-lookup"><span data-stu-id="06e6d-126">See <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="06e6d-127">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="06e6d-127">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="06e6d-128">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="06e6d-128">Element type</span></span> | <span data-ttu-id="06e6d-129">ComplexType [**BackgroundType**](backgroundtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="06e6d-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="06e6d-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06e6d-130">Namespace</span></span>    | <span data-ttu-id="06e6d-131">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="06e6d-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="06e6d-132">Nome schema</span><span class="sxs-lookup"><span data-stu-id="06e6d-132">Schema name</span></span>  | <span data-ttu-id="06e6d-133">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="06e6d-133">Journal Reader</span></span>                                                    |



 

 

 



