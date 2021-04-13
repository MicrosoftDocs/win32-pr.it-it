---
title: Attributo Type (Shadow) (la)
description: Attributo Type (Shadow) (la)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399373"
---
# <a name="type-attribute-shadowvml"></a><span data-ttu-id="cb6e7-103">Attributo Type (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="cb6e7-103">Type Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="cb6e7-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cb6e7-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cb6e7-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cb6e7-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cb6e7-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cb6e7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cb6e7-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cb6e7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cb6e7-110">Specifica il tipo di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-110">Specifies the type of shadow.</span></span> <span data-ttu-id="cb6e7-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-111">Read/write.</span></span> <span data-ttu-id="cb6e7-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-112">**String**.</span></span>

<span data-ttu-id="cb6e7-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="cb6e7-113">**Applies To**</span></span>

[<span data-ttu-id="cb6e7-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="cb6e7-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="cb6e7-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="cb6e7-115">**Tag Syntax**</span></span>

<span data-ttu-id="cb6e7-116"><v: tipo di *elemento* = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="cb6e7-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="cb6e7-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="cb6e7-117">**Script Syntax**</span></span>

<span data-ttu-id="cb6e7-118">*element* . Type = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="cb6e7-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="cb6e7-119">*espressione* = *element*. Type</span><span class="sxs-lookup"><span data-stu-id="cb6e7-119">*expression*=*element*.type</span></span>

<span data-ttu-id="cb6e7-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="cb6e7-120">**Remarks**</span></span>

<span data-ttu-id="cb6e7-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="cb6e7-121">Values include:</span></span>



| <span data-ttu-id="cb6e7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="cb6e7-122">Value</span></span>           | <span data-ttu-id="cb6e7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb6e7-123">Description</span></span>                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6e7-124">single</span><span class="sxs-lookup"><span data-stu-id="cb6e7-124">single</span></span>          | <span data-ttu-id="cb6e7-125">Singola ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-125">Single shadow.</span></span> <span data-ttu-id="cb6e7-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-126">Default.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="cb6e7-127">double</span><span class="sxs-lookup"><span data-stu-id="cb6e7-127">double</span></span>          | <span data-ttu-id="cb6e7-128">Un'ombreggiatura doppia.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-128">A double shadow.</span></span> <span data-ttu-id="cb6e7-129">[Color2](color2-attribute--shadow--vml.md) viene usato per il colore della seconda ombreggiatura e [Offset2](msdn-online-vml-offset2-attribute.md) viene usato per l'offset della seconda ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-129">[Color2](color2-attribute--shadow--vml.md) is used for the color of the second shadow and [Offset2](msdn-online-vml-offset2-attribute.md) is used for the second shadow's offset.</span></span> |
| <span data-ttu-id="cb6e7-130">prospettiva</span><span class="sxs-lookup"><span data-stu-id="cb6e7-130">perspective</span></span>     | <span data-ttu-id="cb6e7-131">Ombreggiatura della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-131">A perspective shadow.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="cb6e7-132">shapeRelative</span><span class="sxs-lookup"><span data-stu-id="cb6e7-132">shapeRelative</span></span>   | <span data-ttu-id="cb6e7-133">L'ombreggiatura viene creata in relazione alla forma.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-133">The shadow is created relative to the shape.</span></span>                                                                                                                                                         |
| <span data-ttu-id="cb6e7-134">drawingRelative</span><span class="sxs-lookup"><span data-stu-id="cb6e7-134">drawingRelative</span></span> | <span data-ttu-id="cb6e7-135">L'ombreggiatura viene creata in relazione al disegno.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-135">The shadow is created relative to the drawing.</span></span>                                                                                                                                                       |
| <span data-ttu-id="cb6e7-136">rilievo</span><span class="sxs-lookup"><span data-stu-id="cb6e7-136">emboss</span></span>          | <span data-ttu-id="cb6e7-137">L'ombreggiatura presenta un aspetto in rilievo.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-137">The shadow has an embossed look.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="cb6e7-138">**Attributo standard la**</span><span class="sxs-lookup"><span data-stu-id="cb6e7-138">**VML Standard Attribute**</span></span>

<span data-ttu-id="cb6e7-139">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="cb6e7-139">**Example**</span></span>

<span data-ttu-id="cb6e7-140">Viene creata una doppia ombreggiatura con la seconda ombreggiatura verde e l'offset 5 punta verso il basso e verso destra.</span><span class="sxs-lookup"><span data-stu-id="cb6e7-140">A double shadow is created with the second shadow green and offset 5 points down and to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 