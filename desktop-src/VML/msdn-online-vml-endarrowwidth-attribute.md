---
title: Attributo EndArrowWidth di la
description: Attributo EndArrowWidth di la
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730154"
---
# <a name="vml-endarrowwidth-attribute"></a><span data-ttu-id="5c526-103">Attributo EndArrowWidth di la</span><span class="sxs-lookup"><span data-stu-id="5c526-103">VML EndArrowWidth Attribute</span></span>

<span data-ttu-id="5c526-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5c526-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5c526-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="5c526-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5c526-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="5c526-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5c526-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="5c526-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5c526-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5c526-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5c526-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5c526-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5c526-110">Definisce la larghezza della freccia per la fine di una riga.</span><span class="sxs-lookup"><span data-stu-id="5c526-110">Defines an arrowhead width for the end of a line.</span></span> <span data-ttu-id="5c526-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5c526-111">Read/write.</span></span> <span data-ttu-id="5c526-112">**VgArrowheadWidth**.</span><span class="sxs-lookup"><span data-stu-id="5c526-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="5c526-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="5c526-113">**Applies To**</span></span>

[<span data-ttu-id="5c526-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="5c526-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="5c526-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="5c526-115">**Tag Syntax**</span></span>

<span data-ttu-id="5c526-116"><v: *element* endarrowwidth = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5c526-116"><v: *element* endarrowwidth=" *expression* "></span></span>

<span data-ttu-id="5c526-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="5c526-117">**Script Syntax**</span></span>

<span data-ttu-id="5c526-118">*element* . endarrowwidth = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="5c526-118">*element* .endarrowwidth="*expression*"</span></span>

<span data-ttu-id="5c526-119">*espressione* = *elemento*. endarrowwidth</span><span class="sxs-lookup"><span data-stu-id="5c526-119">*expression*=*element*.endarrowwidth</span></span>

<span data-ttu-id="5c526-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="5c526-120">**Remarks**</span></span>

<span data-ttu-id="5c526-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="5c526-121">Values include:</span></span>

-   <span data-ttu-id="5c526-122">Limitare</span><span class="sxs-lookup"><span data-stu-id="5c526-122">Narrow</span></span>
-   <span data-ttu-id="5c526-123">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c526-123">Medium (default)</span></span>
-   <span data-ttu-id="5c526-124">Largo</span><span class="sxs-lookup"><span data-stu-id="5c526-124">Wide</span></span>

<span data-ttu-id="5c526-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="5c526-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="5c526-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="5c526-126">**Example**</span></span>

<span data-ttu-id="5c526-127">Una linea viene disegnata con una freccia classica ampia alla fine del tratto.</span><span class="sxs-lookup"><span data-stu-id="5c526-127">A line is drawn with a wide classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 