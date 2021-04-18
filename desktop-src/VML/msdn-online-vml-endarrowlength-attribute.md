---
title: Attributo EndArrowLength di la
description: Attributo EndArrowLength di la
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299854"
---
# <a name="vml-endarrowlength-attribute"></a><span data-ttu-id="1c70f-103">Attributo EndArrowLength di la</span><span class="sxs-lookup"><span data-stu-id="1c70f-103">VML EndArrowLength Attribute</span></span>

<span data-ttu-id="1c70f-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1c70f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1c70f-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="1c70f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1c70f-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="1c70f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1c70f-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="1c70f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1c70f-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1c70f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1c70f-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1c70f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1c70f-110">Definisce una lunghezza della freccia per la fine di una riga.</span><span class="sxs-lookup"><span data-stu-id="1c70f-110">Defines an arrowhead length for the end of a line.</span></span> <span data-ttu-id="1c70f-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1c70f-111">Read/write.</span></span> <span data-ttu-id="1c70f-112">**VgArrowheadLength**.</span><span class="sxs-lookup"><span data-stu-id="1c70f-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="1c70f-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="1c70f-113">**Applies To**</span></span>

[<span data-ttu-id="1c70f-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="1c70f-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="1c70f-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="1c70f-115">**Tag Syntax**</span></span>

<span data-ttu-id="1c70f-116"><v: *element* endarrowlength = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="1c70f-116"><v: *element* endarrowlength=" *expression* "></span></span>

<span data-ttu-id="1c70f-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="1c70f-117">**Script Syntax**</span></span>

<span data-ttu-id="1c70f-118">*element* . endarrowlength = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="1c70f-118">*element* .endarrowlength="*expression*"</span></span>

<span data-ttu-id="1c70f-119">*espressione* = *elemento*. endarrowlength</span><span class="sxs-lookup"><span data-stu-id="1c70f-119">*expression*=*element*.endarrowlength</span></span>

<span data-ttu-id="1c70f-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="1c70f-120">**Remarks**</span></span>

<span data-ttu-id="1c70f-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="1c70f-121">Values include:</span></span>

-   <span data-ttu-id="1c70f-122">Short</span><span class="sxs-lookup"><span data-stu-id="1c70f-122">Short</span></span>
-   <span data-ttu-id="1c70f-123">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c70f-123">Medium (default)</span></span>
-   <span data-ttu-id="1c70f-124">long</span><span class="sxs-lookup"><span data-stu-id="1c70f-124">Long</span></span>

<span data-ttu-id="1c70f-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="1c70f-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="1c70f-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="1c70f-126">**Example**</span></span>

<span data-ttu-id="1c70f-127">Una linea viene disegnata con una freccia classica breve alla fine del tratto.</span><span class="sxs-lookup"><span data-stu-id="1c70f-127">A line is drawn with a short classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 