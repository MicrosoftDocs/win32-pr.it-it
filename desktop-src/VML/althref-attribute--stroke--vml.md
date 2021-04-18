---
title: Attributo AltHRef (Stroke) (la)
description: Attributo AltHRef (Stroke) (la)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300280"
---
# <a name="althref-attribute-strokevml"></a><span data-ttu-id="b1651-103">Attributo AltHRef (Stroke) (la)</span><span class="sxs-lookup"><span data-stu-id="b1651-103">AltHRef Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="b1651-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b1651-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b1651-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="b1651-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b1651-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="b1651-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b1651-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="b1651-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b1651-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b1651-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b1651-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b1651-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b1651-110">Specifica un riferimento alternativo per un'immagine.</span><span class="sxs-lookup"><span data-stu-id="b1651-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="b1651-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b1651-111">Read/write.</span></span> <span data-ttu-id="b1651-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="b1651-112">**String**.</span></span>

<span data-ttu-id="b1651-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="b1651-113">**Applies To**</span></span>

[<span data-ttu-id="b1651-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="b1651-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="b1651-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="b1651-115">**Tag Syntax**</span></span>

<span data-ttu-id="b1651-116"><v: *element* o:althref = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="b1651-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="b1651-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="b1651-117">**Script Syntax**</span></span>

<span data-ttu-id="b1651-118">*element* . althref = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="b1651-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="b1651-119">*espressione* = *elemento*. althref</span><span class="sxs-lookup"><span data-stu-id="b1651-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="b1651-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="b1651-120">**Remarks**</span></span>

<span data-ttu-id="b1651-121">Supporta la conservazione dei dati PICT tramite Roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="b1651-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="b1651-122">Nella scrittura HTML la rappresentazione alternativa, ovvero i dati PICT originali se il file proviene da Macintosh, viene salvata.</span><span class="sxs-lookup"><span data-stu-id="b1651-122">On HTML write, the alternate representation (i.e., the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="b1651-123">In HTML Read, **AltHRef** è favorito tramite **src**.</span><span class="sxs-lookup"><span data-stu-id="b1651-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="b1651-124">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="b1651-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="b1651-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="b1651-125">**Example**</span></span>

<span data-ttu-id="b1651-126">Il tratto della forma ha un **AltHRef** che punta a un file denominato myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="b1651-126">The stroke of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 