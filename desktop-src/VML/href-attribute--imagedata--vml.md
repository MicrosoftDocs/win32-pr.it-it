---
title: Attributo HRef (ImageData) (la)
description: Attributo HRef (ImageData) (la)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727431"
---
# <a name="href-attribute-imagedatavml"></a><span data-ttu-id="69515-103">Attributo HRef (ImageData) (la)</span><span class="sxs-lookup"><span data-stu-id="69515-103">HRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="69515-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="69515-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="69515-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="69515-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="69515-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="69515-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="69515-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="69515-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="69515-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="69515-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="69515-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="69515-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="69515-110">Definisce un URL per un'immagine.</span><span class="sxs-lookup"><span data-stu-id="69515-110">Defines a URL for an image.</span></span> <span data-ttu-id="69515-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="69515-111">Read/write.</span></span> <span data-ttu-id="69515-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="69515-112">**String**.</span></span>

<span data-ttu-id="69515-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="69515-113">**Applies To**</span></span>

[<span data-ttu-id="69515-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="69515-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="69515-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="69515-115">**Tag Syntax**</span></span>

<span data-ttu-id="69515-116"><v: *element* o:href = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="69515-116"><v: *element* o:href=" *expression* "></span></span>

<span data-ttu-id="69515-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="69515-117">**Script Syntax**</span></span>

<span data-ttu-id="69515-118">*element* . href = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="69515-118">*element* .href="*expression*"</span></span>

<span data-ttu-id="69515-119">*espressione* = *elemento*. href</span><span class="sxs-lookup"><span data-stu-id="69515-119">*expression*=*element*.href</span></span>

<span data-ttu-id="69515-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="69515-120">**Remarks**</span></span>

<span data-ttu-id="69515-121">Quando si fa clic sulla forma, il browser caricherà l'URL.</span><span class="sxs-lookup"><span data-stu-id="69515-121">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="69515-122">L'attributo **href** è simile all'attributo HTML **href** standard degli ancoraggi.</span><span class="sxs-lookup"><span data-stu-id="69515-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="69515-123">L'uso di questo attributo rende più semplice la creazione di immagini buttonswith in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="69515-123">Using this attribute makes it easy to create buttonswith images on a Web page.</span></span>

<span data-ttu-id="69515-124">Questo attributo viene usato da Microsoft Office solo se un'immagine è stata collegata e incorporata. Microsoft Word dispone di un'interfaccia utente per l'inserimento di immagini in questo modo.</span><span class="sxs-lookup"><span data-stu-id="69515-124">This attribute is used by Microsoft Office only if a picture has been linked and embedded.Microsoft Word has a user interface for inserting pictures this way.</span></span>

<span data-ttu-id="69515-125">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="69515-125">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="69515-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="69515-126">**Example**</span></span>

<span data-ttu-id="69515-127">Quando si fa clic sull'immagine, il browser caricherà il home page Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="69515-127">When the image is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 