---
title: Attributo Type (Fill) (la)
description: Attributo Type (Fill) (la)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728807"
---
# <a name="type-attribute-fillvml"></a><span data-ttu-id="73468-103">Attributo Type (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="73468-103">Type Attribute (Fill)(VML)</span></span>

<span data-ttu-id="73468-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="73468-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="73468-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="73468-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="73468-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="73468-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="73468-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="73468-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="73468-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="73468-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="73468-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="73468-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="73468-110">Determina il tipo di riempimento.</span><span class="sxs-lookup"><span data-stu-id="73468-110">Determines the type of fill.</span></span> <span data-ttu-id="73468-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="73468-111">Read/write.</span></span> <span data-ttu-id="73468-112">**VgFillType**.</span><span class="sxs-lookup"><span data-stu-id="73468-112">**VgFillType**.</span></span>

<span data-ttu-id="73468-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="73468-113">**Applies To**</span></span>

[<span data-ttu-id="73468-114">Fill</span><span class="sxs-lookup"><span data-stu-id="73468-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="73468-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="73468-115">**Tag Syntax**</span></span>

<span data-ttu-id="73468-116"><v: tipo di *elemento* = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="73468-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="73468-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="73468-117">**Script Syntax**</span></span>

<span data-ttu-id="73468-118">*element* . Type = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="73468-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="73468-119">*espressione* = *element*. Type</span><span class="sxs-lookup"><span data-stu-id="73468-119">*expression*=*element*.type</span></span>

<span data-ttu-id="73468-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="73468-120">**Remarks**</span></span>

<span data-ttu-id="73468-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="73468-121">Values include:</span></span>



| <span data-ttu-id="73468-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="73468-122">Type</span></span>           | <span data-ttu-id="73468-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73468-123">Description</span></span>                                                             |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="73468-124">solido</span><span class="sxs-lookup"><span data-stu-id="73468-124">solid</span></span>          | <span data-ttu-id="73468-125">Il modello di riempimento è a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="73468-125">The fill pattern is solid.</span></span> <span data-ttu-id="73468-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="73468-126">Default.</span></span>                                     |
| <span data-ttu-id="73468-127">gradiente</span><span class="sxs-lookup"><span data-stu-id="73468-127">gradient</span></span>       | <span data-ttu-id="73468-128">I colori di riempimento vengono combinati in una sfumatura lineare, dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="73468-128">The fill colors blend together in a linear gradient from bottom to top.</span></span> |
| <span data-ttu-id="73468-129">gradientradial</span><span class="sxs-lookup"><span data-stu-id="73468-129">gradientradial</span></span> | <span data-ttu-id="73468-130">I colori di riempimento vengono combinati in una sfumatura radiale.</span><span class="sxs-lookup"><span data-stu-id="73468-130">The fill colors blend together in a radial gradient.</span></span>                    |
| <span data-ttu-id="73468-131">tile</span><span class="sxs-lookup"><span data-stu-id="73468-131">tile</span></span>           | <span data-ttu-id="73468-132">L'immagine di riempimento è affiancata.</span><span class="sxs-lookup"><span data-stu-id="73468-132">The fill image is tiled.</span></span>                                                |
| <span data-ttu-id="73468-133">pattern</span><span class="sxs-lookup"><span data-stu-id="73468-133">pattern</span></span>        | <span data-ttu-id="73468-134">L'immagine viene usata per creare un modello usando i colori di riempimento.</span><span class="sxs-lookup"><span data-stu-id="73468-134">The image is used to create a pattern using the fill colors.</span></span>            |
| <span data-ttu-id="73468-135">frame</span><span class="sxs-lookup"><span data-stu-id="73468-135">frame</span></span>          | <span data-ttu-id="73468-136">L'immagine viene adattata per riempire la forma.</span><span class="sxs-lookup"><span data-stu-id="73468-136">The image is stretched to fill the shape.</span></span>                               |



 

<span data-ttu-id="73468-137">**Attributo standard la**</span><span class="sxs-lookup"><span data-stu-id="73468-137">**VML Standard Attribute**</span></span>

<span data-ttu-id="73468-138">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="73468-138">**Example**</span></span>

<span data-ttu-id="73468-139">Viene creato un riempimento in primo piano rosso e sfondo blu usando il modello dell'immagine myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="73468-139">A red foreground and blue background fill is created using the pattern of the image myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 