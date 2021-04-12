---
title: Attributo CropTop di la
description: Attributo CropTop di la
ms.assetid: b54939b6-0505-43b0-bf82-c3df82dc2633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8b2606c7ac5835caeecc145a885de48eaeaf8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337719"
---
# <a name="vml-croptop-attribute"></a><span data-ttu-id="d35be-103">Attributo CropTop di la</span><span class="sxs-lookup"><span data-stu-id="d35be-103">VML CropTop Attribute</span></span>

<span data-ttu-id="d35be-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d35be-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d35be-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d35be-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d35be-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d35be-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d35be-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d35be-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d35be-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d35be-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d35be-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d35be-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d35be-110">Definisce la percentuale di rimozione dell'immagine dal lato superiore.</span><span class="sxs-lookup"><span data-stu-id="d35be-110">Defines the percentage of picture removal from the top side.</span></span> <span data-ttu-id="d35be-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d35be-111">Read/write.</span></span> <span data-ttu-id="d35be-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="d35be-112">**VgNumber**.</span></span>

<span data-ttu-id="d35be-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d35be-113">**Applies To**</span></span>

[<span data-ttu-id="d35be-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="d35be-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="d35be-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d35be-115">**Tag Syntax**</span></span>

<span data-ttu-id="d35be-116"><v: *element* CropTop = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d35be-116"><v: *element* croptop=" *expression* "></span></span>

<span data-ttu-id="d35be-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d35be-117">**Script Syntax**</span></span>

<span data-ttu-id="d35be-118">*element* . CropTop = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d35be-118">*element* .croptop="*expression*"</span></span>

<span data-ttu-id="d35be-119">*espressione* = *elemento*. CropTop</span><span class="sxs-lookup"><span data-stu-id="d35be-119">*expression*=*element*.croptop</span></span>

<span data-ttu-id="d35be-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d35be-120">**Remarks**</span></span>

<span data-ttu-id="d35be-121">La quantità di ritaglio può variare da-1,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="d35be-121">The amount of cropping can range from -1.0 to 1.0.</span></span> <span data-ttu-id="d35be-122">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="d35be-122">The default value is 0.</span></span> <span data-ttu-id="d35be-123">Si noti che il valore 1 non visualizza alcuna immagine.</span><span class="sxs-lookup"><span data-stu-id="d35be-123">Note that a value of 1 will display no picture at all.</span></span> <span data-ttu-id="d35be-124">I valori negativi comportano la compressione dell'immagine verso l'interno dal bordo che viene ritagliato (lo spazio vuoto tra l'immagine e il bordo ritagliato verrà riempito con il colore di riempimento della forma).</span><span class="sxs-lookup"><span data-stu-id="d35be-124">Negative values will result in the picture being squeezed inward from the edge being cropped (the empty space between the picture and the cropped edge will be filled by the fill color of the shape).</span></span> <span data-ttu-id="d35be-125">I valori positivi minori di 1 comportano l'estensione dell'immagine rimanente per adattarla alla forma.</span><span class="sxs-lookup"><span data-stu-id="d35be-125">Positive values less than 1 will result in the remaining picture being stretched to fit the shape.</span></span>

<span data-ttu-id="d35be-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="d35be-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="d35be-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d35be-127">**Example**</span></span>

<span data-ttu-id="d35be-128">L'immagine verrà compressa in un piccolo frammento nella parte inferiore della forma.</span><span class="sxs-lookup"><span data-stu-id="d35be-128">The picture will be squeezed into a narrow sliver at the bottom of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata croptop="-.8" src="kids.jpg"/>
   </v:shape>
```





 

 