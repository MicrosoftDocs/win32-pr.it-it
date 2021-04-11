---
title: Attributo tratteggiato la
description: Attributo tratteggiato la
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118383"
---
# <a name="vml-stroked-attribute"></a><span data-ttu-id="78262-103">Attributo tratteggiato la</span><span class="sxs-lookup"><span data-stu-id="78262-103">VML Stroked Attribute</span></span>

<span data-ttu-id="78262-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="78262-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="78262-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="78262-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="78262-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="78262-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="78262-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="78262-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="78262-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="78262-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="78262-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="78262-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="78262-110">Definisce se il percorso verrà tracciato.</span><span class="sxs-lookup"><span data-stu-id="78262-110">Defines whether the path will be stroked.</span></span> <span data-ttu-id="78262-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="78262-111">Read/write.</span></span> <span data-ttu-id="78262-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span><span class="sxs-lookup"><span data-stu-id="78262-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span></span>

<span data-ttu-id="78262-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="78262-113">**Applies To**</span></span>

[<span data-ttu-id="78262-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="78262-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="78262-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="78262-115">**Tag Syntax**</span></span>

<span data-ttu-id="78262-116"><v: *elemento* stroked = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="78262-116"><v: *element* stroked=" *expression* "></span></span>

<span data-ttu-id="78262-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="78262-117">**Script Syntax**</span></span>

<span data-ttu-id="78262-118">*element* . stroked = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="78262-118">*element* .stroked="*expression*"</span></span>

<span data-ttu-id="78262-119">*espressione* = *elemento*. stroked</span><span class="sxs-lookup"><span data-stu-id="78262-119">*expression*=*element*.stroked</span></span>

<span data-ttu-id="78262-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="78262-120">**Remarks**</span></span>

<span data-ttu-id="78262-121">Il valore viene duplicato dall'attributo **on** dell'elemento [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="78262-121">The value is duplicated from the **On** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="78262-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="78262-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="78262-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="78262-123">**Example**</span></span>

<span data-ttu-id="78262-124">Il percorso della forma viene tracciato.</span><span class="sxs-lookup"><span data-stu-id="78262-124">The shape path is stroked.</span></span>


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="78262-125">[Esempio di attributo stroked](/previous-versions/bb264094(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78262-125">[Stroked Attribute Example](/previous-versions/bb264094(v=vs.85)).</span></span> <span data-ttu-id="78262-126">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="78262-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 