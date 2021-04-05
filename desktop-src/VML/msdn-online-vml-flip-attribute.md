---
title: LA (attributo Flip)
description: LA (attributo Flip)
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730146"
---
# <a name="vml-flip-attribute"></a><span data-ttu-id="f63f1-103">LA (attributo Flip)</span><span class="sxs-lookup"><span data-stu-id="f63f1-103">VML Flip Attribute</span></span>

<span data-ttu-id="f63f1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f63f1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f63f1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="f63f1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f63f1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="f63f1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f63f1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="f63f1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f63f1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f63f1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f63f1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f63f1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f63f1-110">Cambia l'orientamento di una forma.</span><span class="sxs-lookup"><span data-stu-id="f63f1-110">Switches the orientation of a shape.</span></span> <span data-ttu-id="f63f1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f63f1-111">Read/write.</span></span> <span data-ttu-id="f63f1-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="f63f1-112">**String**.</span></span>

<span data-ttu-id="f63f1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="f63f1-113">**Applies To**</span></span>

[<span data-ttu-id="f63f1-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="f63f1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f63f1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="f63f1-115">**Tag Syntax**</span></span>

<span data-ttu-id="f63f1-116"><v: *elemento* Style = "Flip: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f63f1-116"><v: *element* style="flip: *expression* "></span></span>

<span data-ttu-id="f63f1-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="f63f1-117">**Script Syntax**</span></span>

<span data-ttu-id="f63f1-118">*element* . Style. Flip = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="f63f1-118">*element* .style.flip="*expression*"</span></span>

<span data-ttu-id="f63f1-119">*espressione* = *element*. Style. Flip</span><span class="sxs-lookup"><span data-stu-id="f63f1-119">*expression*=*element*.style.flip</span></span>

<span data-ttu-id="f63f1-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="f63f1-120">**Remarks**</span></span>

<span data-ttu-id="f63f1-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="f63f1-121">Values include:</span></span>



| <span data-ttu-id="f63f1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f63f1-122">Value</span></span> | <span data-ttu-id="f63f1-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f63f1-123">Description</span></span>                                           |
|-------|-------------------------------------------------------|
| <span data-ttu-id="f63f1-124">x</span><span class="sxs-lookup"><span data-stu-id="f63f1-124">x</span></span>     | <span data-ttu-id="f63f1-125">Capovolge lungo l'asse y, invertendo le coordinate *x*.</span><span class="sxs-lookup"><span data-stu-id="f63f1-125">Flip along the y-axis, reversing the *x*-coordinates.</span></span> |
| <span data-ttu-id="f63f1-126">y</span><span class="sxs-lookup"><span data-stu-id="f63f1-126">y</span></span>     | <span data-ttu-id="f63f1-127">Capovolge lungo l'asse *x*, invertendo le coordinate y.</span><span class="sxs-lookup"><span data-stu-id="f63f1-127">Flip along the *x*-axis, reversing the y-coordinates.</span></span> |
| <span data-ttu-id="f63f1-128">xy</span><span class="sxs-lookup"><span data-stu-id="f63f1-128">xy</span></span>    | <span data-ttu-id="f63f1-129">Capovolgere gli assi y e *x*.</span><span class="sxs-lookup"><span data-stu-id="f63f1-129">Flip along both the y- and *x*-axis.</span></span>                  |
| <span data-ttu-id="f63f1-130">YX</span><span class="sxs-lookup"><span data-stu-id="f63f1-130">yx</span></span>    | <span data-ttu-id="f63f1-131">Capovolgere gli assi *x* e *y*.</span><span class="sxs-lookup"><span data-stu-id="f63f1-131">Flip along both the *x*- and *y*-axis.</span></span>                |



 

<span data-ttu-id="f63f1-132">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="f63f1-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="f63f1-133">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="f63f1-133">**See Also**</span></span>

[<span data-ttu-id="f63f1-134">VgFlipOrientation</span><span class="sxs-lookup"><span data-stu-id="f63f1-134">VgFlipOrientation</span></span>](msdn-online-vector-markup-language-object-model-reference.md)

<span data-ttu-id="f63f1-135">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="f63f1-135">**Example**</span></span>

<span data-ttu-id="f63f1-136">La forma viene capovolta lungo l'asse *y* invertendo le coordinate *x* .</span><span class="sxs-lookup"><span data-stu-id="f63f1-136">The shape is flipped along the *y* -axis by reversing the *x* -coordinates.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



<span data-ttu-id="f63f1-137">[Esempio di attributo Flip](/previous-versions/bb229670(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f63f1-137">[Flip Attribute Example](/previous-versions/bb229670(v=vs.85)).</span></span> <span data-ttu-id="f63f1-138">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="f63f1-138">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 