---
title: Attributo Margin-Right la
description: Attributo Margin-Right la
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047336"
---
# <a name="vml-margin-right-attribute"></a><span data-ttu-id="d2925-103">Attributo Margin-Right la</span><span class="sxs-lookup"><span data-stu-id="d2925-103">VML Margin-Right Attribute</span></span>

<span data-ttu-id="d2925-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d2925-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d2925-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d2925-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d2925-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d2925-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d2925-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d2925-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d2925-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d2925-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d2925-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d2925-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d2925-110">Specifica il bordo destro del rettangolo che lo contiene della forma rispetto all'ancoraggio della forma.</span><span class="sxs-lookup"><span data-stu-id="d2925-110">Specifies the right edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="d2925-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d2925-111">Read/write.</span></span> <span data-ttu-id="d2925-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="d2925-112">**String**.</span></span>

<span data-ttu-id="d2925-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d2925-113">**Applies To**</span></span>

[<span data-ttu-id="d2925-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="d2925-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d2925-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d2925-115">**Tag Syntax**</span></span>

<span data-ttu-id="d2925-116"><v: *elemento* Style = "margin-right: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d2925-116"><v: *element* style="margin-right: *expression* "></span></span>

<span data-ttu-id="d2925-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d2925-117">**Script Syntax**</span></span>

<span data-ttu-id="d2925-118">*element* . Style. MarginRight = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d2925-118">*element* .style.marginright="*expression*"</span></span>

<span data-ttu-id="d2925-119">*espressione* = *element*. Style. MarginRight</span><span class="sxs-lookup"><span data-stu-id="d2925-119">*expression*=*element*.style.marginright</span></span>

<span data-ttu-id="d2925-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d2925-120">**Remarks**</span></span>

<span data-ttu-id="d2925-121">L'attributo **margin-right** è simile all'attributo standard **margin-right** HTML usato con i fogli di stile.</span><span class="sxs-lookup"><span data-stu-id="d2925-121">The **Margin-Right** attribute is similar to the standard HTML **Margin-Right** attribute used with style sheets.</span></span>

<span data-ttu-id="d2925-122">Si noti che viene usato **MarginRight** anziché **margin-right** per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="d2925-122">Note that **marginright** is used instead of **margin-right** for scripting.</span></span> <span data-ttu-id="d2925-123">Si noti inoltre che se la **posizione** è **assoluta**, il margine non verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="d2925-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="d2925-124">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="d2925-124">Values include:</span></span>



| <span data-ttu-id="d2925-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d2925-125">Value</span></span>      | <span data-ttu-id="d2925-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2925-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2925-127">Auto</span><span class="sxs-lookup"><span data-stu-id="d2925-127">Auto</span></span>       | <span data-ttu-id="d2925-128">Posizione predefinita di un elemento nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="d2925-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="d2925-129">units</span><span class="sxs-lookup"><span data-stu-id="d2925-129">units</span></span>      | <span data-ttu-id="d2925-130">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d2925-130">Default.</span></span> <span data-ttu-id="d2925-131">Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex).</span><span class="sxs-lookup"><span data-stu-id="d2925-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="d2925-132">Se non viene specificata alcuna unità, viene utilizzato pixels (px).</span><span class="sxs-lookup"><span data-stu-id="d2925-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="d2925-133">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="d2925-133">The default value is 0.</span></span> |
| <span data-ttu-id="d2925-134">percentuale</span><span class="sxs-lookup"><span data-stu-id="d2925-134">percentage</span></span> | <span data-ttu-id="d2925-135">Valore espresso come percentuale dell'altezza dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="d2925-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="d2925-136">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="d2925-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="d2925-137">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="d2925-137">**See Also**</span></span>

[<span data-ttu-id="d2925-138">Unità</span><span class="sxs-lookup"><span data-stu-id="d2925-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="d2925-139">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d2925-139">**Example**</span></span>

<span data-ttu-id="d2925-140">Il margine destro è impostato su 25 pixel.</span><span class="sxs-lookup"><span data-stu-id="d2925-140">The right margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



<span data-ttu-id="d2925-141">[Esempio di attributo margin-right](/previous-versions/bb229677(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2925-141">[Margin-Right Attribute Example](/previous-versions/bb229677(v=vs.85)).</span></span> <span data-ttu-id="d2925-142">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="d2925-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 