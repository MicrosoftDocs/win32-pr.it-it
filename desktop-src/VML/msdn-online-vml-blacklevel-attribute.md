---
title: Attributo BlackLevel di la
description: Attributo BlackLevel di la
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046955"
---
# <a name="vml-blacklevel-attribute"></a><span data-ttu-id="e5045-103">Attributo BlackLevel di la</span><span class="sxs-lookup"><span data-stu-id="e5045-103">VML BlackLevel Attribute</span></span>

<span data-ttu-id="e5045-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e5045-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e5045-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e5045-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e5045-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e5045-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e5045-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e5045-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e5045-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e5045-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e5045-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e5045-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e5045-110">Definisce l'intensità del nero in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="e5045-110">Defines the intensity of black in an image.</span></span> <span data-ttu-id="e5045-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e5045-111">Read/write.</span></span> <span data-ttu-id="e5045-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="e5045-112">**VgNumber**.</span></span>

<span data-ttu-id="e5045-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e5045-113">**Applies To**</span></span>

[<span data-ttu-id="e5045-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="e5045-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="e5045-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e5045-115">**Tag Syntax**</span></span>

<span data-ttu-id="e5045-116"><v: *element* blacklevel = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e5045-116"><v: *element* blacklevel=" *expression* "></span></span>

<span data-ttu-id="e5045-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e5045-117">**Script Syntax**</span></span>

<span data-ttu-id="e5045-118">*element* . blacklevel = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e5045-118">*element* .blacklevel="*expression*"</span></span>

<span data-ttu-id="e5045-119">*espressione* = *elemento*. blacklevel</span><span class="sxs-lookup"><span data-stu-id="e5045-119">*expression*=*element*.blacklevel</span></span>

<span data-ttu-id="e5045-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e5045-120">**Remarks**</span></span>

<span data-ttu-id="e5045-121">Consente di modificare il livello di colore in modo che i neri appaiano come veri neri, mentre tutti gli altri colori sono visibili come ombreggiatura sopra il nero.</span><span class="sxs-lookup"><span data-stu-id="e5045-121">Allows the color level to be modified so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span> <span data-ttu-id="e5045-122">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="e5045-122">The default value is 0.</span></span> <span data-ttu-id="e5045-123">Mentre è consentito un numero compreso tra infinito positivo e negativo, i valori minori di-0,5 vengono visualizzati come tutti i neri e i valori maggiori di 0,5 vengono visualizzati come tutti i bianchi.</span><span class="sxs-lookup"><span data-stu-id="e5045-123">While any number between positive and negative infinity is permitted, values less than -0.5 will display as all black and values greater than 0.5 will display as all white.</span></span>

<span data-ttu-id="e5045-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="e5045-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="e5045-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e5045-125">**Example**</span></span>

<span data-ttu-id="e5045-126">L'immagine verrà visualizzata con toni molto scuri.</span><span class="sxs-lookup"><span data-stu-id="e5045-126">The image will be displayed with very dark tones.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 