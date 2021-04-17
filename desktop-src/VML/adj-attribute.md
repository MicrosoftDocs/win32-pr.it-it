---
title: ADJ (attributo)
description: ADJ (attributo)
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299983"
---
# <a name="adj-attribute"></a><span data-ttu-id="d89b1-103">ADJ (attributo)</span><span class="sxs-lookup"><span data-stu-id="d89b1-103">Adj Attribute</span></span>

<span data-ttu-id="d89b1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d89b1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d89b1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d89b1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d89b1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d89b1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d89b1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d89b1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d89b1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d89b1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d89b1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d89b1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d89b1-110">Specifica un valore di regolazione utilizzato per definire i valori per una formula.</span><span class="sxs-lookup"><span data-stu-id="d89b1-110">Specifies an adjustment value used to define values for a formula.</span></span> <span data-ttu-id="d89b1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d89b1-111">Read/write.</span></span> <span data-ttu-id="d89b1-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="d89b1-112">**String**.</span></span>

<span data-ttu-id="d89b1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d89b1-113">**Applies To**</span></span>

[<span data-ttu-id="d89b1-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="d89b1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d89b1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d89b1-115">**Tag Syntax**</span></span>

<span data-ttu-id="d89b1-116"><v: *element* ADJ = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d89b1-116"><v: *element* adj=" *expression* "></span></span>

<span data-ttu-id="d89b1-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d89b1-117">**Script Syntax**</span></span>

<span data-ttu-id="d89b1-118">*element* . ADJ = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d89b1-118">*element* .adj="*expression*"</span></span>

<span data-ttu-id="d89b1-119">*espressione* = *elemento*. ADJ</span><span class="sxs-lookup"><span data-stu-id="d89b1-119">*expression*=*element*.adj</span></span>

<span data-ttu-id="d89b1-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d89b1-120">**Remarks**</span></span>

<span data-ttu-id="d89b1-121">**ADJ** viene usato per fornire punti regolabili per una formula.</span><span class="sxs-lookup"><span data-stu-id="d89b1-121">**Adj** is used to provide adjustable points for a formula.</span></span> <span data-ttu-id="d89b1-122">Se usato nei tag, **ADJ** è una stringa delimitata da virgole con un massimo di 8 valori.</span><span class="sxs-lookup"><span data-stu-id="d89b1-122">If used in tags, **Adj** is a comma-delimited string of up to 8 values.</span></span> <span data-ttu-id="d89b1-123">Alcuni valori possono essere omessi.</span><span class="sxs-lookup"><span data-stu-id="d89b1-123">Some values may be omitted.</span></span> <span data-ttu-id="d89b1-124">Ad esempio, "0, 1, 2,, 4, 5,, 7" è una stringa valida, ma il quarto e il settimo elemento non contengono valori (gli elementi vengono conteggiati a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="d89b1-124">For example, "0,1,2,,4,5,,7" would be a valid string but the fourth and seventh items would not have values (items are counted starting from 0).</span></span>

<span data-ttu-id="d89b1-125">Per gli script, **ADJ** usa il tipo di dati [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="d89b1-125">For scripting, **Adj** uses the [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) data type.</span></span>

<span data-ttu-id="d89b1-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="d89b1-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="d89b1-127">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="d89b1-127">**See Also**</span></span>

[<span data-ttu-id="d89b1-128">Formula</span><span class="sxs-lookup"><span data-stu-id="d89b1-128">Formula</span></span>](msdn-online-vml-formulas-element.md)

<span data-ttu-id="d89b1-129">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d89b1-129">**Example**</span></span>

<span data-ttu-id="d89b1-130">Un quadrato semplice viene creato con le regolazioni.</span><span class="sxs-lookup"><span data-stu-id="d89b1-130">A simple square is created with adjustments.</span></span> <span data-ttu-id="d89b1-131">Viene creata prima di tutto la stringa **ADJ** per definire otto valori di regolazione.</span><span class="sxs-lookup"><span data-stu-id="d89b1-131">First the **Adj** string is created to define eight adjustment values.</span></span> <span data-ttu-id="d89b1-132">Quindi, a ogni valore di regolazione viene fatto riferimento da una delle otto formule, con ogni valore di regolazione precedute da un simbolo di cancelletto ( \# ).</span><span class="sxs-lookup"><span data-stu-id="d89b1-132">Then each adjustment value is referenced by one of the eight formulas, with each adjustment value preceeded by a number sign (\#) symbol.</span></span> <span data-ttu-id="d89b1-133">Infine, un percorso è definito da una stringa che fa riferimento alle formule, con ogni formula precedute dal simbolo "chiocciola" (@).</span><span class="sxs-lookup"><span data-stu-id="d89b1-133">Finally a path is defined by a string that references the formulas, with each formula preceeded by the "at" sign (@) symbol.</span></span>


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



<span data-ttu-id="d89b1-134">[Esempio di attributo ADJ](/previous-versions/bb229662(v=vs.85)) (richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="d89b1-134">[Adj Attribute Example](/previous-versions/bb229662(v=vs.85)) (Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 