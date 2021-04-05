---
title: Attributo Rotation (Shape) (la)
description: Attributo Rotation (Shape) (la)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047310"
---
# <a name="rotation-attribute-shapevml"></a><span data-ttu-id="bb2b8-103">Attributo Rotation (Shape) (la)</span><span class="sxs-lookup"><span data-stu-id="bb2b8-103">Rotation Attribute (Shape)(VML)</span></span>

<span data-ttu-id="bb2b8-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bb2b8-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bb2b8-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bb2b8-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bb2b8-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bb2b8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bb2b8-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bb2b8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bb2b8-110">Definisce l'angolo di rotazione di una forma.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-110">Defines the angle that a shape is rotated.</span></span> <span data-ttu-id="bb2b8-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-111">Read/write.</span></span> <span data-ttu-id="bb2b8-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="bb2b8-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span>

<span data-ttu-id="bb2b8-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="bb2b8-113">**Applies To**</span></span>

[<span data-ttu-id="bb2b8-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="bb2b8-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="bb2b8-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="bb2b8-115">**Tag Syntax**</span></span>

<span data-ttu-id="bb2b8-116"><v: *elemento* Style = "Rotation: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="bb2b8-116"><v: *element* style="rotation: *expression* "></span></span>

<span data-ttu-id="bb2b8-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="bb2b8-117">**Script Syntax**</span></span>

<span data-ttu-id="bb2b8-118">*element* . Rotation = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="bb2b8-118">*element* .rotation="*expression*"</span></span>

<span data-ttu-id="bb2b8-119">*espressione* = *elemento*. Rotation</span><span class="sxs-lookup"><span data-stu-id="bb2b8-119">*expression*=*element*.rotation</span></span>

<span data-ttu-id="bb2b8-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="bb2b8-120">**Remarks**</span></span>

<span data-ttu-id="bb2b8-121">Il valore in gradi può essere positivo o negativo e i valori maggiori di 360 vengono modulati in un cerchio di 360 gradi.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-121">The value in degrees can be positive or negative, and values greater than 360 are modularized to a 360-degree circle.</span></span> <span data-ttu-id="bb2b8-122">Gli angoli positivi sono in senso orario.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-122">Positive angles are clockwise.</span></span> <span data-ttu-id="bb2b8-123">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-123">The default value is 0.</span></span>

<span data-ttu-id="bb2b8-124">Si noti che la forma viene riposizionata dopo la rotazione in modo da riflettere le nuove coordinate del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-124">Note that the shape is repositioned after the rotation to reflect the new bounding box coordinates.</span></span>

<span data-ttu-id="bb2b8-125">Si noti inoltre che, per gli script, l'attributo di **stile** non viene utilizzato e che la **rotazione** viene considerata come un attributo diretto della forma.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-125">Also note that for scripting, the **style** attribute is not used and that **Rotation** is treated as a direct attribute of the shape.</span></span>

<span data-ttu-id="bb2b8-126">L'attributo **Rotation** è simile all'attributo standard di **rotazione** HTML per gli stili.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-126">The **Rotation** attribute is similar to the standard HTML **Rotation** attribute for styles.</span></span>

<span data-ttu-id="bb2b8-127">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="bb2b8-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="bb2b8-128">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="bb2b8-128">**See Also**</span></span>

<span data-ttu-id="bb2b8-129">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="bb2b8-129">**Example**</span></span>

<span data-ttu-id="bb2b8-130">Il rettangolo verrà inclinato di 45 gradi.</span><span class="sxs-lookup"><span data-stu-id="bb2b8-130">The rectangle will be tilted 45 degrees.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



<span data-ttu-id="bb2b8-131">[Esempio di attributo Rotation](/previous-versions/bb264091(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb2b8-131">[Rotation Attribute Example](/previous-versions/bb264091(v=vs.85)).</span></span> <span data-ttu-id="bb2b8-132">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="bb2b8-132">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 