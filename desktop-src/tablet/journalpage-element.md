---
description: Contiene i dettagli relativi a una singola pagina in una nota journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0939194585b067525fa841d6d41674180a40adb9
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432143"
---
# <a name="journalpage-element"></a><span data-ttu-id="21859-103">Elemento JournalPage</span><span class="sxs-lookup"><span data-stu-id="21859-103">JournalPage Element</span></span>

<span data-ttu-id="21859-104">Contiene i dettagli relativi a una singola pagina in una nota journal.</span><span class="sxs-lookup"><span data-stu-id="21859-104">Contains the details about an individual page in a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="21859-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="21859-105">Definition</span></span>

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="21859-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="21859-106">Parent Elements</span></span>

[<span data-ttu-id="21859-107">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="21859-107">**JournalDocument**</span></span>](journaldocument-element.md)

## <a name="child-elements"></a><span data-ttu-id="21859-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="21859-108">Child Elements</span></span>

[<span data-ttu-id="21859-109">**Stazionaria**</span><span class="sxs-lookup"><span data-stu-id="21859-109">**Stationary**</span></span>](stationery-element.md)

[<span data-ttu-id="21859-110">**DocImage**</span><span class="sxs-lookup"><span data-stu-id="21859-110">**DocImage**</span></span>](docimage-element.md)

[<span data-ttu-id="21859-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="21859-111">**TitleInfo**</span></span>](titleinfo-element.md)

[<span data-ttu-id="21859-112">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="21859-112">**Content**</span></span>](content-element--journal-reader.md)

## <a name="attributes"></a><span data-ttu-id="21859-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="21859-113">Attributes</span></span>



| <span data-ttu-id="21859-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="21859-114">Attribute</span></span>      | <span data-ttu-id="21859-115">Type</span><span class="sxs-lookup"><span data-stu-id="21859-115">Type</span></span>                      | <span data-ttu-id="21859-116">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21859-116">Required</span></span> | <span data-ttu-id="21859-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21859-117">Description</span></span>                                                                        | <span data-ttu-id="21859-118">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="21859-118">Possible Values</span></span>                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="21859-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="21859-119">**Number**</span></span>     | <span data-ttu-id="21859-120">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="21859-120">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="21859-121">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21859-121">Required</span></span> | <span data-ttu-id="21859-122">Numero ordinale della pagina all'interno del documento Journal, a partire da uno (1).</span><span class="sxs-lookup"><span data-stu-id="21859-122">The ordinal number of the page within the Journal document, starting with one (1).</span></span> | <span data-ttu-id="21859-123">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="21859-123">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="21859-124">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="21859-124">**Width**</span></span>      | <span data-ttu-id="21859-125">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="21859-125">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="21859-126">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21859-126">Required</span></span> | <span data-ttu-id="21859-127">Larghezza della pagina.</span><span class="sxs-lookup"><span data-stu-id="21859-127">The width of the page.</span></span>                                                             | <span data-ttu-id="21859-128">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="21859-128">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="21859-129">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="21859-129">**Height**</span></span>     | <span data-ttu-id="21859-130">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="21859-130">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="21859-131">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21859-131">Required</span></span> | <span data-ttu-id="21859-132">Altezza della pagina.</span><span class="sxs-lookup"><span data-stu-id="21859-132">The height of the page.</span></span>                                                            | <span data-ttu-id="21859-133">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="21859-133">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="21859-134">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="21859-134">**LineHeight**</span></span> | <span data-ttu-id="21859-135">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="21859-135">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="21859-136">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21859-136">Optional</span></span> | <span data-ttu-id="21859-137">Altezza della riga utilizzata nella pagina.</span><span class="sxs-lookup"><span data-stu-id="21859-137">The height of the line used on the page.</span></span>                                           | <span data-ttu-id="21859-138">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="21859-138">Any non-negative integer.</span></span>                                |
| <span data-ttu-id="21859-139">**Languageid**</span><span class="sxs-lookup"><span data-stu-id="21859-139">**LanguageId**</span></span> | <span data-ttu-id="21859-140">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="21859-140">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="21859-141">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21859-141">Optional</span></span> | <span data-ttu-id="21859-142">ID lingua usato per la pagina.</span><span class="sxs-lookup"><span data-stu-id="21859-142">The language id used for the page.</span></span>                                                 | <span data-ttu-id="21859-143">Intero non negativo che rappresenta un ID lingua valido.</span><span class="sxs-lookup"><span data-stu-id="21859-143">A non-negative integer representing a valid language id.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="21859-144">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="21859-144">Element Information</span></span>



|  <span data-ttu-id="21859-145">Elemento</span><span class="sxs-lookup"><span data-stu-id="21859-145">Element</span></span>     | <span data-ttu-id="21859-146">valore</span><span class="sxs-lookup"><span data-stu-id="21859-146">Value</span></span>                                                     |
|--------------|---------------------------------------------------------------------|
| <span data-ttu-id="21859-147">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="21859-147">Element type</span></span> | <span data-ttu-id="21859-148">[**ComplexType JournalPageType**](journalpagetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="21859-148">[**JournalPageType**](journalpagetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="21859-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21859-149">Namespace</span></span>    | <span data-ttu-id="21859-150">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="21859-150">urn:schemas-microsoft-com:tabletpc:richink</span></span>                          |
| <span data-ttu-id="21859-151">Nome schema</span><span class="sxs-lookup"><span data-stu-id="21859-151">Schema name</span></span>  | <span data-ttu-id="21859-152">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="21859-152">Journal Reader</span></span>                                                      |



 

 

 



