---
title: Attributo LineStyle di la
description: Attributo LineStyle di la
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727426"
---
# <a name="vml-linestyle-attribute"></a><span data-ttu-id="b5229-103">Attributo LineStyle di la</span><span class="sxs-lookup"><span data-stu-id="b5229-103">VML LineStyle Attribute</span></span>

<span data-ttu-id="b5229-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b5229-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b5229-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="b5229-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b5229-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="b5229-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b5229-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="b5229-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b5229-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b5229-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b5229-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b5229-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b5229-110">Definisce lo stile di linea del tratto.</span><span class="sxs-lookup"><span data-stu-id="b5229-110">Defines the line style of the stroke.</span></span> <span data-ttu-id="b5229-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b5229-111">Read/write.</span></span> <span data-ttu-id="b5229-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="b5229-112">**String**.</span></span>

<span data-ttu-id="b5229-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="b5229-113">**Applies To**</span></span>

[<span data-ttu-id="b5229-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="b5229-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="b5229-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="b5229-115">**Tag Syntax**</span></span>

<span data-ttu-id="b5229-116"><v: *element* LineStyle = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="b5229-116"><v: *element* linestyle=" *expression* "></span></span>

<span data-ttu-id="b5229-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="b5229-117">**Script Syntax**</span></span>

<span data-ttu-id="b5229-118">*element* . LineStyle = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="b5229-118">*element* .linestyle="*expression*"</span></span>

<span data-ttu-id="b5229-119">*espressione* = *elemento*. LineStyle</span><span class="sxs-lookup"><span data-stu-id="b5229-119">*expression*=*element*.linestyle</span></span>

<span data-ttu-id="b5229-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="b5229-120">**Remarks**</span></span>

<span data-ttu-id="b5229-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="b5229-121">Values include:</span></span>

-   <span data-ttu-id="b5229-122">Single (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5229-122">Single (default)</span></span>
-   <span data-ttu-id="b5229-123">ThinThin</span><span class="sxs-lookup"><span data-stu-id="b5229-123">ThinThin</span></span>
-   <span data-ttu-id="b5229-124">ThinThick</span><span class="sxs-lookup"><span data-stu-id="b5229-124">ThinThick</span></span>
-   <span data-ttu-id="b5229-125">ThickThin</span><span class="sxs-lookup"><span data-stu-id="b5229-125">ThickThin</span></span>
-   <span data-ttu-id="b5229-126">ThickBetweenThin</span><span class="sxs-lookup"><span data-stu-id="b5229-126">ThickBetweenThin</span></span>

<span data-ttu-id="b5229-127">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="b5229-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="b5229-128">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="b5229-128">**Example**</span></span>

<span data-ttu-id="b5229-129">Viene disegnata una doppia riga con due trattini sottili.</span><span class="sxs-lookup"><span data-stu-id="b5229-129">A double line is drawn with two thin strokes.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 