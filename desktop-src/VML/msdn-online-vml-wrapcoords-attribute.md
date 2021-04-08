---
title: Attributo WrapCoords di la
description: Attributo WrapCoords di la
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727962"
---
# <a name="vml-wrapcoords-attribute"></a><span data-ttu-id="5ceb4-103">Attributo WrapCoords di la</span><span class="sxs-lookup"><span data-stu-id="5ceb4-103">VML WrapCoords Attribute</span></span>

<span data-ttu-id="5ceb4-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5ceb4-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5ceb4-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5ceb4-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5ceb4-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5ceb4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5ceb4-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5ceb4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5ceb4-110">Definisce il poligono delimitatore che racchiude una forma.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-110">Defines the bounding polygon that surrounds a shape.</span></span> <span data-ttu-id="5ceb4-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-111">Read/write.</span></span> <span data-ttu-id="5ceb4-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-112">**String**.</span></span>

<span data-ttu-id="5ceb4-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="5ceb4-113">**Applies To**</span></span>

[<span data-ttu-id="5ceb4-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="5ceb4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="5ceb4-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="5ceb4-115">**Tag Syntax**</span></span>

<span data-ttu-id="5ceb4-116"><v: *element* o:wrapcoords = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5ceb4-116"><v: *element* o:wrapcoords=" *expression* "></span></span>

<span data-ttu-id="5ceb4-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="5ceb4-117">**Remarks**</span></span>

<span data-ttu-id="5ceb4-118">Descrive un elenco delimitato da virgole di x e ycoordinates; ovvero "x1, Y1, X2, Y2, X3, Y3,..." Viene usato quando il testo viene racchiuso tra parentesi intorno a una forma.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-118">Describes a comma-delimited list of x and ycoordinates; that is, "x1,y1,x2,y2,x3,y3,..." This is used when text is tightly wrapped around a shape.</span></span> <span data-ttu-id="5ceb4-119">Il valore predefinito è **null** (una stringa vuota) finché l'attributo **MSO-Wrap-Mode** non è impostato su **Tight** o **through**.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-119">The default is **NULL** (an empty string) until the **MSO-Wrap-Mode** attribute is set to **tight** or **through**.</span></span>

<span data-ttu-id="5ceb4-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="5ceb4-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="5ceb4-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="5ceb4-121">**Example**</span></span>

<span data-ttu-id="5ceb4-122">La forma presenta un rettangolo di delimitazione del testo di 5 unità di dimensioni maggiori rispetto al percorso.</span><span class="sxs-lookup"><span data-stu-id="5ceb4-122">The shape has a text wrap bounding box that is 5 units larger than the path.</span></span>


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 