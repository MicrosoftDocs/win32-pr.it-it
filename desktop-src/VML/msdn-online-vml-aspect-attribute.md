---
title: Attributo aspect la
description: Attributo aspect la
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728335"
---
# <a name="vml-aspect-attribute"></a><span data-ttu-id="9a5c1-103">Attributo aspect la</span><span class="sxs-lookup"><span data-stu-id="9a5c1-103">VML Aspect Attribute</span></span>

<span data-ttu-id="9a5c1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9a5c1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9a5c1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9a5c1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9a5c1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9a5c1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9a5c1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9a5c1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9a5c1-110">Specifica il modo in cui verranno mantenute le proporzioni dell'immagine di riempimento.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-110">Specifies how the fill image aspect ratio will be preserved.</span></span> <span data-ttu-id="9a5c1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-111">Read/write.</span></span> <span data-ttu-id="9a5c1-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-112">**String**.</span></span>

<span data-ttu-id="9a5c1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="9a5c1-113">**Applies To**</span></span>

[<span data-ttu-id="9a5c1-114">Fill</span><span class="sxs-lookup"><span data-stu-id="9a5c1-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="9a5c1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="9a5c1-115">**Tag Syntax**</span></span>

<span data-ttu-id="9a5c1-116"><v: *elemento* aspect = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="9a5c1-116"><v: *element* aspect=" *expression* "></span></span>

<span data-ttu-id="9a5c1-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="9a5c1-117">**Script Syntax**</span></span>

<span data-ttu-id="9a5c1-118">*element* . aspect = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="9a5c1-118">*element* .aspect="*expression*"</span></span>

<span data-ttu-id="9a5c1-119">*espressione* = *elemento*. aspect</span><span class="sxs-lookup"><span data-stu-id="9a5c1-119">*expression*=*element*.aspect</span></span>

<span data-ttu-id="9a5c1-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="9a5c1-120">**Remarks**</span></span>

<span data-ttu-id="9a5c1-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="9a5c1-121">Values include:</span></span>



| <span data-ttu-id="9a5c1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9a5c1-122">Value</span></span>   | <span data-ttu-id="9a5c1-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a5c1-123">Description</span></span>                           |
|---------|---------------------------------------|
| <span data-ttu-id="9a5c1-124">ignore</span><span class="sxs-lookup"><span data-stu-id="9a5c1-124">ignore</span></span>  | <span data-ttu-id="9a5c1-125">Ignorare i problemi di aspetto.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-125">Ignore aspect issues.</span></span> <span data-ttu-id="9a5c1-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-126">Default.</span></span>        |
| <span data-ttu-id="9a5c1-127">atleast</span><span class="sxs-lookup"><span data-stu-id="9a5c1-127">atleast</span></span> | <span data-ttu-id="9a5c1-128">Le dimensioni dell'immagine sono pari almeno alla **dimensione**.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-128">Image is at least as big as **Size**.</span></span> |
| <span data-ttu-id="9a5c1-129">atmost</span><span class="sxs-lookup"><span data-stu-id="9a5c1-129">atmost</span></span>  | <span data-ttu-id="9a5c1-130">L'immagine non è più grande della **dimensione**.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-130">Image is no bigger than **Size**.</span></span>     |



 

<span data-ttu-id="9a5c1-131">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="9a5c1-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="9a5c1-132">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="9a5c1-132">**Example**</span></span>

<span data-ttu-id="9a5c1-133">L'immagine che compone il riempimento è maggiore o uguale a una dimensione di 10 punti per 10 punti.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-133">The image that makes up the fill is greater than or equal to a size of 10 points by 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 