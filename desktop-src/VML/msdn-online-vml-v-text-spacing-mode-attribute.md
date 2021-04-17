---
title: LA V-text-modalità di spaziatura (attributo)
description: LA V-text-modalità di spaziatura (attributo)
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474171"
---
# <a name="vml-v-text-spacing-mode-attribute"></a><span data-ttu-id="af814-103">LA V-text-modalità di spaziatura (attributo)</span><span class="sxs-lookup"><span data-stu-id="af814-103">VML V-Text-Spacing-Mode Attribute</span></span>

<span data-ttu-id="af814-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="af814-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af814-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="af814-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af814-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="af814-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af814-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="af814-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af814-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af814-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af814-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af814-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="af814-110">Definisce la modalità per letterSpacing.</span><span class="sxs-lookup"><span data-stu-id="af814-110">Defines the mode for letterspacing.</span></span> <span data-ttu-id="af814-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="af814-111">Read/write.</span></span> <span data-ttu-id="af814-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="af814-112">**String**.</span></span>

<span data-ttu-id="af814-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="af814-113">**Applies To**</span></span>

[<span data-ttu-id="af814-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="af814-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="af814-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="af814-115">**Tag Syntax**</span></span>

<span data-ttu-id="af814-116"><v: *element* Style = "v-text-spaziation-Mode: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="af814-116"><v: *element* style="v-text-spacing-mode: *expression* "></span></span>

<span data-ttu-id="af814-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="af814-117">**Script Syntax**</span></span>

<span data-ttu-id="af814-118">*element* . Style. v-text-spaziatura-modalità = "*espressione*"</span><span class="sxs-lookup"><span data-stu-id="af814-118">*element* .style.v-text-spacing-mode="*expression*"</span></span>

<span data-ttu-id="af814-119">*espressione* = *element*. Style. v-text-modalità spaziatura</span><span class="sxs-lookup"><span data-stu-id="af814-119">*expression*=*element*.style.v-text-spacing-mode</span></span>

<span data-ttu-id="af814-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="af814-120">**Remarks**</span></span>

<span data-ttu-id="af814-121">I valori includono</span><span class="sxs-lookup"><span data-stu-id="af814-121">Values include</span></span>

-   <span data-ttu-id="af814-122">**compattazione** (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af814-122">**tightening** (default)</span></span>
-   <span data-ttu-id="af814-123">**Tracking**</span><span class="sxs-lookup"><span data-stu-id="af814-123">**tracking**</span></span>

<span data-ttu-id="af814-124">Questo attributo determina se lo spazio verrà rimosso tra ogni lettera (stretta) o aggiunta tra ogni lettera (rilevamento).</span><span class="sxs-lookup"><span data-stu-id="af814-124">This attribute determines whether space will be removed between each letter (tightening) or added between each letter (tracking).</span></span> <span data-ttu-id="af814-125">La quantità di modifiche letterSpacing è definita dall'attributo [V-text-spaziatura](msdn-online-vml-v-text-spacing-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="af814-125">The amount of letterspacing change is defined by the [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) attribute.</span></span>

<span data-ttu-id="af814-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="af814-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="af814-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="af814-127">**Example**</span></span>

<span data-ttu-id="af814-128">Il letterSpacing tra ogni lettera viene aumentato di 200 unità.</span><span class="sxs-lookup"><span data-stu-id="af814-128">The letterspacing between each letter is increased by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 