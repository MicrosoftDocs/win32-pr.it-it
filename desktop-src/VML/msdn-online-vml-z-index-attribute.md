---
title: LA-attributo Z-index
description: LA-attributo Z-index
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963148"
---
# <a name="vml-z-index-attribute"></a><span data-ttu-id="a6902-103">LA-attributo Z-index</span><span class="sxs-lookup"><span data-stu-id="a6902-103">VML Z-Index Attribute</span></span>

<span data-ttu-id="a6902-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a6902-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a6902-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a6902-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a6902-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a6902-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a6902-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a6902-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a6902-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a6902-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a6902-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a6902-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a6902-110">Determina l'ordine di visualizzazione delle forme sovrapposte.</span><span class="sxs-lookup"><span data-stu-id="a6902-110">Determines the display order of overlapping shapes.</span></span> <span data-ttu-id="a6902-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a6902-111">Read/write.</span></span> <span data-ttu-id="a6902-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="a6902-112">**String**.</span></span>

<span data-ttu-id="a6902-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="a6902-113">**Applies To**</span></span>

[<span data-ttu-id="a6902-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="a6902-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a6902-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="a6902-115">**Tag Syntax**</span></span>

<span data-ttu-id="a6902-116"><v: *elemento* Style = "z-index: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a6902-116"><v: *element* style="z-index: *expression* "></span></span>

<span data-ttu-id="a6902-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="a6902-117">**Script Syntax**</span></span>

<span data-ttu-id="a6902-118">*element* . Style. ZIndex = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="a6902-118">*element* .style.zindex="*expression*"</span></span>

<span data-ttu-id="a6902-119">*espressione* = *element*. Style. ZIndex</span><span class="sxs-lookup"><span data-stu-id="a6902-119">*expression*=*element*.style.zindex</span></span>

<span data-ttu-id="a6902-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="a6902-120">**Remarks**</span></span>

<span data-ttu-id="a6902-121">L'attributo **z-index** è simile all'attributo standard HTML **z-index** per gli stili.</span><span class="sxs-lookup"><span data-stu-id="a6902-121">The **Z-Index** attribute is similar to the standard HTML **Z-Index** attribute for styles.</span></span>

<span data-ttu-id="a6902-122">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="a6902-122">Values include:</span></span>



| <span data-ttu-id="a6902-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a6902-123">Value</span></span> | <span data-ttu-id="a6902-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6902-124">Description</span></span>                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6902-125">Auto</span><span class="sxs-lookup"><span data-stu-id="a6902-125">Auto</span></span>  | <span data-ttu-id="a6902-126">Verrà utilizzato l'ordine in cui vengono visualizzate le forme nella pagina HTML, dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="a6902-126">The order that the shapes appear in the HTML page will be used, bottom to top.</span></span>                                                                                                                         |
| <span data-ttu-id="a6902-127">order</span><span class="sxs-lookup"><span data-stu-id="a6902-127">order</span></span> | <span data-ttu-id="a6902-128">Numero che rappresenta la precedenza di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="a6902-128">A number that represents the stacking precedence.</span></span> <span data-ttu-id="a6902-129">Una forma con un numero più alto verrà visualizzata come se wereoverlapping (in "front" di) una forma con un numero inferiore.</span><span class="sxs-lookup"><span data-stu-id="a6902-129">A shape with a a higher number will be displayed as if it wereoverlapping (in "front" of) a shape with a lower number.</span></span> <span data-ttu-id="a6902-130">È possibile usare i numeri negativi.</span><span class="sxs-lookup"><span data-stu-id="a6902-130">Negative numbers can be used.</span></span> |



 

<span data-ttu-id="a6902-131">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="a6902-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="a6902-132">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="a6902-132">**Example**</span></span>

<span data-ttu-id="a6902-133">La forma rossa verrà visualizzata in "anteriore" della forma blu, perché ha un indice z superiore.</span><span class="sxs-lookup"><span data-stu-id="a6902-133">The red shape will be displayed in "front" of the blue shape, because it has a higher z-index.</span></span>


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



<span data-ttu-id="a6902-134">[Esempio di attributo Z-index](/previous-versions/ms530275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a6902-134">[Z-Index Attribute Example](/previous-versions/ms530275(v=vs.85)).</span></span> <span data-ttu-id="a6902-135">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="a6902-135">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 