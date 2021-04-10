---
title: Attributo size (Fill) (la)
description: Attributo size (Fill) (la)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963146"
---
# <a name="size-attribute-fillvml"></a><span data-ttu-id="0b7b4-103">Attributo size (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="0b7b4-103">Size Attribute (Fill)(VML)</span></span>

<span data-ttu-id="0b7b4-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0b7b4-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0b7b4-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0b7b4-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0b7b4-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0b7b4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0b7b4-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0b7b4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0b7b4-110">Definisce le dimensioni dell'immagine per il riempimento.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-110">Defines the size of the image for the fill.</span></span> <span data-ttu-id="0b7b4-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-111">Read/write.</span></span> <span data-ttu-id="0b7b4-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0b7b4-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="0b7b4-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="0b7b4-113">**Applies To**</span></span>

[<span data-ttu-id="0b7b4-114">Fill</span><span class="sxs-lookup"><span data-stu-id="0b7b4-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="0b7b4-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="0b7b4-115">**Tag Syntax**</span></span>

<span data-ttu-id="0b7b4-116"><v: *element* size = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0b7b4-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="0b7b4-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="0b7b4-117">**Script Syntax**</span></span>

<span data-ttu-id="0b7b4-118">*element* . size = "*Expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="0b7b4-118">*element* .size="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="0b7b4-119">*espressione* = *element*. size</span><span class="sxs-lookup"><span data-stu-id="0b7b4-119">*expression*=*element*.size</span></span>

<span data-ttu-id="0b7b4-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="0b7b4-120">**Remarks**</span></span>

<span data-ttu-id="0b7b4-121">Il valore predefinito corrisponde alla dimensione dell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-121">The default is the size of the original image.</span></span> <span data-ttu-id="0b7b4-122">Dimensioni maggiori di shapewill visualizzano una versione ingrandita ma ritagliata dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-122">Sizes that are larger than the shapewill display a magnified but clipped version of the image.</span></span>

<span data-ttu-id="0b7b4-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="0b7b4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="0b7b4-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0b7b4-124">**Example**</span></span>

<span data-ttu-id="0b7b4-125">Anche se le dimensioni originali dell'immagine sono 50 per 50 punti, l'immagine verrà visualizzata come immagine 10 per 10 al centro della riempita.</span><span class="sxs-lookup"><span data-stu-id="0b7b4-125">Even though the original size of the image is 50-by-50 points, the image will be displayed as a 10-by-10 image in the center of the fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 