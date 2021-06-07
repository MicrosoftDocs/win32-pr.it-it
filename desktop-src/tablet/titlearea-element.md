---
description: Contiene informazioni sulla posizione e sul delimitatore per la nota Titolo, se presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432193"
---
# <a name="titlearea-element"></a><span data-ttu-id="b79e0-103">Elemento TitleArea</span><span class="sxs-lookup"><span data-stu-id="b79e0-103">TitleArea Element</span></span>

<span data-ttu-id="b79e0-104">Contiene informazioni sulla posizione e sul delimitatore per la nota Titolo, se presente.</span><span class="sxs-lookup"><span data-stu-id="b79e0-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="b79e0-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="b79e0-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="b79e0-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="b79e0-106">Parent Elements</span></span>

[<span data-ttu-id="b79e0-107">**Titolo**</span><span class="sxs-lookup"><span data-stu-id="b79e0-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="b79e0-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b79e0-108">Child Elements</span></span>

<span data-ttu-id="b79e0-109">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="b79e0-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="b79e0-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="b79e0-110">Attributes</span></span>



| <span data-ttu-id="b79e0-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="b79e0-111">Attribute</span></span>  | <span data-ttu-id="b79e0-112">Type</span><span class="sxs-lookup"><span data-stu-id="b79e0-112">Type</span></span>                      | <span data-ttu-id="b79e0-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b79e0-113">Required</span></span> | <span data-ttu-id="b79e0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b79e0-114">Description</span></span>                                                                             | <span data-ttu-id="b79e0-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="b79e0-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="b79e0-116">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="b79e0-116">**Left**</span></span>   | <span data-ttu-id="b79e0-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b79e0-117">**xs:integer**</span></span>            | <span data-ttu-id="b79e0-118">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b79e0-118">Required</span></span> | <span data-ttu-id="b79e0-119">Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b79e0-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="b79e0-120">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="b79e0-120">Any integer.</span></span>              |
| <span data-ttu-id="b79e0-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="b79e0-121">**Top**</span></span>    | <span data-ttu-id="b79e0-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="b79e0-122">**xs:integer**</span></span>            | <span data-ttu-id="b79e0-123">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b79e0-123">Required</span></span> | <span data-ttu-id="b79e0-124">Distanza tra l'origine e il punto in alto nel rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b79e0-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="b79e0-125">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="b79e0-125">Any integer.</span></span>              |
| <span data-ttu-id="b79e0-126">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="b79e0-126">**Width**</span></span>  | <span data-ttu-id="b79e0-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b79e0-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b79e0-128">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b79e0-128">Required</span></span> | <span data-ttu-id="b79e0-129">Larghezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b79e0-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="b79e0-130">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="b79e0-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="b79e0-131">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="b79e0-131">**Height**</span></span> | <span data-ttu-id="b79e0-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="b79e0-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="b79e0-133">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b79e0-133">Required</span></span> | <span data-ttu-id="b79e0-134">Altezza del rettangolo di selezione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="b79e0-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="b79e0-135">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="b79e0-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="b79e0-136">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="b79e0-136">Element Information</span></span>



|   <span data-ttu-id="b79e0-137">Elemento</span><span class="sxs-lookup"><span data-stu-id="b79e0-137">Element</span></span>    | <span data-ttu-id="b79e0-138">valore</span><span class="sxs-lookup"><span data-stu-id="b79e0-138">Value</span></span>                                                           |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="b79e0-139">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="b79e0-139">Element type</span></span> | <span data-ttu-id="b79e0-140">[**complexType TitleAreaType**](titleareatype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="b79e0-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="b79e0-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b79e0-141">Namespace</span></span>    | <span data-ttu-id="b79e0-142">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="b79e0-142">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="b79e0-143">Nome schema</span><span class="sxs-lookup"><span data-stu-id="b79e0-143">Schema name</span></span>  | <span data-ttu-id="b79e0-144">Lettore journal</span><span class="sxs-lookup"><span data-stu-id="b79e0-144">Journal Reader</span></span>                                                  |



 

 

 



