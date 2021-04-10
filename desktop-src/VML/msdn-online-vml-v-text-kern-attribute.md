---
title: Attributo la V-text-Kern
description: Attributo la V-text-Kern
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963292"
---
# <a name="vml-v-text-kern-attribute"></a><span data-ttu-id="c282c-103">Attributo la V-text-Kern</span><span class="sxs-lookup"><span data-stu-id="c282c-103">VML V-Text-Kern Attribute</span></span>

<span data-ttu-id="c282c-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c282c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c282c-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c282c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c282c-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c282c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c282c-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c282c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c282c-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c282c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c282c-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c282c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c282c-110">Determina se la crenatura è attivata.</span><span class="sxs-lookup"><span data-stu-id="c282c-110">Determines whether kerning is turned on.</span></span> <span data-ttu-id="c282c-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c282c-111">Read/write.</span></span> <span data-ttu-id="c282c-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c282c-112">**VgTriState**.</span></span>

<span data-ttu-id="c282c-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="c282c-113">**Applies To**</span></span>

[<span data-ttu-id="c282c-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="c282c-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="c282c-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="c282c-115">**Tag Syntax**</span></span>

<span data-ttu-id="c282c-116"><v: *elemento* Style = "v-text-Kern: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c282c-116"><v: *element* style="v-text-kern: *expression* "></span></span>

<span data-ttu-id="c282c-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="c282c-117">**Script Syntax**</span></span>

<span data-ttu-id="c282c-118">*element* . Style. v-text-Kern = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="c282c-118">*element* .style.v-text-kern="*expression*"</span></span>

<span data-ttu-id="c282c-119">*espressione* = *element*. Style. v-text-Kern</span><span class="sxs-lookup"><span data-stu-id="c282c-119">*expression*=*element*.style.v-text-kern</span></span>

<span data-ttu-id="c282c-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="c282c-120">**Remarks**</span></span>

<span data-ttu-id="c282c-121">Se **true**, la crenatura è attivata.</span><span class="sxs-lookup"><span data-stu-id="c282c-121">If **True**, the kerning is turned on.</span></span> <span data-ttu-id="c282c-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="c282c-122">The default is **False**.</span></span> <span data-ttu-id="c282c-123">La crenatura è la rimozione dello spazio tra alcune coppie di lettere per compensare i letterforms non uniformi.</span><span class="sxs-lookup"><span data-stu-id="c282c-123">Kerning is the removal of space between certain letter pairs to compensate for uneven letterforms.</span></span> <span data-ttu-id="c282c-124">Ad esempio, se la crenatura è attivata, viene rimosso spazio aggiuntivo tra una "T" maiuscola e una "i" minuscola.</span><span class="sxs-lookup"><span data-stu-id="c282c-124">For example, if kerning is turned on, extra space between a capital "T" and a lowercase "i" would be removed.</span></span>

<span data-ttu-id="c282c-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="c282c-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="c282c-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="c282c-126">**Example**</span></span>

<span data-ttu-id="c282c-127">La crenatura è attivata.</span><span class="sxs-lookup"><span data-stu-id="c282c-127">Kerning is turned on.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 