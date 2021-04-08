---
title: Attributo StrokeWeight di la
description: Attributo StrokeWeight di la
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728071"
---
# <a name="vml-strokeweight-attribute"></a><span data-ttu-id="58994-103">Attributo StrokeWeight di la</span><span class="sxs-lookup"><span data-stu-id="58994-103">VML StrokeWeight Attribute</span></span>

<span data-ttu-id="58994-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="58994-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="58994-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="58994-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="58994-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="58994-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="58994-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="58994-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="58994-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="58994-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="58994-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="58994-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="58994-110">Definisce lo spessore del pennello che accarezza il percorso di una forma.</span><span class="sxs-lookup"><span data-stu-id="58994-110">Defines the brush thickness that strokes the path of a shape.</span></span> <span data-ttu-id="58994-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="58994-111">Read/write.</span></span> <span data-ttu-id="58994-112">**VGLength**.</span><span class="sxs-lookup"><span data-stu-id="58994-112">**VGLength**.</span></span>

<span data-ttu-id="58994-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="58994-113">**Applies To**</span></span>

[<span data-ttu-id="58994-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="58994-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="58994-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="58994-115">**Tag Syntax**</span></span>

<span data-ttu-id="58994-116"><v: *element* StrokeWeight = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="58994-116"><v: *element* strokeweight=" *expression* "></span></span>

<span data-ttu-id="58994-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="58994-117">**Script Syntax**</span></span>

<span data-ttu-id="58994-118">*element* . StrokeWeight = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="58994-118">*element* .strokeweight="*expression*"</span></span>

<span data-ttu-id="58994-119">*espressione* = *elemento*. StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="58994-119">*expression*=*element*.strokeweight</span></span>

<span data-ttu-id="58994-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="58994-120">**Remarks**</span></span>

<span data-ttu-id="58994-121">Il valore viene duplicato dall'attributo **Weight** dell'elemento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="58994-121">The value is duplicated from the **Weight** attribute of the **Stroke** element.</span></span> <span data-ttu-id="58994-122">Se viene specificato un numero, ma non vengono aggiunte unità, l'unità di misura predefinita è Emu.</span><span class="sxs-lookup"><span data-stu-id="58994-122">If a number is specified, but no units are added, the default unit of measurement is the Emu.</span></span> <span data-ttu-id="58994-123">Se non viene specificato alcun valore, il valore predefinito è 1 pixel (1px).</span><span class="sxs-lookup"><span data-stu-id="58994-123">If no value is specified, the default is 1 pixel (1px).</span></span>

<span data-ttu-id="58994-124">Per gli script, tuttavia, l'unità di misura predefinita è in punti.</span><span class="sxs-lookup"><span data-stu-id="58994-124">For scripting, however, the default unit of measurement is in points.</span></span>

<span data-ttu-id="58994-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="58994-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="58994-126">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="58994-126">**See Also**</span></span>

<span data-ttu-id="58994-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [unità](msdn-online-vml-units.md)</span><span class="sxs-lookup"><span data-stu-id="58994-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span></span>

<span data-ttu-id="58994-128">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="58994-128">**Example**</span></span>

<span data-ttu-id="58994-129">Lo spessore del tratto della forma è 1 punto.</span><span class="sxs-lookup"><span data-stu-id="58994-129">The stroke weight of the shape is 1 point.</span></span>


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="58994-130">[Esempio di attributo StrokeWeight](/previous-versions/bb264095(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58994-130">[StrokeWeight Attribute Example](/previous-versions/bb264095(v=vs.85)).</span></span> <span data-ttu-id="58994-131">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="58994-131">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 