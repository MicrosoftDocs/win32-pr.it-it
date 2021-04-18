---
title: LA clip-attributo
description: LA clip-attributo
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300018"
---
# <a name="vml-clip-attribute"></a><span data-ttu-id="16270-103">LA clip-attributo</span><span class="sxs-lookup"><span data-stu-id="16270-103">VML Clip Attribute</span></span>

<span data-ttu-id="16270-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="16270-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="16270-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="16270-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="16270-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="16270-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="16270-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="16270-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="16270-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="16270-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="16270-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="16270-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="16270-110">Determina se il ritaglio è on.</span><span class="sxs-lookup"><span data-stu-id="16270-110">Determines whether the clipping is on.</span></span> <span data-ttu-id="16270-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="16270-111">Read/write.</span></span> <span data-ttu-id="16270-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="16270-112">**VgTriState**.</span></span>

<span data-ttu-id="16270-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="16270-113">**Applies To**</span></span>

[<span data-ttu-id="16270-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="16270-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="16270-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="16270-115">**Tag Syntax**</span></span>

<span data-ttu-id="16270-116"><v: *elemento* clip = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="16270-116"><v: *element* clip=" *expression* "></span></span>

<span data-ttu-id="16270-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="16270-117">**Script Syntax**</span></span>

<span data-ttu-id="16270-118">*element* . clip = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="16270-118">*element* .clip="*expression*"</span></span>

<span data-ttu-id="16270-119">*espressione* = *elemento*. clip</span><span class="sxs-lookup"><span data-stu-id="16270-119">*expression*=*element*.clip</span></span>

<span data-ttu-id="16270-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="16270-120">**Remarks**</span></span>

<span data-ttu-id="16270-121">Se il **clip** è **false**, la forma verrà ridimensionata in base al frame.</span><span class="sxs-lookup"><span data-stu-id="16270-121">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="16270-122">Se **true**, tutte le parti della forma che si trovano all'esterno del frame non verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="16270-122">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="16270-123">Si noti che l' [origine](origin-attribute--vmlframe--vml.md) e le [dimensioni](size-attribute--vmlframe.md) non verranno utilizzate a meno che la **clip** non sia **true**.</span><span class="sxs-lookup"><span data-stu-id="16270-123">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="16270-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="16270-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="16270-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="16270-125">**Example**</span></span>

<span data-ttu-id="16270-126">L'immagine definita nel file esterno verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="16270-126">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 