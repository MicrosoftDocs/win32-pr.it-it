---
title: Attributo Height la
description: Attributo Height la
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117950"
---
# <a name="vml-height-attribute"></a><span data-ttu-id="e9d74-103">Attributo Height la</span><span class="sxs-lookup"><span data-stu-id="e9d74-103">VML Height Attribute</span></span>

<span data-ttu-id="e9d74-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e9d74-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e9d74-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e9d74-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e9d74-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e9d74-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e9d74-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e9d74-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e9d74-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e9d74-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e9d74-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e9d74-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e9d74-110">Specifica l'altezza della forma.</span><span class="sxs-lookup"><span data-stu-id="e9d74-110">Specifies the height of the shape.</span></span> <span data-ttu-id="e9d74-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e9d74-111">Read/write.</span></span> <span data-ttu-id="e9d74-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="e9d74-112">**String**.</span></span>

<span data-ttu-id="e9d74-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e9d74-113">**Applies To**</span></span>

[<span data-ttu-id="e9d74-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="e9d74-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e9d74-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e9d74-115">**Tag Syntax**</span></span>

<span data-ttu-id="e9d74-116"><v: *elemento* Style = "height: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e9d74-116"><v: *element* style="height: *expression* "></span></span>

<span data-ttu-id="e9d74-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e9d74-117">**Script Syntax**</span></span>

<span data-ttu-id="e9d74-118">*element* . Style. Height = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e9d74-118">*element* .style.height="*expression*"</span></span>

<span data-ttu-id="e9d74-119">*espressione* = *element*. Style. Height</span><span class="sxs-lookup"><span data-stu-id="e9d74-119">*expression*=*element*.style.height</span></span>

<span data-ttu-id="e9d74-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e9d74-120">**Remarks**</span></span>

<span data-ttu-id="e9d74-121">L'attributo **Height** è simile all'attributo **Height** HTML standard per gli stili.</span><span class="sxs-lookup"><span data-stu-id="e9d74-121">The **Height** attribute is similar to the standard HTML **Height** attribute for styles.</span></span>

<span data-ttu-id="e9d74-122">È possibile eseguire il mapping delle unità all'elemento padre oppure in unità assolute.</span><span class="sxs-lookup"><span data-stu-id="e9d74-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="e9d74-123">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="e9d74-123">Values include:</span></span>



| <span data-ttu-id="e9d74-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e9d74-124">Value</span></span>      | <span data-ttu-id="e9d74-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9d74-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d74-126">Auto</span><span class="sxs-lookup"><span data-stu-id="e9d74-126">Auto</span></span>       | <span data-ttu-id="e9d74-127">Posizione predefinita di un elemento nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="e9d74-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="e9d74-128">units</span><span class="sxs-lookup"><span data-stu-id="e9d74-128">units</span></span>      | <span data-ttu-id="e9d74-129">Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex).</span><span class="sxs-lookup"><span data-stu-id="e9d74-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="e9d74-130">Se non viene specificata alcuna unità, viene utilizzato pixels (px).</span><span class="sxs-lookup"><span data-stu-id="e9d74-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="e9d74-131">percentuale</span><span class="sxs-lookup"><span data-stu-id="e9d74-131">percentage</span></span> | <span data-ttu-id="e9d74-132">Valore espresso come percentuale dell'altezza dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="e9d74-132">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="e9d74-133">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="e9d74-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="e9d74-134">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="e9d74-134">**See Also**</span></span>

[<span data-ttu-id="e9d74-135">Unità</span><span class="sxs-lookup"><span data-stu-id="e9d74-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="e9d74-136">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e9d74-136">**Example**</span></span>

<span data-ttu-id="e9d74-137">L'altezza della forma è impostata su 30.</span><span class="sxs-lookup"><span data-stu-id="e9d74-137">The height of the shape is set to 30.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



<span data-ttu-id="e9d74-138">[Esempio di attributo Height](/previous-versions/bb229671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9d74-138">[Height Attribute Example](/previous-versions/bb229671(v=vs.85)).</span></span> <span data-ttu-id="e9d74-139">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="e9d74-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 