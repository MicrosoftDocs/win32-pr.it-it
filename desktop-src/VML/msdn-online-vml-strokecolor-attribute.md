---
title: Attributo StrokeColor di la
description: Attributo StrokeColor di la
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046904"
---
# <a name="vml-strokecolor-attribute"></a><span data-ttu-id="5991c-103">Attributo StrokeColor di la</span><span class="sxs-lookup"><span data-stu-id="5991c-103">VML StrokeColor Attribute</span></span>

<span data-ttu-id="5991c-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5991c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5991c-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="5991c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5991c-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="5991c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5991c-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="5991c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5991c-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5991c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5991c-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5991c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5991c-110">Definisce il colore del pennello che traccia il percorso di una forma.</span><span class="sxs-lookup"><span data-stu-id="5991c-110">Defines the brush color that strokes the path of a shape.</span></span> <span data-ttu-id="5991c-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5991c-111">Read/write.</span></span> <span data-ttu-id="5991c-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="5991c-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span>

<span data-ttu-id="5991c-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="5991c-113">**Applies To**</span></span>

[<span data-ttu-id="5991c-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="5991c-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="5991c-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="5991c-115">**Tag Syntax**</span></span>

<span data-ttu-id="5991c-116"><v: *element* strokecolor = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5991c-116"><v: *element* strokecolor=" *expression* "></span></span>

<span data-ttu-id="5991c-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="5991c-117">**Script Syntax**</span></span>

<span data-ttu-id="5991c-118">*element* . strokecolor = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="5991c-118">*element* .strokecolor="*expression*"</span></span>

<span data-ttu-id="5991c-119">*espressione* = *elemento*. StrokeColor</span><span class="sxs-lookup"><span data-stu-id="5991c-119">*expression*=*element*.strokecolor</span></span>

<span data-ttu-id="5991c-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="5991c-120">**Remarks**</span></span>

<span data-ttu-id="5991c-121">Il valore viene duplicato dall'attributo **color** dell'elemento [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5991c-121">The value is duplicated from the **Color** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="5991c-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="5991c-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="5991c-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="5991c-123">**Example**</span></span>

<span data-ttu-id="5991c-124">Il colore del tratto del rettangolo è rosso.</span><span class="sxs-lookup"><span data-stu-id="5991c-124">The color of the stroke of the rectangle is red.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="5991c-125">[Esempio di attributo StrokeColor](/previous-versions/bb264093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5991c-125">[StrokeColor Attribute Example](/previous-versions/bb264093(v=vs.85)).</span></span> <span data-ttu-id="5991c-126">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="5991c-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 