---
title: Attributo src (Fill) (la)
description: Attributo src (Fill) (la)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473198"
---
# <a name="src-attribute-fillvml"></a><span data-ttu-id="bfaf4-103">Attributo src (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="bfaf4-103">Src Attribute (Fill)(VML)</span></span>

<span data-ttu-id="bfaf4-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bfaf4-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bfaf4-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bfaf4-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bfaf4-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bfaf4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bfaf4-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bfaf4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bfaf4-110">Definisce l'immagine da caricare per un riempimento.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-110">Defines the image to load for a fill.</span></span> <span data-ttu-id="bfaf4-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-111">Read/write.</span></span> <span data-ttu-id="bfaf4-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-112">**String**.</span></span>

<span data-ttu-id="bfaf4-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="bfaf4-113">**Applies To**</span></span>

[<span data-ttu-id="bfaf4-114">Fill</span><span class="sxs-lookup"><span data-stu-id="bfaf4-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="bfaf4-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="bfaf4-115">**Tag Syntax**</span></span>

<span data-ttu-id="bfaf4-116"><v: *element* src = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="bfaf4-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="bfaf4-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="bfaf4-117">**Script Syntax**</span></span>

<span data-ttu-id="bfaf4-118">*element* . src = "*Expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="bfaf4-118">*element* .src="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="bfaf4-119">*espressione* = *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="bfaf4-119">*expression*=*element*.src</span></span>

<span data-ttu-id="bfaf4-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="bfaf4-120">**Remarks**</span></span>

<span data-ttu-id="bfaf4-121">URL di un'immagine da caricare per le compilazioni di immagini e modelli.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="bfaf4-122">Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="bfaf4-123">Se questo attributo viene visualizzato da solo (ovvero senza **href** o attributo **title** ), l'immagine viene collegata.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-123">If this attribute appears alone (that is, no **HRef** or **Title** attribute), then the image is linked.</span></span>

<span data-ttu-id="bfaf4-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="bfaf4-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="bfaf4-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="bfaf4-125">**Example**</span></span>

<span data-ttu-id="bfaf4-126">Viene visualizzata un'immagine affiancata che usa il file myimage.gif come origine.</span><span class="sxs-lookup"><span data-stu-id="bfaf4-126">A tiled image using the file myimage.gif as a source is displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 