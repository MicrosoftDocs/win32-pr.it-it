---
title: Attributo di visibilità la
description: Attributo di visibilità la
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299954"
---
# <a name="vml-visibility-attribute"></a><span data-ttu-id="b3d2a-103">Attributo di visibilità la</span><span class="sxs-lookup"><span data-stu-id="b3d2a-103">VML Visibility Attribute</span></span>

<span data-ttu-id="b3d2a-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b3d2a-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b3d2a-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b3d2a-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b3d2a-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b3d2a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b3d2a-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b3d2a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b3d2a-110">Determina se una forma viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-110">Determines whether a shape is displayed.</span></span> <span data-ttu-id="b3d2a-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-111">Read/write.</span></span> <span data-ttu-id="b3d2a-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-112">**String**.</span></span>

<span data-ttu-id="b3d2a-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="b3d2a-113">**Applies To**</span></span>

[<span data-ttu-id="b3d2a-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="b3d2a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b3d2a-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="b3d2a-115">**Tag Syntax**</span></span>

<span data-ttu-id="b3d2a-116"><v: *elemento* Style = "Visibility: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="b3d2a-116"><v: *element* style="visibility: *expression* "></span></span>

<span data-ttu-id="b3d2a-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="b3d2a-117">**Script Syntax**</span></span>

<span data-ttu-id="b3d2a-118">*element* . Style. Visibility = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="b3d2a-118">*element* .style.visibility="*expression*"</span></span>

<span data-ttu-id="b3d2a-119">*espressione* = *element*. Style. Visibility</span><span class="sxs-lookup"><span data-stu-id="b3d2a-119">*expression*=*element*.style.visibility</span></span>

<span data-ttu-id="b3d2a-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="b3d2a-120">**Remarks**</span></span>

<span data-ttu-id="b3d2a-121">L'attributo **visibility** è simile all'attributo di **visibilità** HTML standard per gli stili.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-121">The **Visibility** attribute is similar to the standard HTML **Visibility** attribute for styles.</span></span>

<span data-ttu-id="b3d2a-122">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="b3d2a-122">Values include:</span></span>



| <span data-ttu-id="b3d2a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b3d2a-123">Value</span></span>    | <span data-ttu-id="b3d2a-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3d2a-124">Description</span></span>                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d2a-125">visible</span><span class="sxs-lookup"><span data-stu-id="b3d2a-125">visible</span></span>  | <span data-ttu-id="b3d2a-126">La forma è visibile.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-126">The shape is visible.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="b3d2a-127">hidden</span><span class="sxs-lookup"><span data-stu-id="b3d2a-127">hidden</span></span>   | <span data-ttu-id="b3d2a-128">La forma non è visibile, ma fa ancora parte del flusso degli oggetti nel browser.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-128">The shape is not visible, but is still part of the flow of the objects in the browser.</span></span> <span data-ttu-id="b3d2a-129">Gli eventi del mouse non vengono elaborati.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-129">Mouse events are not processed.</span></span>                                                                  |
| <span data-ttu-id="b3d2a-130">inherit</span><span class="sxs-lookup"><span data-stu-id="b3d2a-130">inherit</span></span>  | <span data-ttu-id="b3d2a-131">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-131">Default.</span></span> <span data-ttu-id="b3d2a-132">Lo stato di visibilità viene ereditato dall'elemento padre della forma.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-132">The visibility state is inherited from the parent of the shape.</span></span> <span data-ttu-id="b3d2a-133">Le applicazioni Microsoft Office utilizzano solo **ereditarietà** e **Hidden**; tutti gli altri valori vengono mappati per **ereditare**.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-133">Microsoft Office applications only use **inherit** and **hidden**; any other values are mapped to **inherit**.</span></span> |
| <span data-ttu-id="b3d2a-134">comprimere</span><span class="sxs-lookup"><span data-stu-id="b3d2a-134">collapse</span></span> | <span data-ttu-id="b3d2a-135">Utilizzato per le applicazioni di modifica grafica che possono comprimere gruppi di forme; ad esempio, i delineatori.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-135">Used for graphical editing applications that can collapse groups of shapes; for example, outliners.</span></span>                                                                                     |



 

<span data-ttu-id="b3d2a-136">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="b3d2a-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="b3d2a-137">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="b3d2a-137">**Example**</span></span>

<span data-ttu-id="b3d2a-138">Il codice seguente crea una forma, ma la rende nascosta.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-138">The following code creates a shape but makes it hidden.</span></span> <span data-ttu-id="b3d2a-139">Il flusso di altri oggetti nel documento verrà aggirato, lasciando uno spazio delle stesse dimensioni della forma.</span><span class="sxs-lookup"><span data-stu-id="b3d2a-139">Other objects in the document will flow around it, leaving a space the same size as the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



<span data-ttu-id="b3d2a-140">[Esempio di attributo Visibility](/previous-versions/bb264100(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b3d2a-140">[Visibility Attribute Example](/previous-versions/bb264100(v=vs.85)).</span></span> <span data-ttu-id="b3d2a-141">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="b3d2a-141">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 