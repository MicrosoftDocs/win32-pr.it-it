---
title: Attributo src (Stroke) (la)
description: Attributo src (Stroke) (la)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727543"
---
# <a name="src-attribute-strokevml"></a><span data-ttu-id="c8740-103">Attributo src (Stroke) (la)</span><span class="sxs-lookup"><span data-stu-id="c8740-103">Src Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="c8740-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c8740-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c8740-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c8740-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c8740-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c8740-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c8740-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c8740-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c8740-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c8740-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c8740-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c8740-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c8740-110">Definisce l'immagine di origine da caricare per un riempimento del tratto.</span><span class="sxs-lookup"><span data-stu-id="c8740-110">Defines the source image to load for a stroke fill.</span></span> <span data-ttu-id="c8740-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c8740-111">Read/write.</span></span> <span data-ttu-id="c8740-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="c8740-112">**String**.</span></span>

<span data-ttu-id="c8740-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="c8740-113">**Applies To**</span></span>

[<span data-ttu-id="c8740-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="c8740-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="c8740-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="c8740-115">**Tag Syntax**</span></span>

<span data-ttu-id="c8740-116"><v: *element* src = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c8740-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="c8740-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="c8740-117">**Script Syntax**</span></span>

<span data-ttu-id="c8740-118">*element* . src = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="c8740-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="c8740-119">*espressione* = *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="c8740-119">*expression*=*element*.src</span></span>

<span data-ttu-id="c8740-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="c8740-120">**Remarks**</span></span>

<span data-ttu-id="c8740-121">URL di un'immagine da caricare per le compilazioni di immagini e modelli.</span><span class="sxs-lookup"><span data-stu-id="c8740-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="c8740-122">Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine.</span><span class="sxs-lookup"><span data-stu-id="c8740-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="c8740-123">Se questo attributo viene visualizzato da solo, ovvero senza **href** o **title**, l'immagine viene collegata.</span><span class="sxs-lookup"><span data-stu-id="c8740-123">If this attribute appears alone, that is, no **HRef** or **Title**, then the image is linked.</span></span>

<span data-ttu-id="c8740-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="c8740-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="c8740-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="c8740-125">**Example**</span></span>

<span data-ttu-id="c8740-126">Il tratto viene creato con l'immagine specificata dal file di cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="c8740-126">The stroke is created with the image specified by the cylinder.gif file.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 