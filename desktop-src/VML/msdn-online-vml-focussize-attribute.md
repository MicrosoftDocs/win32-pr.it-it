---
title: Attributo FocusSize di la
description: Attributo FocusSize di la
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047337"
---
# <a name="vml-focussize-attribute"></a><span data-ttu-id="ae9c2-103">Attributo FocusSize di la</span><span class="sxs-lookup"><span data-stu-id="ae9c2-103">VML FocusSize Attribute</span></span>

<span data-ttu-id="ae9c2-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ae9c2-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ae9c2-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ae9c2-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ae9c2-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ae9c2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ae9c2-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ae9c2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ae9c2-110">Definisce le dimensioni dello stato attivo per i riempimenti radiali.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-110">Defines the focus size for radial fills.</span></span> <span data-ttu-id="ae9c2-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-111">Read/write.</span></span> <span data-ttu-id="ae9c2-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-112">**VgVector2D**.</span></span>

<span data-ttu-id="ae9c2-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ae9c2-113">**Applies To**</span></span>

[<span data-ttu-id="ae9c2-114">Fill</span><span class="sxs-lookup"><span data-stu-id="ae9c2-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="ae9c2-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ae9c2-115">**Tag Syntax**</span></span>

<span data-ttu-id="ae9c2-116"><v: *element* focussize = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ae9c2-116"><v: *element* focussize=" *expression* "></span></span>

<span data-ttu-id="ae9c2-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="ae9c2-117">**Script Syntax**</span></span>

<span data-ttu-id="ae9c2-118">*element* . focussize = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="ae9c2-118">*element* .focussize="*expression*"</span></span>

<span data-ttu-id="ae9c2-119">*espressione* = *elemento*. focussize</span><span class="sxs-lookup"><span data-stu-id="ae9c2-119">*expression*=*element*.focussize</span></span>

<span data-ttu-id="ae9c2-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ae9c2-120">**Remarks**</span></span>

<span data-ttu-id="ae9c2-121">I valori sono frazioni della larghezza e dell'altezza della forma.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-121">The values are fractions of the width and height of the shape.</span></span> <span data-ttu-id="ae9c2-122">Il primo è una percentuale del riempimento al bordo destro della forma e la seconda è una percentuale del riempimento nella parte inferiore della forma.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-122">The first is a percentage of the fill to the right edge of the shape and the second is a percentage of the fill to the bottom of the shape.</span></span> <span data-ttu-id="ae9c2-123">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-123">The default value is 0,0.</span></span> <span data-ttu-id="ae9c2-124">Un valore **FocusSize** pari a 100%, 100% e un **FocusPosition** di 0, 0 renderebbe il totale di color2 che dominano completamente la Blend.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-124">A **FocusSize** value of 100%,100% and a **FocusPosition** of 0,0 would make Color2 dominate the blend completely.</span></span> <span data-ttu-id="ae9c2-125">Per le miscele bilanciate è consigliabile utilizzare valori di dimensioni ridotte di circa il 10%.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-125">Small values of around 10%,10% are recommended for balanced blends.</span></span>

<span data-ttu-id="ae9c2-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="ae9c2-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="ae9c2-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="ae9c2-127">**Example**</span></span>

<span data-ttu-id="ae9c2-128">Il riempimento radiale creerà una Blend che inizia al centro come blu e diventa rossa su tutti e quattro i bordi.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-128">The radial fill will create a blend starting in the center as blue and becoming red on all four edges.</span></span> <span data-ttu-id="ae9c2-129">Il centro della Blend viene definito da **FocusPosition** e la dimensione del colore iniziale interno è determinata da **FocusSize**.</span><span class="sxs-lookup"><span data-stu-id="ae9c2-129">The center of the blend is defined by **FocusPosition** and the size of the inner starting color is determined by **FocusSize**.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 