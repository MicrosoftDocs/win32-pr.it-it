---
title: Attributo Width la
description: Attributo Width la
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299951"
---
# <a name="vml-width-attribute"></a><span data-ttu-id="e03a1-103">Attributo Width la</span><span class="sxs-lookup"><span data-stu-id="e03a1-103">VML Width Attribute</span></span>

<span data-ttu-id="e03a1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e03a1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e03a1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e03a1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e03a1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e03a1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e03a1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e03a1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e03a1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e03a1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e03a1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e03a1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e03a1-110">Definisce la larghezza della forma.</span><span class="sxs-lookup"><span data-stu-id="e03a1-110">Defines the width of the shape.</span></span> <span data-ttu-id="e03a1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e03a1-111">Read/write.</span></span> <span data-ttu-id="e03a1-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="e03a1-112">**String**.</span></span>

<span data-ttu-id="e03a1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e03a1-113">**Applies To**</span></span>

[<span data-ttu-id="e03a1-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="e03a1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e03a1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e03a1-115">**Tag Syntax**</span></span>

<span data-ttu-id="e03a1-116"><v: *elemento* Style = "width: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e03a1-116"><v: *element* style="width: *expression* "></span></span>

<span data-ttu-id="e03a1-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e03a1-117">**Script Syntax**</span></span>

<span data-ttu-id="e03a1-118">*element* . Style. Width = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e03a1-118">*element* .style.width="*expression*"</span></span>

<span data-ttu-id="e03a1-119">*espressione* = *element*. Style. Width</span><span class="sxs-lookup"><span data-stu-id="e03a1-119">*expression*=*element*.style.width</span></span>

<span data-ttu-id="e03a1-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e03a1-120">**Remarks**</span></span>

<span data-ttu-id="e03a1-121">L'attributo **Width** è simile all'attributo **Width** HTML standard per gli stili.</span><span class="sxs-lookup"><span data-stu-id="e03a1-121">The **Width** attribute is similar to the standard HTML **Width** attribute for styles.</span></span>

<span data-ttu-id="e03a1-122">È possibile eseguire il mapping delle unità all'elemento padre oppure in unità assolute.</span><span class="sxs-lookup"><span data-stu-id="e03a1-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="e03a1-123">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="e03a1-123">Values include:</span></span>



| <span data-ttu-id="e03a1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e03a1-124">Value</span></span>      | <span data-ttu-id="e03a1-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e03a1-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03a1-126">Auto</span><span class="sxs-lookup"><span data-stu-id="e03a1-126">Auto</span></span>       | <span data-ttu-id="e03a1-127">Posizione predefinita di un elemento nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="e03a1-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="e03a1-128">units</span><span class="sxs-lookup"><span data-stu-id="e03a1-128">units</span></span>      | <span data-ttu-id="e03a1-129">Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex).</span><span class="sxs-lookup"><span data-stu-id="e03a1-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="e03a1-130">Se non viene specificata alcuna unità, viene utilizzato pixels (px).</span><span class="sxs-lookup"><span data-stu-id="e03a1-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="e03a1-131">percentuale</span><span class="sxs-lookup"><span data-stu-id="e03a1-131">percentage</span></span> | <span data-ttu-id="e03a1-132">Valore espresso come percentuale della larghezza dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="e03a1-132">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="e03a1-133">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="e03a1-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="e03a1-134">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="e03a1-134">**See Also**</span></span>

[<span data-ttu-id="e03a1-135">Unità</span><span class="sxs-lookup"><span data-stu-id="e03a1-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="e03a1-136">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e03a1-136">**Example**</span></span>

<span data-ttu-id="e03a1-137">La larghezza della forma è 25.</span><span class="sxs-lookup"><span data-stu-id="e03a1-137">The width of the shape is 25.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



<span data-ttu-id="e03a1-138">[Esempio di attributo Width](/previous-versions/bb264101(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e03a1-138">[Width Attribute Example](/previous-versions/bb264101(v=vs.85)).</span></span> <span data-ttu-id="e03a1-139">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="e03a1-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 