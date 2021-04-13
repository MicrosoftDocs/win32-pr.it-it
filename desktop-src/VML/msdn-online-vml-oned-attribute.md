---
title: Attributo OnEd di la
description: Attributo OnEd di la
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339015"
---
# <a name="vml-oned-attribute"></a><span data-ttu-id="a20e7-103">Attributo OnEd di la</span><span class="sxs-lookup"><span data-stu-id="a20e7-103">VML OnEd Attribute</span></span>

<span data-ttu-id="a20e7-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a20e7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a20e7-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a20e7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a20e7-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a20e7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a20e7-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a20e7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a20e7-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a20e7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a20e7-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a20e7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a20e7-110">Determina se gli handle aggiuntivi di una forma sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="a20e7-110">Determines whether the extra handles of a shape are hidden.</span></span> <span data-ttu-id="a20e7-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a20e7-111">Read/write.</span></span> <span data-ttu-id="a20e7-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a20e7-112">**VgTriState**.</span></span>

<span data-ttu-id="a20e7-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="a20e7-113">**Applies To**</span></span>

[<span data-ttu-id="a20e7-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="a20e7-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a20e7-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="a20e7-115">**Tag Syntax**</span></span>

<span data-ttu-id="a20e7-116"><v: *element* o:oned = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a20e7-116"><v: *element* o:oned=" *expression* "></span></span>

<span data-ttu-id="a20e7-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="a20e7-117">**Remarks**</span></span>

<span data-ttu-id="a20e7-118">Nasconde tutti gli handle di forma ad eccezione della parte superiore sinistra e della parte inferiore destra; ovvero gli stessi handle utilizzati per un segmento di linea retta.</span><span class="sxs-lookup"><span data-stu-id="a20e7-118">Hides all shape handles except the top left and bottom right; that is, the same handles that are used for a straight line segment.</span></span> <span data-ttu-id="a20e7-119">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="a20e7-119">The default is **False**.</span></span>

<span data-ttu-id="a20e7-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="a20e7-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="a20e7-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="a20e7-121">**Example**</span></span>

<span data-ttu-id="a20e7-122">Tutti gli handle, tranne quelli in alto a sinistra e in basso a destra, della forma sono nascosti.</span><span class="sxs-lookup"><span data-stu-id="a20e7-122">All but the top left and bottom right handles of the shape are hidden.</span></span>


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 