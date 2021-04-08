---
title: Attributo Margin-Bottom la
description: Attributo Margin-Bottom la
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728823"
---
# <a name="vml-margin-bottom-attribute"></a><span data-ttu-id="3f176-103">Attributo Margin-Bottom la</span><span class="sxs-lookup"><span data-stu-id="3f176-103">VML Margin-Bottom Attribute</span></span>

<span data-ttu-id="3f176-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3f176-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3f176-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3f176-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3f176-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3f176-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3f176-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3f176-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3f176-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3f176-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3f176-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3f176-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3f176-110">Specifica il bordo inferiore del rettangolo che lo contiene della forma rispetto all'ancoraggio della forma.</span><span class="sxs-lookup"><span data-stu-id="3f176-110">Specifies the bottom edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="3f176-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3f176-111">Read/write.</span></span> <span data-ttu-id="3f176-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="3f176-112">**String**.</span></span>

<span data-ttu-id="3f176-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="3f176-113">**Applies To**</span></span>

[<span data-ttu-id="3f176-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="3f176-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3f176-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="3f176-115">**Tag Syntax**</span></span>

<span data-ttu-id="3f176-116"><v: *elemento* margin-bottom = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3f176-116"><v: *element* margin-bottom=" *expression* "></span></span>

<span data-ttu-id="3f176-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="3f176-117">**Script Syntax**</span></span>

<span data-ttu-id="3f176-118">*element* . MarginBottom = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="3f176-118">*element* .marginbottom="*expression*"</span></span>

<span data-ttu-id="3f176-119">*espressione* = *elemento*. MarginBottom</span><span class="sxs-lookup"><span data-stu-id="3f176-119">*expression*=*element*.marginbottom</span></span>

<span data-ttu-id="3f176-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="3f176-120">**Remarks**</span></span>

<span data-ttu-id="3f176-121">L'attributo **margin-bottom** è simile all'attributo **margin-bottom** HTML standard usato con i fogli di stile.</span><span class="sxs-lookup"><span data-stu-id="3f176-121">The **Margin-Bottom** attribute is similar to the standard HTML **Margin-Bottom** attribute used with style sheets.</span></span>

<span data-ttu-id="3f176-122">Si noti che **MarginBottom** viene usato al posto del **margine inferiore** per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="3f176-122">Note that **marginbottom** is used instead of **margin-bottom** for scripting.</span></span> <span data-ttu-id="3f176-123">Si noti inoltre che se la **posizione** è **assoluta**, il margine non verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="3f176-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="3f176-124">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="3f176-124">Values include:</span></span>



| <span data-ttu-id="3f176-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3f176-125">Value</span></span>      | <span data-ttu-id="3f176-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f176-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f176-127">Auto</span><span class="sxs-lookup"><span data-stu-id="3f176-127">Auto</span></span>       | <span data-ttu-id="3f176-128">Posizione predefinita di un elemento nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="3f176-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="3f176-129">units</span><span class="sxs-lookup"><span data-stu-id="3f176-129">units</span></span>      | <span data-ttu-id="3f176-130">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3f176-130">Default.</span></span> <span data-ttu-id="3f176-131">Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex).</span><span class="sxs-lookup"><span data-stu-id="3f176-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="3f176-132">Se non viene specificata alcuna unità, viene utilizzato pixels (px).</span><span class="sxs-lookup"><span data-stu-id="3f176-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="3f176-133">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="3f176-133">The default value is 0.</span></span> |
| <span data-ttu-id="3f176-134">percentuale</span><span class="sxs-lookup"><span data-stu-id="3f176-134">percentage</span></span> | <span data-ttu-id="3f176-135">Valore espresso come percentuale dell'altezza dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="3f176-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="3f176-136">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="3f176-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="3f176-137">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="3f176-137">**See Also**</span></span>

[<span data-ttu-id="3f176-138">Unità</span><span class="sxs-lookup"><span data-stu-id="3f176-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="3f176-139">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="3f176-139">**Example**</span></span>

<span data-ttu-id="3f176-140">Il margine inferiore è impostato su 25 pixel.</span><span class="sxs-lookup"><span data-stu-id="3f176-140">The bottom margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



<span data-ttu-id="3f176-141">[Esempio di attributo margin-bottom](/previous-versions/bb229675(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f176-141">[Margin-Bottom Attribute Example](/previous-versions/bb229675(v=vs.85)).</span></span> <span data-ttu-id="3f176-142">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="3f176-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 