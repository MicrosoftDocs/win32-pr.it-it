---
title: Attributo ImageAlignShape di la
description: Attributo ImageAlignShape di la
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82aaab9c4c470b41bcf9fdb96ee2c048a7d0b81d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338119"
---
# <a name="vml-imagealignshape-attribute"></a><span data-ttu-id="f4141-103">Attributo ImageAlignShape di la</span><span class="sxs-lookup"><span data-stu-id="f4141-103">VML ImageAlignShape Attribute</span></span>

<span data-ttu-id="f4141-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f4141-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f4141-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="f4141-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f4141-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="f4141-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f4141-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="f4141-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f4141-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f4141-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f4141-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f4141-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f4141-110">Determina l'allineamento dell'immagine del tratto.</span><span class="sxs-lookup"><span data-stu-id="f4141-110">Determines the alignment of the stroke image.</span></span> <span data-ttu-id="f4141-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f4141-111">Read/write.</span></span> <span data-ttu-id="f4141-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="f4141-112">**VgTriState**.</span></span>

<span data-ttu-id="f4141-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="f4141-113">**Applies To**</span></span>

[<span data-ttu-id="f4141-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="f4141-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="f4141-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="f4141-115">**Tag Syntax**</span></span>

<span data-ttu-id="f4141-116"><v:</span><span class="sxs-lookup"><span data-stu-id="f4141-116"><v:</span></span>

<span data-ttu-id="f4141-117">elemento *imagealignshape = "* expression *" >*</span><span class="sxs-lookup"><span data-stu-id="f4141-117">element *imagealignshape="* expression *">*</span></span>

<span data-ttu-id="f4141-118">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="f4141-118">**Script Syntax**</span></span>

<span data-ttu-id="f4141-119">Element *. imagealignshape = "* Expression *"*</span><span class="sxs-lookup"><span data-stu-id="f4141-119">element *.imagealignshape="* expression *"*</span></span>

<span data-ttu-id="f4141-120">*=* elemento Expression *. imagealignshape*</span><span class="sxs-lookup"><span data-stu-id="f4141-120">expression *=* element *.imagealignshape*</span></span>

<span data-ttu-id="f4141-121">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="f4141-121">**Remarks**</span></span>

<span data-ttu-id="f4141-122">Se **true**, allineare l'immagine alla forma, altrimenti allineare l'immagine alla finestra.</span><span class="sxs-lookup"><span data-stu-id="f4141-122">If **True**, align the image with the shape, else align the image with the window.</span></span> <span data-ttu-id="f4141-123">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="f4141-123">The default is **True**.</span></span>

<span data-ttu-id="f4141-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="f4141-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f4141-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="f4141-125">**Example**</span></span>

<span data-ttu-id="f4141-126">L'immagine è allineata con la finestra.</span><span class="sxs-lookup"><span data-stu-id="f4141-126">The image is aligned with the window.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 