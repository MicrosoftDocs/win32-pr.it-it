---
title: LA-attributo in scala di grigi
description: LA-attributo in scala di grigi
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399237"
---
# <a name="vml-grayscale-attribute"></a><span data-ttu-id="6671d-103">LA-attributo in scala di grigi</span><span class="sxs-lookup"><span data-stu-id="6671d-103">VML GrayScale Attribute</span></span>

<span data-ttu-id="6671d-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6671d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6671d-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="6671d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6671d-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="6671d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6671d-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="6671d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6671d-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6671d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6671d-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6671d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6671d-110">Determina se un'immagine verrà visualizzata in modalità scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="6671d-110">Determines whether a picture will be displayed in grayscale mode.</span></span> <span data-ttu-id="6671d-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6671d-111">Read/write.</span></span> <span data-ttu-id="6671d-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="6671d-112">**VgTriState**.</span></span>

<span data-ttu-id="6671d-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="6671d-113">**Applies To**</span></span>

[<span data-ttu-id="6671d-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="6671d-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="6671d-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="6671d-115">**Tag Syntax**</span></span>

<span data-ttu-id="6671d-116"><v: *elemento* scala di grigi = " *espressione* " ></span><span class="sxs-lookup"><span data-stu-id="6671d-116"><v: *element* grayscale=" *expression* "></span></span>

<span data-ttu-id="6671d-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="6671d-117">**Script Syntax**</span></span>

<span data-ttu-id="6671d-118">*element* . scalece = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="6671d-118">*element* .grayscale="*expression*"</span></span>

<span data-ttu-id="6671d-119">*espressione* = *elemento*. scala di grigi</span><span class="sxs-lookup"><span data-stu-id="6671d-119">*expression*=*element*.grayscale</span></span>

<span data-ttu-id="6671d-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="6671d-120">**Remarks**</span></span>

<span data-ttu-id="6671d-121">Se **true**, l'immagine verrà visualizzata in grigio anziché in colore.</span><span class="sxs-lookup"><span data-stu-id="6671d-121">If **True**, the picture will be displayed in grayscale instead of color.</span></span> <span data-ttu-id="6671d-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="6671d-122">The default is **False**.</span></span>

<span data-ttu-id="6671d-123">Il valore è basato sulla raccomandazione CCIR 709, che favorisce un peso più verde e produce risultati più soddisfacenti per il colore naturale.</span><span class="sxs-lookup"><span data-stu-id="6671d-123">The value is based according to CCIR recommendation 709, which favors more green weight and produces more pleasing results for natural color.</span></span>

<span data-ttu-id="6671d-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="6671d-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="6671d-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="6671d-125">**Example**</span></span>

<span data-ttu-id="6671d-126">L'immagine verrà visualizzata in scala di grigi anziché in colore.</span><span class="sxs-lookup"><span data-stu-id="6671d-126">The image will be displayed in grayscale instead of color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 