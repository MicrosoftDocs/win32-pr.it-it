---
description: Contiene i dettagli relativi a una singola pagina in una nota del journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883418"
---
# <a name="journalpage-element"></a><span data-ttu-id="ed795-103">Elemento JournalPage</span><span class="sxs-lookup"><span data-stu-id="ed795-103">JournalPage Element</span></span>

<span data-ttu-id="ed795-104">Contiene i dettagli relativi a una singola pagina in una nota del journal.</span><span class="sxs-lookup"><span data-stu-id="ed795-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="ed795-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="ed795-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="ed795-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="ed795-106">Parent Elements</span></span>

[<span data-ttu-id="ed795-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="ed795-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="ed795-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="ed795-108">Child Elements</span></span>

[<span data-ttu-id="ed795-109">**Stazionaria**</span><span class="sxs-lookup"><span data-stu-id="ed795-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="ed795-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="ed795-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="ed795-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="ed795-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="ed795-112">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="ed795-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="ed795-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="ed795-113">Attributes</span></span>



| <span data-ttu-id="ed795-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="ed795-114">Attribute</span></span>      | <span data-ttu-id="ed795-115">Type</span><span class="sxs-lookup"><span data-stu-id="ed795-115">Type</span></span>                      | <span data-ttu-id="ed795-116">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="ed795-116">Required</span></span> | <span data-ttu-id="ed795-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed795-117">Description</span></span>                                                                        | <span data-ttu-id="ed795-118">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ed795-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="ed795-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="ed795-119">**Number**</span></span>     | <span data-ttu-id="ed795-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ed795-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ed795-121">Necessario</span><span class="sxs-lookup"><span data-stu-id="ed795-121">Required</span></span> | <span data-ttu-id="ed795-122">Numero ordinale della pagina all'interno del documento Journal, a partire da uno (1).</span><span class="sxs-lookup"><span data-stu-id="ed795-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="ed795-123">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="ed795-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="ed795-124">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="ed795-124">**Width**</span></span>      | <span data-ttu-id="ed795-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ed795-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ed795-126">Necessario</span><span class="sxs-lookup"><span data-stu-id="ed795-126">Required</span></span> | <span data-ttu-id="ed795-127">Larghezza della pagina.</span><span class="sxs-lookup"><span data-stu-id="ed795-127">The width of the page.</span></span>                                                             | <span data-ttu-id="ed795-128">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="ed795-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="ed795-129">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="ed795-129">**Height**</span></span>     | <span data-ttu-id="ed795-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ed795-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ed795-131">Necessario</span><span class="sxs-lookup"><span data-stu-id="ed795-131">Required</span></span> | <span data-ttu-id="ed795-132">Altezza della pagina.</span><span class="sxs-lookup"><span data-stu-id="ed795-132">The height of the page.</span></span>                                                            | <span data-ttu-id="ed795-133">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="ed795-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="ed795-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="ed795-134">**LineHeight**</span></span> | <span data-ttu-id="ed795-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ed795-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ed795-136">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="ed795-136">Optional</span></span> | <span data-ttu-id="ed795-137">Altezza della riga utilizzata nella pagina.</span><span class="sxs-lookup"><span data-stu-id="ed795-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="ed795-138">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="ed795-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="ed795-139">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="ed795-139">**LanguageId**</span></span> | <span data-ttu-id="ed795-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="ed795-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="ed795-141">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="ed795-141">Optional</span></span> | <span data-ttu-id="ed795-142">ID lingua utilizzato per la pagina.</span><span class="sxs-lookup"><span data-stu-id="ed795-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="ed795-143">Intero non negativo che rappresenta un ID lingua valido.</span><span class="sxs-lookup"><span data-stu-id="ed795-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="ed795-144">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="ed795-144">Element Information</span></span>



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed795-145">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="ed795-145">Element type</span></span> | <span data-ttu-id="ed795-146">ComplexType [**JournalPageType**](journalpagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="ed795-146">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ed795-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed795-147">Namespace</span></span>    | <span data-ttu-id="ed795-148">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="ed795-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="ed795-149">Nome schema</span><span class="sxs-lookup"><span data-stu-id="ed795-149">Schema name</span></span>  | <span data-ttu-id="ed795-150">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="ed795-150">Journal Reader</span></span>                                                      |



 

 

 



