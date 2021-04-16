---
description: Elemento di primo livello in un file XML di nota del journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530169"
---
# <a name="journaldocument-element"></a><span data-ttu-id="1b0e9-103">Elemento JournalDocument</span><span class="sxs-lookup"><span data-stu-id="1b0e9-103">JournalDocument Element</span></span>

<span data-ttu-id="1b0e9-104">Elemento di primo livello in un file XML di nota del journal.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="1b0e9-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="1b0e9-105">Definition</span></span>

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a><span data-ttu-id="1b0e9-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="1b0e9-106">Parent Elements</span></span>

<span data-ttu-id="1b0e9-107">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1b0e9-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1b0e9-108">Child Elements</span></span>

[<span data-ttu-id="1b0e9-109">**Cancelleria**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="1b0e9-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="1b0e9-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="1b0e9-111">Attributes</span></span>



| <span data-ttu-id="1b0e9-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b0e9-112">Attribute</span></span>             | <span data-ttu-id="1b0e9-113">Type</span><span class="sxs-lookup"><span data-stu-id="1b0e9-113">Type</span></span>                      | <span data-ttu-id="1b0e9-114">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="1b0e9-114">Required</span></span> | <span data-ttu-id="1b0e9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b0e9-115">Description</span></span>                                                      | <span data-ttu-id="1b0e9-116">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1b0e9-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="1b0e9-117">**Versione**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-117">**Version**</span></span>           | <span data-ttu-id="1b0e9-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-118">**xs:string**</span></span>             | <span data-ttu-id="1b0e9-119">Necessario</span><span class="sxs-lookup"><span data-stu-id="1b0e9-119">Required</span></span> | <span data-ttu-id="1b0e9-120">Versione del documento Journal rappresentata nel file XML.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="1b0e9-121">1.0</span><span class="sxs-lookup"><span data-stu-id="1b0e9-121">1.0</span></span>                       |
| <span data-ttu-id="1b0e9-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="1b0e9-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="1b0e9-124">Necessario</span><span class="sxs-lookup"><span data-stu-id="1b0e9-124">Required</span></span> | <span data-ttu-id="1b0e9-125">Larghezza predefinita della pagina per il documento Journal.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="1b0e9-126">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="1b0e9-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="1b0e9-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="1b0e9-129">Necessario</span><span class="sxs-lookup"><span data-stu-id="1b0e9-129">Required</span></span> | <span data-ttu-id="1b0e9-130">Altezza predefinita della pagina per il documento Journal.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="1b0e9-131">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="1b0e9-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="1b0e9-132">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1b0e9-132">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="1b0e9-133">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="1b0e9-133">Element type</span></span> | <span data-ttu-id="1b0e9-134">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="1b0e9-134">**JournalDocument**</span></span>                        |
| <span data-ttu-id="1b0e9-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1b0e9-135">Namespace</span></span>    | <span data-ttu-id="1b0e9-136">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="1b0e9-136">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="1b0e9-137">Nome schema</span><span class="sxs-lookup"><span data-stu-id="1b0e9-137">Schema name</span></span>  | <span data-ttu-id="1b0e9-138">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="1b0e9-138">Journal Reader</span></span>                             |



 

 

 



