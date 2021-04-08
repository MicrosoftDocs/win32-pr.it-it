---
title: Attributo bilevel la
description: Attributo bilevel la
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728311"
---
# <a name="vml-bilevel-attribute"></a><span data-ttu-id="9bc43-103">Attributo bilevel la</span><span class="sxs-lookup"><span data-stu-id="9bc43-103">VML Bilevel Attribute</span></span>

<span data-ttu-id="9bc43-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9bc43-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9bc43-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="9bc43-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9bc43-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="9bc43-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9bc43-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="9bc43-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9bc43-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9bc43-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9bc43-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9bc43-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9bc43-110">Determina se un'immagine verrà visualizzata in bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="9bc43-110">Determines whether an image will be displayed in black and white.</span></span> <span data-ttu-id="9bc43-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9bc43-111">Read/write.</span></span> <span data-ttu-id="9bc43-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="9bc43-112">**VgTriState**.</span></span>

<span data-ttu-id="9bc43-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="9bc43-113">**Applies To**</span></span>

[<span data-ttu-id="9bc43-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="9bc43-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="9bc43-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="9bc43-115">**Tag Syntax**</span></span>

<span data-ttu-id="9bc43-116"><v: *element* bilevel = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="9bc43-116"><v: *element* bilevel=" *expression* "></span></span>

<span data-ttu-id="9bc43-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="9bc43-117">**Script Syntax**</span></span>

<span data-ttu-id="9bc43-118">*element* . bilevel = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="9bc43-118">*element* .bilevel="*expression*"</span></span>

<span data-ttu-id="9bc43-119">*espressione* = *element*. bilevel</span><span class="sxs-lookup"><span data-stu-id="9bc43-119">*expression*=*element*.bilevel</span></span>

<span data-ttu-id="9bc43-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="9bc43-120">**Remarks**</span></span>

<span data-ttu-id="9bc43-121">Se **true**, l'immagine verrà visualizzata utilizzando due colori (nero e bianco).</span><span class="sxs-lookup"><span data-stu-id="9bc43-121">If **True**, the image will be displayed using two colors (black and white).</span></span> <span data-ttu-id="9bc43-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="9bc43-122">The default is **False**.</span></span> <span data-ttu-id="9bc43-123">In questo modo viene creato un effetto simile alla posterzzazione.</span><span class="sxs-lookup"><span data-stu-id="9bc43-123">This creates an effect similar to posterization.</span></span>

<span data-ttu-id="9bc43-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="9bc43-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="9bc43-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="9bc43-125">**Example**</span></span>

<span data-ttu-id="9bc43-126">L'immagine verrà visualizzata solo in bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="9bc43-126">The image will be displayed in black and white only.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 