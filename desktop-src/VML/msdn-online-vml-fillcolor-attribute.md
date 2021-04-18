---
title: Attributo FillColor di la
description: Attributo FillColor di la
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300401"
---
# <a name="vml-fillcolor-attribute"></a><span data-ttu-id="ca551-103">Attributo FillColor di la</span><span class="sxs-lookup"><span data-stu-id="ca551-103">VML FillColor Attribute</span></span>

<span data-ttu-id="ca551-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ca551-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ca551-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ca551-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ca551-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ca551-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ca551-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ca551-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ca551-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ca551-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ca551-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ca551-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ca551-110">Definisce il colore del pennello che riempie il percorso chiuso di una forma.</span><span class="sxs-lookup"><span data-stu-id="ca551-110">Defines the brush color that fills the closed path of a shape.</span></span> <span data-ttu-id="ca551-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ca551-111">Read/write.</span></span> <span data-ttu-id="ca551-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="ca551-112">[IVgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="ca551-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ca551-113">**Applies To**</span></span>

[<span data-ttu-id="ca551-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="ca551-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ca551-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ca551-115">**Tag Syntax**</span></span>

<span data-ttu-id="ca551-116"><v: *element* FillColor = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ca551-116"><v: *element* fillcolor=" *expression* "></span></span>

<span data-ttu-id="ca551-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="ca551-117">**Script Syntax**</span></span>

<span data-ttu-id="ca551-118">*element* . FillColor = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="ca551-118">*element* .fillcolor="*expression*"</span></span>

<span data-ttu-id="ca551-119">*espressione* = *elemento*. FillColor</span><span class="sxs-lookup"><span data-stu-id="ca551-119">*expression*=*element*.fillcolor</span></span>

<span data-ttu-id="ca551-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ca551-120">**Remarks**</span></span>

<span data-ttu-id="ca551-121">Il valore **FillColor** viene duplicato dall'attributo **color** dell'elemento **Fill** .</span><span class="sxs-lookup"><span data-stu-id="ca551-121">The **FillColor** value is duplicated from the **Color** attribute of the **Fill** element.</span></span>

<span data-ttu-id="ca551-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="ca551-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="ca551-123">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="ca551-123">**See Also**</span></span>

<span data-ttu-id="ca551-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span><span class="sxs-lookup"><span data-stu-id="ca551-124">[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)</span></span>

<span data-ttu-id="ca551-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="ca551-125">**Example**</span></span>

<span data-ttu-id="ca551-126">Il colore di riempimento del rettangolo è rosso.</span><span class="sxs-lookup"><span data-stu-id="ca551-126">The fill color of the rectangle is red.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="ca551-127">[Esempio di attributo FillColor](/previous-versions/bb229668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ca551-127">[FillColor Attribute Example](/previous-versions/bb229668(v=vs.85)).</span></span> <span data-ttu-id="ca551-128">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="ca551-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 