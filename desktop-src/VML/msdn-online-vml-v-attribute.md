---
title: Attributo la V
description: Attributo la V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117942"
---
# <a name="vml-v-attribute"></a><span data-ttu-id="655dc-103">Attributo la V</span><span class="sxs-lookup"><span data-stu-id="655dc-103">VML V Attribute</span></span>

<span data-ttu-id="655dc-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="655dc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="655dc-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="655dc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="655dc-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="655dc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="655dc-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="655dc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="655dc-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="655dc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="655dc-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="655dc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="655dc-110">Definisce i comandi che costituiscono un percorso.</span><span class="sxs-lookup"><span data-stu-id="655dc-110">Defines the commands that make up a path.</span></span> <span data-ttu-id="655dc-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="655dc-111">Read/write.</span></span> <span data-ttu-id="655dc-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="655dc-112">**String**.</span></span>

<span data-ttu-id="655dc-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="655dc-113">**Applies To**</span></span>

[<span data-ttu-id="655dc-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="655dc-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="655dc-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="655dc-115">**Tag Syntax**</span></span>

<span data-ttu-id="655dc-116"><v: *element* v = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="655dc-116"><v: *element* v=" *expression* "></span></span>

<span data-ttu-id="655dc-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="655dc-117">**Script Syntax**</span></span>

<span data-ttu-id="655dc-118">*element* . v = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="655dc-118">*element* .v="*expression*"</span></span>

<span data-ttu-id="655dc-119">*espressione* = *elemento*. v</span><span class="sxs-lookup"><span data-stu-id="655dc-119">*expression*=*element*.v</span></span>

<span data-ttu-id="655dc-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="655dc-120">**Remarks**</span></span>

<span data-ttu-id="655dc-121">Esegue l'override dell'attributo **path** di una forma.</span><span class="sxs-lookup"><span data-stu-id="655dc-121">Overrides the **Path** attribute of a shape.</span></span> <span data-ttu-id="655dc-122">Le coordinate possono essere numeri fissi, numeri relativi o riferimenti alle formule (usando il formato " @n ", dove n è un numero di formula. ad esempio, " @2 " si riferisce alla seconda formula nella matrice di formule).</span><span class="sxs-lookup"><span data-stu-id="655dc-122">Coordinates can be fixed numbers, relative numbers, or references to formulas (by using the format of "@n" where n is a formula number; for example, "@2" refers to the second formula in the formula array).</span></span>

<span data-ttu-id="655dc-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="655dc-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="655dc-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="655dc-124">**Example**</span></span>

<span data-ttu-id="655dc-125">Un rettangolo viene creato usando l'attributo **V** .</span><span class="sxs-lookup"><span data-stu-id="655dc-125">A rectangle is created using the **V** attribute.</span></span> <span data-ttu-id="655dc-126">Si noti che viene usata una lettera minuscola L (comando **LineTo** ) dopo il primo set di coordinate delimitate da virgole.</span><span class="sxs-lookup"><span data-stu-id="655dc-126">Note that a lowercase letter L (**lineto** command) is used after the first set of comma-delimited coordinates.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 