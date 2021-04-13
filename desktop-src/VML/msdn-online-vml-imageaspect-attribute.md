---
title: Attributo ImageAspect di la
description: Attributo ImageAspect di la
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338118"
---
# <a name="vml-imageaspect-attribute"></a><span data-ttu-id="edfc8-103">Attributo ImageAspect di la</span><span class="sxs-lookup"><span data-stu-id="edfc8-103">VML ImageAspect Attribute</span></span>

<span data-ttu-id="edfc8-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="edfc8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="edfc8-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="edfc8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="edfc8-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="edfc8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="edfc8-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="edfc8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="edfc8-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="edfc8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="edfc8-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="edfc8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="edfc8-110">Definisce il modo in cui verranno mantenute le proporzioni dell'immagine del tratto.</span><span class="sxs-lookup"><span data-stu-id="edfc8-110">Defines how the stroke image aspect ratio will be preserved.</span></span> <span data-ttu-id="edfc8-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="edfc8-111">Read/write.</span></span> <span data-ttu-id="edfc8-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="edfc8-112">**String**.</span></span>

<span data-ttu-id="edfc8-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="edfc8-113">**Applies To**</span></span>

[<span data-ttu-id="edfc8-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="edfc8-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="edfc8-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="edfc8-115">**Tag Syntax**</span></span>

<span data-ttu-id="edfc8-116"><v:</span><span class="sxs-lookup"><span data-stu-id="edfc8-116"><v:</span></span>

<span data-ttu-id="edfc8-117">elemento *imageaspect = "* expression *" >*</span><span class="sxs-lookup"><span data-stu-id="edfc8-117">element *imageaspect="* expression *">*</span></span>

<span data-ttu-id="edfc8-118">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="edfc8-118">**Script Syntax**</span></span>

<span data-ttu-id="edfc8-119">Element *. imageaspect = "* Expression *"*</span><span class="sxs-lookup"><span data-stu-id="edfc8-119">element *.imageaspect="* expression *"*</span></span>

<span data-ttu-id="edfc8-120">*=* elemento Expression *. imageaspect*</span><span class="sxs-lookup"><span data-stu-id="edfc8-120">expression *=* element *.imageaspect*</span></span>

<span data-ttu-id="edfc8-121">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="edfc8-121">**Remarks**</span></span>

<span data-ttu-id="edfc8-122">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="edfc8-122">Values include:</span></span>



| <span data-ttu-id="edfc8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="edfc8-123">Value</span></span>   | <span data-ttu-id="edfc8-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edfc8-124">Description</span></span>                                |
|---------|--------------------------------------------|
| <span data-ttu-id="edfc8-125">Ignora</span><span class="sxs-lookup"><span data-stu-id="edfc8-125">Ignore</span></span>  | <span data-ttu-id="edfc8-126">Ignorare i problemi di aspetto.</span><span class="sxs-lookup"><span data-stu-id="edfc8-126">Ignore aspect issues.</span></span>                      |
| <span data-ttu-id="edfc8-127">AtLeast</span><span class="sxs-lookup"><span data-stu-id="edfc8-127">AtLeast</span></span> | <span data-ttu-id="edfc8-128">L'immagine è almeno uguale a **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="edfc8-128">Image is at least as big as **ImageSize**.</span></span> |
| <span data-ttu-id="edfc8-129">AtMost</span><span class="sxs-lookup"><span data-stu-id="edfc8-129">AtMost</span></span>  | <span data-ttu-id="edfc8-130">L'immagine non è maggiore di **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="edfc8-130">Image is no bigger than **ImageSize**.</span></span>     |



 

<span data-ttu-id="edfc8-131">In ogni caso, l'attributo **ImageSize** verrà regolato in modo da mantenere l'aspetto dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="edfc8-131">In each case, the **ImageSize** attribute will be adjusted to preserve the aspect of the image.</span></span>

<span data-ttu-id="edfc8-132">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="edfc8-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="edfc8-133">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="edfc8-133">**Example**</span></span>

<span data-ttu-id="edfc8-134">L'immagine del tratto sarà almeno uguale alla dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="edfc8-134">The stroke image will be at least as big as the image size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 