---
title: Attributo la Left
description: Attributo la Left
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474027"
---
# <a name="vml-left-attribute"></a><span data-ttu-id="6e291-103">Attributo la Left</span><span class="sxs-lookup"><span data-stu-id="6e291-103">VML Left Attribute</span></span>

<span data-ttu-id="6e291-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6e291-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6e291-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="6e291-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6e291-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="6e291-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6e291-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="6e291-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6e291-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6e291-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6e291-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6e291-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6e291-110">Determina la posizione della forma rispetto all'elemento a sinistra del flusso del documento.</span><span class="sxs-lookup"><span data-stu-id="6e291-110">Determines the position of the shape relative to the element left of it in the document flow.</span></span> <span data-ttu-id="6e291-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6e291-111">Read/write.</span></span> <span data-ttu-id="6e291-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="6e291-112">**String**.</span></span>

<span data-ttu-id="6e291-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="6e291-113">**Applies To**</span></span>

[<span data-ttu-id="6e291-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="6e291-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="6e291-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="6e291-115">**Tag Syntax**</span></span>

<span data-ttu-id="6e291-116"><v: *elemento* Style = "Left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="6e291-116"><v: *element* style="left: *expression* "></span></span>

<span data-ttu-id="6e291-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="6e291-117">**Script Syntax**</span></span>

<span data-ttu-id="6e291-118">*element* . Style. Left = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="6e291-118">*element* .style.left="*expression*"</span></span>

<span data-ttu-id="6e291-119">*espressione* = *element*. Style. Left</span><span class="sxs-lookup"><span data-stu-id="6e291-119">*expression*=*element*.style.left</span></span>

<span data-ttu-id="6e291-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="6e291-120">**Remarks**</span></span>

<span data-ttu-id="6e291-121">L'attributo **Left** è simile all'attributo HTML **Left** standard per gli stili.</span><span class="sxs-lookup"><span data-stu-id="6e291-121">The **Left** attribute is similar to the standard HTML **Left** attribute for styles.</span></span>

<span data-ttu-id="6e291-122">È possibile eseguire il mapping delle unità all'elemento padre oppure in unità assolute.</span><span class="sxs-lookup"><span data-stu-id="6e291-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="6e291-123">Questo attributo non verrà scritto per le forme ancorate inline.</span><span class="sxs-lookup"><span data-stu-id="6e291-123">This attribute will not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="6e291-124">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="6e291-124">Values include:</span></span>



| <span data-ttu-id="6e291-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6e291-125">Value</span></span>      | <span data-ttu-id="6e291-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e291-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e291-127">Auto</span><span class="sxs-lookup"><span data-stu-id="6e291-127">Auto</span></span>       | <span data-ttu-id="6e291-128">Posizione predefinita di un elemento nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="6e291-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="6e291-129">units</span><span class="sxs-lookup"><span data-stu-id="6e291-129">units</span></span>      | <span data-ttu-id="6e291-130">Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex).</span><span class="sxs-lookup"><span data-stu-id="6e291-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="6e291-131">Se non viene specificata alcuna unità, viene utilizzato pixels (px).</span><span class="sxs-lookup"><span data-stu-id="6e291-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="6e291-132">percentuale</span><span class="sxs-lookup"><span data-stu-id="6e291-132">percentage</span></span> | <span data-ttu-id="6e291-133">Valore espresso come percentuale della larghezza dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="6e291-133">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="6e291-134">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="6e291-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="6e291-135">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="6e291-135">**See Also**</span></span>

[<span data-ttu-id="6e291-136">Unità</span><span class="sxs-lookup"><span data-stu-id="6e291-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="6e291-137">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="6e291-137">**Example**</span></span>

<span data-ttu-id="6e291-138">Il valore sinistro della forma è impostato su 1 nell'esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="6e291-138">The left value of the shape is set to 1 in the example below.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="6e291-139">[Esempio di attributo Left](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span><span class="sxs-lookup"><span data-stu-id="6e291-139">[Left Attribute Example](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span></span> <span data-ttu-id="6e291-140">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="6e291-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 