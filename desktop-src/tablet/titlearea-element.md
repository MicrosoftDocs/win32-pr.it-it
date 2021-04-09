---
description: Contiene la posizione e le informazioni di delimitazione per il titolo della nota, se presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento elemento titlearea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968515"
---
# <a name="titlearea-element"></a><span data-ttu-id="0eaa4-103">Elemento elemento titlearea</span><span class="sxs-lookup"><span data-stu-id="0eaa4-103">TitleArea Element</span></span>

<span data-ttu-id="0eaa4-104">Contiene la posizione e le informazioni di delimitazione per il titolo della nota, se presente.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="0eaa4-105">Definizione</span><span class="sxs-lookup"><span data-stu-id="0eaa4-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="0eaa4-106">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="0eaa4-106">Parent Elements</span></span>

[<span data-ttu-id="0eaa4-107">**Titolo**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="0eaa4-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0eaa4-108">Child Elements</span></span>

<span data-ttu-id="0eaa4-109">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="0eaa4-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="0eaa4-110">Attributes</span></span>



| <span data-ttu-id="0eaa4-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="0eaa4-111">Attribute</span></span>  | <span data-ttu-id="0eaa4-112">Type</span><span class="sxs-lookup"><span data-stu-id="0eaa4-112">Type</span></span>                      | <span data-ttu-id="0eaa4-113">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="0eaa4-113">Required</span></span> | <span data-ttu-id="0eaa4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eaa4-114">Description</span></span>                                                                             | <span data-ttu-id="0eaa4-115">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0eaa4-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="0eaa4-116">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-116">**Left**</span></span>   | <span data-ttu-id="0eaa4-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-117">**xs:integer**</span></span>            | <span data-ttu-id="0eaa4-118">Necessario</span><span class="sxs-lookup"><span data-stu-id="0eaa4-118">Required</span></span> | <span data-ttu-id="0eaa4-119">Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="0eaa4-120">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-120">Any integer.</span></span>              |
| <span data-ttu-id="0eaa4-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-121">**Top**</span></span>    | <span data-ttu-id="0eaa4-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-122">**xs:integer**</span></span>            | <span data-ttu-id="0eaa4-123">Necessario</span><span class="sxs-lookup"><span data-stu-id="0eaa4-123">Required</span></span> | <span data-ttu-id="0eaa4-124">Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="0eaa4-125">Qualsiasi numero intero.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-125">Any integer.</span></span>              |
| <span data-ttu-id="0eaa4-126">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-126">**Width**</span></span>  | <span data-ttu-id="0eaa4-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0eaa4-128">Necessario</span><span class="sxs-lookup"><span data-stu-id="0eaa4-128">Required</span></span> | <span data-ttu-id="0eaa4-129">Larghezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="0eaa4-130">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="0eaa4-131">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-131">**Height**</span></span> | <span data-ttu-id="0eaa4-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0eaa4-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0eaa4-133">Necessario</span><span class="sxs-lookup"><span data-stu-id="0eaa4-133">Required</span></span> | <span data-ttu-id="0eaa4-134">Altezza del rettangolo di delimitazione per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="0eaa4-135">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="0eaa4-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="0eaa4-136">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="0eaa4-136">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="0eaa4-137">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="0eaa4-137">Element type</span></span> | <span data-ttu-id="0eaa4-138">ComplexType [**TitleAreaType**](titleareatype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="0eaa4-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="0eaa4-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0eaa4-139">Namespace</span></span>    | <span data-ttu-id="0eaa4-140">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="0eaa4-140">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="0eaa4-141">Nome schema</span><span class="sxs-lookup"><span data-stu-id="0eaa4-141">Schema name</span></span>  | <span data-ttu-id="0eaa4-142">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="0eaa4-142">Journal Reader</span></span>                                                  |



 

 

 



