---
title: Attributo elemento FillType di la
description: Attributo elemento FillType di la
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963434"
---
# <a name="vml-filltype-attribute"></a><span data-ttu-id="0cbf7-103">Attributo elemento FillType di la</span><span class="sxs-lookup"><span data-stu-id="0cbf7-103">VML FillType Attribute</span></span>

<span data-ttu-id="0cbf7-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0cbf7-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0cbf7-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0cbf7-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0cbf7-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0cbf7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0cbf7-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0cbf7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0cbf7-110">Definisce il tipo di riempimento utilizzato per lo sfondo di un tratto.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-110">Defines the type of fill used for the background of a stroke.</span></span> <span data-ttu-id="0cbf7-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-111">Read/write.</span></span> <span data-ttu-id="0cbf7-112">**VgFillType**.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-112">**VgFillType**.</span></span>

<span data-ttu-id="0cbf7-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="0cbf7-113">**Applies To**</span></span>

[<span data-ttu-id="0cbf7-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="0cbf7-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="0cbf7-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="0cbf7-115">**Tag Syntax**</span></span>

<span data-ttu-id="0cbf7-116"><v: *element* elemento FillType = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0cbf7-116"><v: *element* filltype=" *expression* "></span></span>

<span data-ttu-id="0cbf7-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="0cbf7-117">**Script Syntax**</span></span>

<span data-ttu-id="0cbf7-118">*element* . elemento FillType = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="0cbf7-118">*element* .filltype="*expression*"</span></span>

<span data-ttu-id="0cbf7-119">*espressione* = *elemento*. elemento FillType</span><span class="sxs-lookup"><span data-stu-id="0cbf7-119">*expression*=*element*.filltype</span></span>

<span data-ttu-id="0cbf7-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="0cbf7-120">**Remarks**</span></span>

<span data-ttu-id="0cbf7-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="0cbf7-121">Values include:</span></span>



| <span data-ttu-id="0cbf7-122">DashStyle</span><span class="sxs-lookup"><span data-stu-id="0cbf7-122">DashStyle</span></span> | <span data-ttu-id="0cbf7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cbf7-123">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="0cbf7-124">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="0cbf7-124">Solid</span></span>     | <span data-ttu-id="0cbf7-125">Il modello di riempimento è a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-125">The fill pattern is solid.</span></span> <span data-ttu-id="0cbf7-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-126">Default value.</span></span>      |
| <span data-ttu-id="0cbf7-127">Tile</span><span class="sxs-lookup"><span data-stu-id="0cbf7-127">Tile</span></span>      | <span data-ttu-id="0cbf7-128">L'immagine di riempimento è affiancata.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-128">The fill image is tiled.</span></span>                       |
| <span data-ttu-id="0cbf7-129">Modello</span><span class="sxs-lookup"><span data-stu-id="0cbf7-129">Pattern</span></span>   | <span data-ttu-id="0cbf7-130">L'immagine di riempimento viene estesa per formare un modello.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-130">The fill image is stretched to form a pattern.</span></span> |
| <span data-ttu-id="0cbf7-131">Frame</span><span class="sxs-lookup"><span data-stu-id="0cbf7-131">Frame</span></span>     | <span data-ttu-id="0cbf7-132">L'immagine di riempimento diventa un bordo per la forma.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-132">The fill image becomes a border for the shape.</span></span> |



 

<span data-ttu-id="0cbf7-133">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="0cbf7-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="0cbf7-134">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0cbf7-134">**Example**</span></span>

<span data-ttu-id="0cbf7-135">Il tratto della forma ha una trama affiancata creata dall'immagine del cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="0cbf7-135">The stroke of the shape has a tiled texture created from the cylinder.gif image.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 