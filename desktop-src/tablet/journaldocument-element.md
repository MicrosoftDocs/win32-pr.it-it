---
description: Elemento di primo livello in un file XML di nota journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432173"
---
# <a name="journaldocument-element"></a><span data-ttu-id="f9783-103">Elemento JournalDocument</span><span class="sxs-lookup"><span data-stu-id="f9783-103">JournalDocument Element</span></span>

<span data-ttu-id="f9783-104">Elemento di primo livello in un file XML di nota journal.</span><span class="sxs-lookup"><span data-stu-id="f9783-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="f9783-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="f9783-105">Definition</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="f9783-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="f9783-106">Parent Elements</span></span>

<span data-ttu-id="f9783-107">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="f9783-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f9783-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f9783-108">Child Elements</span></span>

[<span data-ttu-id="f9783-109">**Cancelleria**</span><span class="sxs-lookup"><span data-stu-id="f9783-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="f9783-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="f9783-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="f9783-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="f9783-111">Attributes</span></span>



| <span data-ttu-id="f9783-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="f9783-112">Attribute</span></span>             | <span data-ttu-id="f9783-113">Type</span><span class="sxs-lookup"><span data-stu-id="f9783-113">Type</span></span>                      | <span data-ttu-id="f9783-114">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9783-114">Required</span></span> | <span data-ttu-id="f9783-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9783-115">Description</span></span>                                                      | <span data-ttu-id="f9783-116">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="f9783-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="f9783-117">**Versione**</span><span class="sxs-lookup"><span data-stu-id="f9783-117">**Version**</span></span>           | <span data-ttu-id="f9783-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="f9783-118">**xs:string**</span></span>             | <span data-ttu-id="f9783-119">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9783-119">Required</span></span> | <span data-ttu-id="f9783-120">Versione del documento Journal rappresentata nel file XML.</span><span class="sxs-lookup"><span data-stu-id="f9783-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="f9783-121">1.0</span><span class="sxs-lookup"><span data-stu-id="f9783-121">1.0</span></span>                       |
| <span data-ttu-id="f9783-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="f9783-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="f9783-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f9783-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f9783-124">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9783-124">Required</span></span> | <span data-ttu-id="f9783-125">Larghezza predefinita della pagina per il documento Journal.</span><span class="sxs-lookup"><span data-stu-id="f9783-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="f9783-126">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="f9783-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="f9783-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="f9783-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="f9783-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f9783-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f9783-129">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9783-129">Required</span></span> | <span data-ttu-id="f9783-130">Altezza predefinita della pagina per il documento Journal.</span><span class="sxs-lookup"><span data-stu-id="f9783-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="f9783-131">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="f9783-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="f9783-132">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f9783-132">Element Information</span></span>



|  <span data-ttu-id="f9783-133">Elemento</span><span class="sxs-lookup"><span data-stu-id="f9783-133">Element</span></span>     | <span data-ttu-id="f9783-134">valore</span><span class="sxs-lookup"><span data-stu-id="f9783-134">Value</span></span>                                                     |
|--------------|--------------------------------------------|
| <span data-ttu-id="f9783-135">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="f9783-135">Element type</span></span> | <span data-ttu-id="f9783-136">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="f9783-136">**JournalDocument**</span></span>                        |
| <span data-ttu-id="f9783-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9783-137">Namespace</span></span>    | <span data-ttu-id="f9783-138">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="f9783-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="f9783-139">Nome schema</span><span class="sxs-lookup"><span data-stu-id="f9783-139">Schema name</span></span>  | <span data-ttu-id="f9783-140">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="f9783-140">Journal Reader</span></span>                             |



 

 

 



