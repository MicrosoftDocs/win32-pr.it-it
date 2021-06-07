---
description: Contiene il contenuto di una pagina Journal.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content - elemento [Lettore journal]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432153"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="c4e1b-103">Lettore journal \[ dell'elemento Content\]</span><span class="sxs-lookup"><span data-stu-id="c4e1b-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="c4e1b-104">Contiene il contenuto di una pagina Journal.</span><span class="sxs-lookup"><span data-stu-id="c4e1b-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="c4e1b-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="c4e1b-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="c4e1b-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="c4e1b-106">Parent Elements</span></span>

[<span data-ttu-id="c4e1b-107">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="c4e1b-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="c4e1b-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c4e1b-108">Child Elements</span></span>

[<span data-ttu-id="c4e1b-109">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="c4e1b-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="c4e1b-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="c4e1b-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="c4e1b-111">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="c4e1b-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="c4e1b-112">**Text**</span><span class="sxs-lookup"><span data-stu-id="c4e1b-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="c4e1b-113">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="c4e1b-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="c4e1b-114">**Bandiera**</span><span class="sxs-lookup"><span data-stu-id="c4e1b-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="c4e1b-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="c4e1b-115">Attributes</span></span>



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
<th><span data-ttu-id="c4e1b-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="c4e1b-116">Attribute</span></span></th>
<th><span data-ttu-id="c4e1b-117">Type</span><span class="sxs-lookup"><span data-stu-id="c4e1b-117">Type</span></span></th>
<th><span data-ttu-id="c4e1b-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="c4e1b-118">Required</span></span></th>
<th><span data-ttu-id="c4e1b-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4e1b-119">Description</span></span></th>
<th><span data-ttu-id="c4e1b-120">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c4e1b-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4e1b-121"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="c4e1b-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="c4e1b-122"><a href="contenttype-complex-type.md"><strong>complexType ContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="c4e1b-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="c4e1b-123">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="c4e1b-123">Required</span></span></td>
<td><span data-ttu-id="c4e1b-124">Se il tipo è &quot; &quot; Inert, il contenuto non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="c4e1b-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="c4e1b-125">Normale</span><span class="sxs-lookup"><span data-stu-id="c4e1b-125">Normal</span></span></li>
<li><span data-ttu-id="c4e1b-126">Inerte</span><span class="sxs-lookup"><span data-stu-id="c4e1b-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="c4e1b-127">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c4e1b-127">Element Information</span></span>



|  <span data-ttu-id="c4e1b-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="c4e1b-128">Element</span></span>     | <span data-ttu-id="c4e1b-129">valore</span><span class="sxs-lookup"><span data-stu-id="c4e1b-129">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="c4e1b-130">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="c4e1b-130">Element type</span></span> | <span data-ttu-id="c4e1b-131">[**complexType ContentType**](contenttype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="c4e1b-131">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="c4e1b-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c4e1b-132">Namespace</span></span>    | <span data-ttu-id="c4e1b-133">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="c4e1b-133">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="c4e1b-134">Nome schema</span><span class="sxs-lookup"><span data-stu-id="c4e1b-134">Schema name</span></span>  | <span data-ttu-id="c4e1b-135">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="c4e1b-135">Journal Reader</span></span>                                              |



 

 

 




