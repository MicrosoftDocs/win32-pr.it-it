---
description: Contiene il contenuto di una pagina journal.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content (elemento) [Reader Journal]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314930"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="b5f38-103">\[Lettore Journal elemento contenuto\]</span><span class="sxs-lookup"><span data-stu-id="b5f38-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="b5f38-104">Contiene il contenuto di una pagina journal.</span><span class="sxs-lookup"><span data-stu-id="b5f38-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="b5f38-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="b5f38-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="b5f38-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b5f38-106">Parent Elements</span></span>

[<span data-ttu-id="b5f38-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="b5f38-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="b5f38-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b5f38-108">Child Elements</span></span>

[<span data-ttu-id="b5f38-109">**Nodo del gruppo**</span><span class="sxs-lookup"><span data-stu-id="b5f38-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="b5f38-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="b5f38-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="b5f38-111">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="b5f38-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="b5f38-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="b5f38-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="b5f38-113">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="b5f38-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="b5f38-114">**Contrassegno**</span><span class="sxs-lookup"><span data-stu-id="b5f38-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="b5f38-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="b5f38-115">Attributes</span></span>



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
<th><span data-ttu-id="b5f38-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="b5f38-116">Attribute</span></span></th>
<th><span data-ttu-id="b5f38-117">Type</span><span class="sxs-lookup"><span data-stu-id="b5f38-117">Type</span></span></th>
<th><span data-ttu-id="b5f38-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b5f38-118">Required</span></span></th>
<th><span data-ttu-id="b5f38-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5f38-119">Description</span></span></th>
<th><span data-ttu-id="b5f38-120">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="b5f38-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5f38-121"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="b5f38-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="b5f38-122"><a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b5f38-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="b5f38-123">Necessario</span><span class="sxs-lookup"><span data-stu-id="b5f38-123">Required</span></span></td>
<td><span data-ttu-id="b5f38-124">Se il tipo è &quot; inerte &quot; , il contenuto non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="b5f38-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="b5f38-125">Normale</span><span class="sxs-lookup"><span data-stu-id="b5f38-125">Normal</span></span></li>
<li><span data-ttu-id="b5f38-126">Inerte</span><span class="sxs-lookup"><span data-stu-id="b5f38-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="b5f38-127">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b5f38-127">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="b5f38-128">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b5f38-128">Element type</span></span> | <span data-ttu-id="b5f38-129">ComplexType [**ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="b5f38-129">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b5f38-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b5f38-130">Namespace</span></span>    | <span data-ttu-id="b5f38-131">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="b5f38-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="b5f38-132">Nome schema</span><span class="sxs-lookup"><span data-stu-id="b5f38-132">Schema name</span></span>  | <span data-ttu-id="b5f38-133">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="b5f38-133">Journal Reader</span></span>                                              |



 

 

 




