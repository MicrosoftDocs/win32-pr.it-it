---
title: Attributo AltHRef (Fill) (la)
description: Attributo AltHRef (Fill) (la)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473446"
---
# <a name="althref-attribute-fillvml"></a><span data-ttu-id="23ec8-103">Attributo AltHRef (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="23ec8-103">AltHRef Attribute (Fill)(VML)</span></span>

<span data-ttu-id="23ec8-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="23ec8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="23ec8-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="23ec8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="23ec8-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="23ec8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="23ec8-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="23ec8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="23ec8-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="23ec8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="23ec8-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="23ec8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="23ec8-110">Definisce un riferimento alternativo per un'immagine.</span><span class="sxs-lookup"><span data-stu-id="23ec8-110">Defines an alternate reference for an image.</span></span> <span data-ttu-id="23ec8-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="23ec8-111">Read/write.</span></span> <span data-ttu-id="23ec8-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="23ec8-112">**String**.</span></span>

<span data-ttu-id="23ec8-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="23ec8-113">**Applies To**</span></span>

[<span data-ttu-id="23ec8-114">Fill</span><span class="sxs-lookup"><span data-stu-id="23ec8-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="23ec8-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="23ec8-115">**Tag Syntax**</span></span>

<span data-ttu-id="23ec8-116"><v: *element* o:althref = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="23ec8-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="23ec8-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="23ec8-117">**Script Syntax**</span></span>

<span data-ttu-id="23ec8-118">*element* . althref = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="23ec8-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="23ec8-119">*espressione* = *elemento*. althref</span><span class="sxs-lookup"><span data-stu-id="23ec8-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="23ec8-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="23ec8-120">**Remarks**</span></span>

<span data-ttu-id="23ec8-121">Supporta la conservazione dei dati PICT tramite Roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="23ec8-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="23ec8-122">Nella scrittura HTML la rappresentazione alternativa, ovvero i dati PICT originali se il file proviene da Apple Macintosh, viene salvata.</span><span class="sxs-lookup"><span data-stu-id="23ec8-122">On HTML write, the alternate representation (the original PICT data if the file originated from the Apple Macintosh) is saved.</span></span> <span data-ttu-id="23ec8-123">In HTML Read, **AltHRef** è favorito tramite **src**.</span><span class="sxs-lookup"><span data-stu-id="23ec8-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="23ec8-124">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="23ec8-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="23ec8-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="23ec8-125">**Example**</span></span>

<span data-ttu-id="23ec8-126">Il riempimento della forma dispone di un **AltHRef** che punta a un file denominato myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="23ec8-126">The fill of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 