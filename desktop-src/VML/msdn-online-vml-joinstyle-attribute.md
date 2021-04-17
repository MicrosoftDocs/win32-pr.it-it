---
title: Attributo JoinStyle di la
description: Attributo JoinStyle di la
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300012"
---
# <a name="vml-joinstyle-attribute"></a><span data-ttu-id="c7d07-103">Attributo JoinStyle di la</span><span class="sxs-lookup"><span data-stu-id="c7d07-103">VML JoinStyle Attribute</span></span>

<span data-ttu-id="c7d07-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c7d07-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c7d07-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c7d07-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c7d07-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c7d07-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c7d07-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c7d07-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c7d07-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c7d07-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c7d07-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c7d07-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c7d07-110">Definisce lo stile di join di una polilinea.</span><span class="sxs-lookup"><span data-stu-id="c7d07-110">Defines the join style of a polyline.</span></span> <span data-ttu-id="c7d07-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c7d07-111">Read/write.</span></span> <span data-ttu-id="c7d07-112">Stringa.</span><span class="sxs-lookup"><span data-stu-id="c7d07-112">String.</span></span>

<span data-ttu-id="c7d07-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="c7d07-113">**Applies To**</span></span>

[<span data-ttu-id="c7d07-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="c7d07-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="c7d07-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="c7d07-115">**Tag Syntax**</span></span>

<span data-ttu-id="c7d07-116"><v: *element* joinstyle = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c7d07-116"><v: *element* joinstyle=" *expression* "></span></span>

<span data-ttu-id="c7d07-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="c7d07-117">**Script Syntax**</span></span>

<span data-ttu-id="c7d07-118">*element* . joinstyle = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="c7d07-118">*element* .joinstyle="*expression*"</span></span>

<span data-ttu-id="c7d07-119">*espressione* = *elemento*. joinstyle</span><span class="sxs-lookup"><span data-stu-id="c7d07-119">*expression*=*element*.joinstyle</span></span>

<span data-ttu-id="c7d07-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="c7d07-120">**Remarks**</span></span>

<span data-ttu-id="c7d07-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="c7d07-121">Values include:</span></span>

-   <span data-ttu-id="c7d07-122">Round (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7d07-122">round (default)</span></span>
-   <span data-ttu-id="c7d07-123">smussatura</span><span class="sxs-lookup"><span data-stu-id="c7d07-123">bevel</span></span>
-   <span data-ttu-id="c7d07-124">quartabuono</span><span class="sxs-lookup"><span data-stu-id="c7d07-124">miter</span></span>

<span data-ttu-id="c7d07-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="c7d07-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="c7d07-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="c7d07-126">**Example**</span></span>

<span data-ttu-id="c7d07-127">Le giunzioni sulla polilinea sono smussate.</span><span class="sxs-lookup"><span data-stu-id="c7d07-127">The joints on the polyline are beveled.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 