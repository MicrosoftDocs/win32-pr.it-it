---
title: Attributo la Weight
description: Attributo la Weight
ms.assetid: 40164818-6b04-4afe-91cc-9fb8b12cb718
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7a1a4d5dca91da6b3750f0d901d4e278a80dd7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299953"
---
# <a name="vml-weight-attribute"></a><span data-ttu-id="7b5f8-103">Attributo la Weight</span><span class="sxs-lookup"><span data-stu-id="7b5f8-103">VML Weight Attribute</span></span>

<span data-ttu-id="7b5f8-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7b5f8-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7b5f8-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7b5f8-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7b5f8-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7b5f8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7b5f8-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7b5f8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7b5f8-110">Definisce lo spessore di un tratto.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-110">Defines the thickness of a stroke.</span></span> <span data-ttu-id="7b5f8-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-111">Read/write.</span></span> <span data-ttu-id="7b5f8-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-112">**String**.</span></span>

<span data-ttu-id="7b5f8-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="7b5f8-113">**Applies To**</span></span>

[<span data-ttu-id="7b5f8-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="7b5f8-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="7b5f8-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="7b5f8-115">**Tag Syntax**</span></span>

<span data-ttu-id="7b5f8-116"><v: *element* weight = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="7b5f8-116"><v: *element* weight=" *expression* "></span></span>

<span data-ttu-id="7b5f8-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="7b5f8-117">**Script Syntax**</span></span>

<span data-ttu-id="7b5f8-118">*element* . Weight = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="7b5f8-118">*element* .weight="*expression*"</span></span>

<span data-ttu-id="7b5f8-119">*espressione* = *elemento*. peso</span><span class="sxs-lookup"><span data-stu-id="7b5f8-119">*expression*=*element*.weight</span></span>

<span data-ttu-id="7b5f8-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="7b5f8-120">**Remarks**</span></span>

<span data-ttu-id="7b5f8-121">Questo attributo è uguale all'attributo **StrokeWeight** della **forma** e ne esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-121">This attribute is the same as the **StrokeWeight** attribute of **Shape** and overrides it.</span></span> <span data-ttu-id="7b5f8-122">Il valore predefinito è 1 Point.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-122">The default value is 1 point.</span></span>

<span data-ttu-id="7b5f8-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="7b5f8-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7b5f8-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="7b5f8-124">**Example**</span></span>

<span data-ttu-id="7b5f8-125">Il tratto ha uno spessore di 5 punti, non 2 punti.</span><span class="sxs-lookup"><span data-stu-id="7b5f8-125">The stroke has a thickness of 5 points, not 2 points.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="2pt"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke weight="5pt"/>
   </v:shape>
```



 

 