---
title: La MSO-wrap-distance-Top attributo
description: La MSO-wrap-distance-Top attributo
ms.assetid: 20444d16-fa84-4685-911c-288150c2674b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a16898733ead7bf3728d8f520888c8a05ef5fe6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300006"
---
# <a name="vml-mso-wrap-distance-top-attribute"></a><span data-ttu-id="c784d-103">La MSO-wrap-distance-Top attributo</span><span class="sxs-lookup"><span data-stu-id="c784d-103">VML MSO-Wrap-Distance-Top Attribute</span></span>

<span data-ttu-id="c784d-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c784d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c784d-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c784d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c784d-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c784d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c784d-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c784d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c784d-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c784d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c784d-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c784d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c784d-110">Definisce la distanza tra l'inizio della forma e il testo che lo racchiude.</span><span class="sxs-lookup"><span data-stu-id="c784d-110">Defines the distance from the shape top to the text that wraps around it.</span></span> <span data-ttu-id="c784d-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c784d-111">Read/write.</span></span> <span data-ttu-id="c784d-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="c784d-112">**String**.</span></span>

<span data-ttu-id="c784d-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="c784d-113">**Applies To**</span></span>

[<span data-ttu-id="c784d-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="c784d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c784d-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="c784d-115">**Tag Syntax**</span></span>

<span data-ttu-id="c784d-116"><v: *element* Style = "MSO-wrap-distance-Top: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c784d-116"><v: *element* style="mso-wrap-distance-top: *expression* "></span></span>

<span data-ttu-id="c784d-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="c784d-117">**Remarks**</span></span>

<span data-ttu-id="c784d-118">Si noti che questo attributo è diverso dall'attributo del **margine** CSS.</span><span class="sxs-lookup"><span data-stu-id="c784d-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="c784d-119">**Margin** modifica l'origine della forma in modo da includere le aree dei margini, ma la distanza dal ritorno a capo nell'Microsoft Office non modifica l'origine della forma.</span><span class="sxs-lookup"><span data-stu-id="c784d-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="c784d-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="c784d-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="c784d-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="c784d-121">**Example**</span></span>

<span data-ttu-id="c784d-122">La forma ha una distanza di ritorno a capo superiore di 10 punti.</span><span class="sxs-lookup"><span data-stu-id="c784d-122">The shape has a top wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 