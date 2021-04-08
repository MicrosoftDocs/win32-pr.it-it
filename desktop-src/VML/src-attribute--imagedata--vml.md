---
title: Attributo src (ImageData) (la)
description: Attributo src (ImageData) (la)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046807"
---
# <a name="src-attribute-imagedatavml"></a><span data-ttu-id="95398-103">Attributo src (ImageData) (la)</span><span class="sxs-lookup"><span data-stu-id="95398-103">Src Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="95398-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="95398-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="95398-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="95398-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="95398-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="95398-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="95398-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="95398-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="95398-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="95398-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="95398-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="95398-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="95398-110">Definisce un'origine per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="95398-110">Defines a source for the image.</span></span> <span data-ttu-id="95398-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="95398-111">Read/write.</span></span> <span data-ttu-id="95398-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="95398-112">**String**.</span></span>

<span data-ttu-id="95398-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="95398-113">**Applies To**</span></span>

[<span data-ttu-id="95398-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="95398-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="95398-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="95398-115">**Tag Syntax**</span></span>

<span data-ttu-id="95398-116"><v: *element* src = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="95398-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="95398-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="95398-117">**Script Syntax**</span></span>

<span data-ttu-id="95398-118">*element* . src = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="95398-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="95398-119">*espressione* = *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="95398-119">*expression*=*element*.src</span></span>

<span data-ttu-id="95398-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="95398-120">**Remarks**</span></span>

<span data-ttu-id="95398-121">Questo attributo deve essere sempre utilizzato con l'elemento [ImageData](msdn-online-vml-imagedata-element.md) e puntare a dati di immagine validi per un'immagine da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="95398-121">This attribute must always be used with the [ImageData](msdn-online-vml-imagedata-element.md) element and point to valid image data for a picture to be displayed.</span></span> <span data-ttu-id="95398-122">Se questo attributo viene visualizzato senza [href](https://www.bing.com/search?q=HRef) o [title](title-attribute--imagedata--vml.md), l'immagine viene collegata.</span><span class="sxs-lookup"><span data-stu-id="95398-122">If this attribute appears without [HRef](https://www.bing.com/search?q=HRef) or [Title](title-attribute--imagedata--vml.md), then the image is linked.</span></span>

<span data-ttu-id="95398-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="95398-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="95398-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="95398-124">**Example**</span></span>

<span data-ttu-id="95398-125">L'origine dell'immagine è un file denominato "kids.jpg".</span><span class="sxs-lookup"><span data-stu-id="95398-125">The source of the image is a file named "kids.jpg".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 