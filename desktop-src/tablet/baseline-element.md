---
description: Fornisce le informazioni (x, y) per i punti iniziale e finale della linea di base di un paragrafo nel documento Journal. Lo spazio delle coordinate usato per questi valori è HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento Baseline
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225874"
---
# <a name="baseline-element"></a><span data-ttu-id="51f1f-104">Elemento Baseline</span><span class="sxs-lookup"><span data-stu-id="51f1f-104">Baseline Element</span></span>

<span data-ttu-id="51f1f-105">Fornisce le informazioni (x, y) per i punti iniziale e finale della linea di base di un paragrafo nel documento Journal.</span><span class="sxs-lookup"><span data-stu-id="51f1f-105">Provides (x, y) information for the starting and ending points of the baseline of a paragraph in the Journal document.</span></span> <span data-ttu-id="51f1f-106">Lo spazio delle coordinate usato per questi valori è **HIMETRIC**.</span><span class="sxs-lookup"><span data-stu-id="51f1f-106">The coordinate space used for these values is **HIMETRIC**.</span></span>

## <a name="definition"></a><span data-ttu-id="51f1f-107">Definizione</span><span class="sxs-lookup"><span data-stu-id="51f1f-107">Definition</span></span>

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a><span data-ttu-id="51f1f-108">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="51f1f-108">Parent Elements</span></span>

[<span data-ttu-id="51f1f-109">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="51f1f-109">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="child-elements"></a><span data-ttu-id="51f1f-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="51f1f-110">Child Elements</span></span>

<span data-ttu-id="51f1f-111">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="51f1f-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="51f1f-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="51f1f-112">Attributes</span></span>



| <span data-ttu-id="51f1f-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="51f1f-113">Attribute</span></span>  | <span data-ttu-id="51f1f-114">Type</span><span class="sxs-lookup"><span data-stu-id="51f1f-114">Type</span></span>                      | <span data-ttu-id="51f1f-115">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="51f1f-115">Required</span></span> | <span data-ttu-id="51f1f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51f1f-116">Description</span></span>                                                      | <span data-ttu-id="51f1f-117">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="51f1f-117">Possible Values</span></span>           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="51f1f-118">**StartX**</span><span class="sxs-lookup"><span data-stu-id="51f1f-118">**StartX**</span></span> | <span data-ttu-id="51f1f-119">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="51f1f-119">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="51f1f-120">Necessario</span><span class="sxs-lookup"><span data-stu-id="51f1f-120">Required</span></span> | <span data-ttu-id="51f1f-121">Valore X per il punto che contrassegna l'inizio della linea di base.</span><span class="sxs-lookup"><span data-stu-id="51f1f-121">The X value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="51f1f-122">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="51f1f-122">Any non-negative integer.</span></span> |
| <span data-ttu-id="51f1f-123">**StartY**</span><span class="sxs-lookup"><span data-stu-id="51f1f-123">**StartY**</span></span> | <span data-ttu-id="51f1f-124">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="51f1f-124">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="51f1f-125">Necessario</span><span class="sxs-lookup"><span data-stu-id="51f1f-125">Required</span></span> | <span data-ttu-id="51f1f-126">Valore Y per il punto che contrassegna l'inizio della linea di base.</span><span class="sxs-lookup"><span data-stu-id="51f1f-126">The Y value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="51f1f-127">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="51f1f-127">Any non-negative integer.</span></span> |
| <span data-ttu-id="51f1f-128">**EndX**</span><span class="sxs-lookup"><span data-stu-id="51f1f-128">**EndX**</span></span>   | <span data-ttu-id="51f1f-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="51f1f-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="51f1f-130">Necessario</span><span class="sxs-lookup"><span data-stu-id="51f1f-130">Required</span></span> | <span data-ttu-id="51f1f-131">Valore X per il punto che contrassegna la fine della linea di base.</span><span class="sxs-lookup"><span data-stu-id="51f1f-131">The X value for the point marking the end of the baseline.</span></span>       | <span data-ttu-id="51f1f-132">Qualsiasi numero intero non negativo.</span><span class="sxs-lookup"><span data-stu-id="51f1f-132">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="51f1f-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="51f1f-133">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="51f1f-134">Tipo di elemento</span><span class="sxs-lookup"><span data-stu-id="51f1f-134">Element type</span></span> | <span data-ttu-id="51f1f-135">ComplexType [**BaselineType**](baselinetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="51f1f-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="51f1f-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="51f1f-136">Namespace</span></span>    | <span data-ttu-id="51f1f-137">urn: schemas-microsoft-com: TabletPC: RichInk</span><span class="sxs-lookup"><span data-stu-id="51f1f-137">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="51f1f-138">Nome schema</span><span class="sxs-lookup"><span data-stu-id="51f1f-138">Schema name</span></span>  | <span data-ttu-id="51f1f-139">Lettore Journal</span><span class="sxs-lookup"><span data-stu-id="51f1f-139">Journal Reader</span></span>                                                |



 

 

 



