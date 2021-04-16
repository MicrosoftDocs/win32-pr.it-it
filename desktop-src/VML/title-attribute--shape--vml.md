---
title: Attributo title (Shape) (la)
description: Attributo title (Shape) (la)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474155"
---
# <a name="title-attribute-shapevml"></a><span data-ttu-id="3381a-103">Attributo title (Shape) (la)</span><span class="sxs-lookup"><span data-stu-id="3381a-103">Title Attribute (Shape)(VML)</span></span>

<span data-ttu-id="3381a-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3381a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3381a-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3381a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3381a-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3381a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3381a-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3381a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3381a-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3381a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3381a-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3381a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3381a-110">Definisce il testo visualizzato quando il puntatore del mouse viene spostato sulla forma.</span><span class="sxs-lookup"><span data-stu-id="3381a-110">Defines the text displayed when the mouse pointer moves over the shape.</span></span> <span data-ttu-id="3381a-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3381a-111">Read/write.</span></span> <span data-ttu-id="3381a-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="3381a-112">**String**.</span></span>

<span data-ttu-id="3381a-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="3381a-113">**Applies To**</span></span>

[<span data-ttu-id="3381a-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="3381a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3381a-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="3381a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3381a-116"><v: *element* title = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3381a-116"><v: *element* title=" *expression* "></span></span>

<span data-ttu-id="3381a-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="3381a-117">**Script Syntax**</span></span>

<span data-ttu-id="3381a-118">*element* . title = "*espressione*"</span><span class="sxs-lookup"><span data-stu-id="3381a-118">*element* .title="*expression*"</span></span>

<span data-ttu-id="3381a-119">*espressione* = *element*. title</span><span class="sxs-lookup"><span data-stu-id="3381a-119">*expression*=*element*.title</span></span>

<span data-ttu-id="3381a-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="3381a-120">**Remarks**</span></span>

<span data-ttu-id="3381a-121">L'attributo **title** è simile all'attributo del **titolo** HTML standard.</span><span class="sxs-lookup"><span data-stu-id="3381a-121">The **Title** attribute is similar to the standard HTML **Title** attribute.</span></span> <span data-ttu-id="3381a-122">Il comportamento di un titolo è simile a una descrizione comando di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3381a-122">The behavior of a title is similar to a Microsoft Windows ToolTip.</span></span>

<span data-ttu-id="3381a-123">**Attributo standard la**</span><span class="sxs-lookup"><span data-stu-id="3381a-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="3381a-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="3381a-124">**Example**</span></span>

<span data-ttu-id="3381a-125">Il titolo della forma è "visualizzazione Descrizione comando" e verrà visualizzato quando il puntatore del mouse viene spostato sulla forma.</span><span class="sxs-lookup"><span data-stu-id="3381a-125">The title of the shape is "ToolTip display" and will appear when the mouse pointer moves over the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="3381a-126">[Esempio di attributo title](/previous-versions/bb264097(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3381a-126">[Title Attribute Example](/previous-versions/bb264097(v=vs.85)).</span></span> <span data-ttu-id="3381a-127">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="3381a-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 