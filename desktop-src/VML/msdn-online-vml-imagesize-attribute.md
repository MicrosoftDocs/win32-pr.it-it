---
title: Attributo ImageSize di la
description: Attributo ImageSize di la
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae01d3162fdff67f0385736e5f0450b14ed6115
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728087"
---
# <a name="vml-imagesize-attribute"></a><span data-ttu-id="d6df1-103">Attributo ImageSize di la</span><span class="sxs-lookup"><span data-stu-id="d6df1-103">VML ImageSize Attribute</span></span>

<span data-ttu-id="d6df1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d6df1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d6df1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d6df1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d6df1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d6df1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d6df1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d6df1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d6df1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d6df1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d6df1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d6df1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d6df1-110">Definisce le dimensioni dell'immagine per il tratto.</span><span class="sxs-lookup"><span data-stu-id="d6df1-110">Defines the size of the image for the stroke.</span></span> <span data-ttu-id="d6df1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d6df1-111">Read/write.</span></span> <span data-ttu-id="d6df1-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="d6df1-112">**VgVector2D**.</span></span>

<span data-ttu-id="d6df1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d6df1-113">**Applies To**</span></span>

[<span data-ttu-id="d6df1-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="d6df1-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="d6df1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d6df1-115">**Tag Syntax**</span></span>

<span data-ttu-id="d6df1-116"><v: *element* ImageSize = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d6df1-116"><v: *element* imagesize=" *expression* "></span></span>

<span data-ttu-id="d6df1-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d6df1-117">**Script Syntax**</span></span>

<span data-ttu-id="d6df1-118">*element* . ImageSize = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d6df1-118">*element* .imagesize="*expression*"</span></span>

<span data-ttu-id="d6df1-119">*espressione* = *elemento*. ImageSize</span><span class="sxs-lookup"><span data-stu-id="d6df1-119">*expression*=*element*.imagesize</span></span>

<span data-ttu-id="d6df1-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d6df1-120">**Remarks**</span></span>

<span data-ttu-id="d6df1-121">Il valore predefinito corrisponde alla dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="d6df1-121">Default is the size of the image.</span></span>

<span data-ttu-id="d6df1-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="d6df1-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="d6df1-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d6df1-123">**Example**</span></span>

<span data-ttu-id="d6df1-124">L'immagine del tratto sarà una dimensione di 10 per 10 punti.</span><span class="sxs-lookup"><span data-stu-id="d6df1-124">The stroke image will be a 10-by-10 point size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 