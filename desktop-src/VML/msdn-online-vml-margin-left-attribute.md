---
title: Attributo Margin-Left la
description: Attributo Margin-Left la
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f98900e862f22f31ad444bc6fb6f372627eca1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338366"
---
# <a name="vml-margin-left-attribute"></a><span data-ttu-id="f2325-103">Attributo Margin-Left la</span><span class="sxs-lookup"><span data-stu-id="f2325-103">VML Margin-Left Attribute</span></span>

<span data-ttu-id="f2325-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f2325-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f2325-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="f2325-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f2325-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="f2325-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f2325-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="f2325-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f2325-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f2325-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f2325-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f2325-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f2325-110">Specifica il bordo sinistro del rettangolo che lo contiene della forma rispetto all'ancoraggio della forma.</span><span class="sxs-lookup"><span data-stu-id="f2325-110">Specifies the left edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="f2325-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f2325-111">Read/write.</span></span> <span data-ttu-id="f2325-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f2325-112">**String**.</span></span>

<span data-ttu-id="f2325-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="f2325-113">**Applies To**</span></span>

[<span data-ttu-id="f2325-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="f2325-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f2325-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="f2325-115">**Tag Syntax**</span></span>

<span data-ttu-id="f2325-116"><v: *elemento* Style = "margin-left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f2325-116"><v: *element* style="margin-left: *expression* "></span></span>

<span data-ttu-id="f2325-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="f2325-117">**Script Syntax**</span></span>

<span data-ttu-id="f2325-118">*element* . Style. MarginLeft = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="f2325-118">*element* .style.marginleft="*expression*"</span></span>

<span data-ttu-id="f2325-119">*espressione* = *element*. Style. MarginLeft</span><span class="sxs-lookup"><span data-stu-id="f2325-119">*expression*=*element*.style.marginleft</span></span>

<span data-ttu-id="f2325-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="f2325-120">**Remarks**</span></span>

<span data-ttu-id="f2325-121">L'attributo **margin-left** è simile all'attributo **margin-left** HTML standard usato con i fogli di stile.</span><span class="sxs-lookup"><span data-stu-id="f2325-121">The **Margin-Left** attribute is similar to the standard HTML **Margin-Left** attribute used with style sheets.</span></span>

<span data-ttu-id="f2325-122">Si noti che viene usato **MarginLeft** anziché **margin-left** per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="f2325-122">Note that **marginleft** is used instead of **margin-left** for scripting.</span></span> <span data-ttu-id="f2325-123">Si noti inoltre che se la **posizione** è **assoluta**, il margine non verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="f2325-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="f2325-124">Questa proprietà viene usata al posto di **Left** per le forme in Microsoft Word e Microsoft Excel che si trovano in una posizione relativa a un punto di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="f2325-124">This property is used instead of **Left** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="f2325-125">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="f2325-125">Values include:</span></span>



| <span data-ttu-id="f2325-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f2325-126">Value</span></span>      | <span data-ttu-id="f2325-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2325-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2325-128">Auto</span><span class="sxs-lookup"><span data-stu-id="f2325-128">Auto</span></span>       | <span data-ttu-id="f2325-129">Posizione predefinita di un elemento nel flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="f2325-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="f2325-130">units</span><span class="sxs-lookup"><span data-stu-id="f2325-130">units</span></span>      | <span data-ttu-id="f2325-131">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f2325-131">Default.</span></span> <span data-ttu-id="f2325-132">Un numero con un indicatore di unità assoluto (cm, mm, in, PT, PC o px) o un designatore di unità relative (em o ex).</span><span class="sxs-lookup"><span data-stu-id="f2325-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="f2325-133">Se non viene specificata alcuna unità, viene utilizzato pixels (px).</span><span class="sxs-lookup"><span data-stu-id="f2325-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="f2325-134">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="f2325-134">The default value is 0.</span></span> |
| <span data-ttu-id="f2325-135">percentuale</span><span class="sxs-lookup"><span data-stu-id="f2325-135">percentage</span></span> | <span data-ttu-id="f2325-136">Valore espresso come percentuale dell'altezza dell'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="f2325-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="f2325-137">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="f2325-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="f2325-138">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="f2325-138">**See Also**</span></span>

[<span data-ttu-id="f2325-139">Unità</span><span class="sxs-lookup"><span data-stu-id="f2325-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="f2325-140">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="f2325-140">**Example**</span></span>

<span data-ttu-id="f2325-141">Il margine sinistro è impostato su 25 pixel.</span><span class="sxs-lookup"><span data-stu-id="f2325-141">The left margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



<span data-ttu-id="f2325-142">[Esempio di attributo margin-left](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span><span class="sxs-lookup"><span data-stu-id="f2325-142">[Margin-Left Attribute Example](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span></span> <span data-ttu-id="f2325-143">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="f2325-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 