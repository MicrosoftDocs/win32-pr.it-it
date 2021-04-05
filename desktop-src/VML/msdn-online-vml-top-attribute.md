---
title: LA attributo Top
description: LA attributo Top
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728242"
---
# <a name="vml-top-attribute"></a><span data-ttu-id="3217a-103">LA attributo Top</span><span class="sxs-lookup"><span data-stu-id="3217a-103">VML Top Attribute</span></span>

<span data-ttu-id="3217a-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3217a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3217a-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3217a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3217a-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3217a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3217a-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3217a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3217a-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3217a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3217a-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3217a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3217a-110">Definisce la posizione della forma rispetto all'elemento sopra di esso nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="3217a-110">Defines the position of the shape relative to the element above it in the flow of the page.</span></span> <span data-ttu-id="3217a-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3217a-111">Read/write.</span></span> <span data-ttu-id="3217a-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="3217a-112">**String**.</span></span>

<span data-ttu-id="3217a-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="3217a-113">**Applies To**</span></span>

[<span data-ttu-id="3217a-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="3217a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3217a-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="3217a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3217a-116"><v: *elemento* Style = "Top: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3217a-116"><v: *element* style="top: *expression* "></span></span>

<span data-ttu-id="3217a-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="3217a-117">**Script Syntax**</span></span>

<span data-ttu-id="3217a-118">*element* . Style.Top = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="3217a-118">*element* .style.top="*expression*"</span></span>

<span data-ttu-id="3217a-119">*espressione* = *elemento*. Style.Top</span><span class="sxs-lookup"><span data-stu-id="3217a-119">*expression*=*element*.style.top</span></span>

<span data-ttu-id="3217a-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="3217a-120">**Remarks**</span></span>

<span data-ttu-id="3217a-121">L'attributo **Top** è simile all'attributo **Top** HTML standard per gli stili.</span><span class="sxs-lookup"><span data-stu-id="3217a-121">The **Top** attribute is similar to the standard HTML **Top** attribute for styles.</span></span>

<span data-ttu-id="3217a-122">È possibile eseguire il mapping delle unità all'elemento padre oppure in unità assolute.</span><span class="sxs-lookup"><span data-stu-id="3217a-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="3217a-123">Questo attributo non può essere scritto per forme ancorate inline.</span><span class="sxs-lookup"><span data-stu-id="3217a-123">This attribute may not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="3217a-124">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="3217a-124">Values include:</span></span>



| <span data-ttu-id="3217a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3217a-125">Value</span></span>      | <span data-ttu-id="3217a-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3217a-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3217a-127">Auto</span><span class="sxs-lookup"><span data-stu-id="3217a-127">Auto</span></span>       | <span data-ttu-id="3217a-128">Posizione predefinita di un elemento nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="3217a-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="3217a-129">units</span><span class="sxs-lookup"><span data-stu-id="3217a-129">units</span></span>      | <span data-ttu-id="3217a-130">Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex).</span><span class="sxs-lookup"><span data-stu-id="3217a-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="3217a-131">Se non viene specificata alcuna unità, viene utilizzato pixels (px).</span><span class="sxs-lookup"><span data-stu-id="3217a-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="3217a-132">percentuale</span><span class="sxs-lookup"><span data-stu-id="3217a-132">percentage</span></span> | <span data-ttu-id="3217a-133">Valore espresso come percentuale dell'altezza dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="3217a-133">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="3217a-134">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="3217a-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="3217a-135">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="3217a-135">**See Also**</span></span>

[<span data-ttu-id="3217a-136">Unità</span><span class="sxs-lookup"><span data-stu-id="3217a-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="3217a-137">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="3217a-137">**Example**</span></span>

<span data-ttu-id="3217a-138">Il bordo superiore della forma è 5 pixel sotto l'oggetto che lo precede nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="3217a-138">The top edge of the shape is 5 pixels below the object that precedes it in the flow of the page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="3217a-139">[Esempio di attributo Top](/previous-versions/bb264098(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3217a-139">[Top Attribute Example](/previous-versions/bb264098(v=vs.85)).</span></span> <span data-ttu-id="3217a-140">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="3217a-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 