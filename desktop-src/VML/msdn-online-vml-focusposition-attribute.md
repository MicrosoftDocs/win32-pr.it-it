---
title: Attributo FocusPosition di la
description: Attributo FocusPosition di la
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118427"
---
# <a name="vml-focusposition-attribute"></a><span data-ttu-id="ea668-103">Attributo FocusPosition di la</span><span class="sxs-lookup"><span data-stu-id="ea668-103">VML FocusPosition Attribute</span></span>

<span data-ttu-id="ea668-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ea668-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ea668-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ea668-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ea668-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ea668-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ea668-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ea668-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ea668-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ea668-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ea668-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ea668-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ea668-110">Definisce il centro di una sfumatura radiale.</span><span class="sxs-lookup"><span data-stu-id="ea668-110">Defines the center of a radial gradient.</span></span> <span data-ttu-id="ea668-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ea668-111">Read/write.</span></span> <span data-ttu-id="ea668-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="ea668-112">**VgVector2D**.</span></span>

<span data-ttu-id="ea668-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ea668-113">**Applies To**</span></span>

[<span data-ttu-id="ea668-114">Fill</span><span class="sxs-lookup"><span data-stu-id="ea668-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="ea668-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ea668-115">**Tag Syntax**</span></span>

<span data-ttu-id="ea668-116"><v: *element* focusposition = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ea668-116"><v: *element* focusposition=" *expression* "></span></span>

<span data-ttu-id="ea668-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="ea668-117">**Script Syntax**</span></span>

<span data-ttu-id="ea668-118">*element* . focusposition = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="ea668-118">*element* .focusposition="*expression*"</span></span>

<span data-ttu-id="ea668-119">*espressione* = *elemento*. focusposition</span><span class="sxs-lookup"><span data-stu-id="ea668-119">*expression*=*element*.focusposition</span></span>

<span data-ttu-id="ea668-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ea668-120">**Remarks**</span></span>

<span data-ttu-id="ea668-121">Specifica le sfumature radiali al centro positionfor.</span><span class="sxs-lookup"><span data-stu-id="ea668-121">Specifies the center positionfor radial gradients.</span></span> <span data-ttu-id="ea668-122">Il vettore è una frazione della larghezza e dell'altezza della forma.</span><span class="sxs-lookup"><span data-stu-id="ea668-122">The vector is a fraction of the width and height of the shape.</span></span> <span data-ttu-id="ea668-123">Il primo è una percentuale del riempimento al bordo sinistro; il secondo è una percentuale del riempimento nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="ea668-123">The first is a percentage of the fill to the left edge; the second is a percentage of the fill to the top.</span></span> <span data-ttu-id="ea668-124">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="ea668-124">The default value is 0,0.</span></span> <span data-ttu-id="ea668-125">Per posizionare un riempimento radiale al centro di una forma, utilizzare il valore del 50%, del 50%.</span><span class="sxs-lookup"><span data-stu-id="ea668-125">To position a radial fill at the center of a shape, use the value of 50%,50%.</span></span>

<span data-ttu-id="ea668-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="ea668-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="ea668-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="ea668-127">**Example**</span></span>

<span data-ttu-id="ea668-128">Il riempimento radiale verrà centrato in modo che il blu si avvii al centro e si irradia verso l'esterno, cambiando gradualmente in rosso nel momento in cui raggiunge i bordi esterni e gli angoli.</span><span class="sxs-lookup"><span data-stu-id="ea668-128">The radial fill will be centered so that blue will start in the center and radiate outward, gradually changing to red by the time it reaches the outside edges and corners.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 