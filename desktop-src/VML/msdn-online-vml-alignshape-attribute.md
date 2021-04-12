---
title: Attributo AlignShape di la
description: Attributo AlignShape di la
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339030"
---
# <a name="vml-alignshape-attribute"></a><span data-ttu-id="dc864-103">Attributo AlignShape di la</span><span class="sxs-lookup"><span data-stu-id="dc864-103">VML AlignShape Attribute</span></span>

<span data-ttu-id="dc864-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="dc864-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dc864-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="dc864-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dc864-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="dc864-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dc864-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="dc864-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dc864-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dc864-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dc864-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dc864-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dc864-110">Determina se un'immagine viene allineata a una forma.</span><span class="sxs-lookup"><span data-stu-id="dc864-110">Determines whether an image will align with a shape.</span></span> <span data-ttu-id="dc864-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="dc864-111">Read/write.</span></span> <span data-ttu-id="dc864-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="dc864-112">**VgTriState**.</span></span>

<span data-ttu-id="dc864-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="dc864-113">**Applies To**</span></span>

[<span data-ttu-id="dc864-114">Fill</span><span class="sxs-lookup"><span data-stu-id="dc864-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="dc864-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="dc864-115">**Tag Syntax**</span></span>

<span data-ttu-id="dc864-116"><v: *element* alignshape = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="dc864-116"><v: *element* alignshape=" *expression* "></span></span>

<span data-ttu-id="dc864-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="dc864-117">**Script Syntax**</span></span>

<span data-ttu-id="dc864-118">*element* . alignshape = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="dc864-118">*element* .alignshape="*expression*"</span></span>

<span data-ttu-id="dc864-119">*espressione* = *elemento*. alignshape</span><span class="sxs-lookup"><span data-stu-id="dc864-119">*expression*=*element*.alignshape</span></span>

<span data-ttu-id="dc864-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="dc864-120">**Remarks**</span></span>

<span data-ttu-id="dc864-121">Se **true**, l'immagine utilizzata per creare il riempimento è allineata alla forma.</span><span class="sxs-lookup"><span data-stu-id="dc864-121">If **True**, the image used to create the fill is aligned with the shape.</span></span> <span data-ttu-id="dc864-122">Se **false**, l'immagine utilizzata per creare il riempimento è allineata con la finestra.</span><span class="sxs-lookup"><span data-stu-id="dc864-122">If **False**, the image used to create the fill is aligned with the window.</span></span> <span data-ttu-id="dc864-123">L'impostazione predefinita è **True**.</span><span class="sxs-lookup"><span data-stu-id="dc864-123">Default is **True**.</span></span>

<span data-ttu-id="dc864-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="dc864-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="dc864-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="dc864-125">**Example**</span></span>

<span data-ttu-id="dc864-126">L'immagine di riempimento affiancata creata da myimage.gif è allineata alla finestra, non alla forma; anche se la forma viene ruotata, l'immagine non lo è.</span><span class="sxs-lookup"><span data-stu-id="dc864-126">The tiled fill image created from myimage.gif is aligned with the window, not the shape; even though the shape is rotated, the image is not.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 