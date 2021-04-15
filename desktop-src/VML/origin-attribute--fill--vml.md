---
title: Attributo Origin (Fill) (la)
description: Attributo Origin (Fill) (la)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399677"
---
# <a name="origin-attribute-fillvml"></a><span data-ttu-id="1494e-103">Attributo Origin (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="1494e-103">Origin Attribute (Fill)(VML)</span></span>

<span data-ttu-id="1494e-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1494e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1494e-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="1494e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1494e-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="1494e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1494e-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="1494e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1494e-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1494e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1494e-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1494e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1494e-110">Definisce il centro di un'immagine di riempimento.</span><span class="sxs-lookup"><span data-stu-id="1494e-110">Defines the center of a fill image.</span></span> <span data-ttu-id="1494e-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1494e-111">Read/write.</span></span> <span data-ttu-id="1494e-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="1494e-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="1494e-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="1494e-113">**Applies To**</span></span>

[<span data-ttu-id="1494e-114">Fill</span><span class="sxs-lookup"><span data-stu-id="1494e-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="1494e-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="1494e-115">**Tag Syntax**</span></span>

<span data-ttu-id="1494e-116"><v: *element* Origin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="1494e-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="1494e-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="1494e-117">**Script Syntax**</span></span>

<span data-ttu-id="1494e-118">*element* . Origin = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="1494e-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="1494e-119">*espressione* = *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="1494e-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="1494e-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="1494e-120">**Remarks**</span></span>

<span data-ttu-id="1494e-121">Specifica un punto relativo all'angolo superiore sinistro dell'immagine; questo punto viene trattato come origine dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1494e-121">Specifies a point relative to the upper left corner of the image; this point is treated as the origin of the image.</span></span> <span data-ttu-id="1494e-122">Il valore predefinito è il centro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1494e-122">Default is the center of the image.</span></span> <span data-ttu-id="1494e-123">Il vettore è una frazione della larghezza e dell'altezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1494e-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="1494e-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="1494e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="1494e-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="1494e-125">**Example**</span></span>

<span data-ttu-id="1494e-126">L'immagine del riempimento viene spostata verso sinistra fino a un punto 50% della larghezza della forma.</span><span class="sxs-lookup"><span data-stu-id="1494e-126">The image of the fill is shifted left to a point 50% of the width of the shape .</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 