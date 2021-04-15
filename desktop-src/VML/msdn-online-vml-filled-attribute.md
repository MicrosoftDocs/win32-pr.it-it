---
title: Attributo riempito la
description: Attributo riempito la
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474187"
---
# <a name="vml-filled-attribute"></a><span data-ttu-id="f1290-103">Attributo riempito la</span><span class="sxs-lookup"><span data-stu-id="f1290-103">VML Filled Attribute</span></span>

<span data-ttu-id="f1290-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f1290-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f1290-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="f1290-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f1290-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="f1290-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f1290-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="f1290-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f1290-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f1290-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f1290-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f1290-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f1290-110">Determina se verrà compilato il percorso chiuso.</span><span class="sxs-lookup"><span data-stu-id="f1290-110">Determines whether the closed path will be filled.</span></span> <span data-ttu-id="f1290-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f1290-111">Read/write.</span></span> <span data-ttu-id="f1290-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="f1290-112">**VgTriState**.</span></span>

<span data-ttu-id="f1290-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="f1290-113">**Applies To**</span></span>

[<span data-ttu-id="f1290-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="f1290-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f1290-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="f1290-115">**Tag Syntax**</span></span>

<span data-ttu-id="f1290-116"><v: *elemento* filled = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="f1290-116"><v: *element* filled=" *expression* "></span></span>

<span data-ttu-id="f1290-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="f1290-117">**Script Syntax**</span></span>

<span data-ttu-id="f1290-118">*element* . filled = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="f1290-118">*element* .filled="*expression*"</span></span>

<span data-ttu-id="f1290-119">*espressione* = *elemento*. filled</span><span class="sxs-lookup"><span data-stu-id="f1290-119">*expression*=*element*.filled</span></span>

<span data-ttu-id="f1290-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="f1290-120">**Remarks**</span></span>

<span data-ttu-id="f1290-121">Il valore viene duplicato dall'attributo **on** dell'elemento [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1290-121">The value is duplicated from the **On** attribute of the [Fill](msdn-online-vml-fill-element.md) element.</span></span>

<span data-ttu-id="f1290-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="f1290-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="f1290-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="f1290-123">**Example**</span></span>

<span data-ttu-id="f1290-124">Il percorso della forma è pieno.</span><span class="sxs-lookup"><span data-stu-id="f1290-124">The shape path is filled.</span></span>


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="f1290-125">[Esempio di attributo compilato](/previous-versions/bb229669(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1290-125">[Filled Attribute Example](/previous-versions/bb229669(v=vs.85)).</span></span> <span data-ttu-id="f1290-126">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="f1290-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 