---
title: Attributo la V-text-spaziatura
description: Attributo la V-text-spaziatura
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399375"
---
# <a name="vml-v-text-spacing-attribute"></a><span data-ttu-id="4ff99-103">Attributo la V-text-spaziatura</span><span class="sxs-lookup"><span data-stu-id="4ff99-103">VML V-Text-Spacing Attribute</span></span>

<span data-ttu-id="4ff99-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4ff99-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4ff99-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="4ff99-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4ff99-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="4ff99-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4ff99-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="4ff99-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4ff99-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4ff99-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4ff99-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4ff99-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4ff99-110">Definisce la quantità di spaziatura per il testo.</span><span class="sxs-lookup"><span data-stu-id="4ff99-110">Defines the amount of spacing for text.</span></span> <span data-ttu-id="4ff99-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4ff99-111">Read/write.</span></span> <span data-ttu-id="4ff99-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="4ff99-112">**VgNumber**.</span></span>

<span data-ttu-id="4ff99-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="4ff99-113">**Applies To**</span></span>

[<span data-ttu-id="4ff99-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="4ff99-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="4ff99-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="4ff99-115">**Tag Syntax**</span></span>

<span data-ttu-id="4ff99-116"><v: *elemento* Style = "v-text-spaziation: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="4ff99-116"><v: *element* style="v-text-spacing: *expression* "></span></span>

<span data-ttu-id="4ff99-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="4ff99-117">**Script Syntax**</span></span>

<span data-ttu-id="4ff99-118">*element* . Style. v-text-spaziation = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="4ff99-118">*element* .style.v-text-spacing="*expression*"</span></span>

<span data-ttu-id="4ff99-119">*espressione* = *elemento*. Style. v-spaziatura testo</span><span class="sxs-lookup"><span data-stu-id="4ff99-119">*expression*=*element*.style.v-text-spacing</span></span>

<span data-ttu-id="4ff99-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="4ff99-120">**Remarks**</span></span>

<span data-ttu-id="4ff99-121">Il valore predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="4ff99-121">The default value is 100.</span></span> <span data-ttu-id="4ff99-122">Per ulteriori informazioni sulla spaziatura del testo, vedere l'attributo [V-text-spaziation-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4ff99-122">See the [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) attribute for more information about text spacing.</span></span>

<span data-ttu-id="4ff99-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="4ff99-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="4ff99-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="4ff99-124">**Example**</span></span>

<span data-ttu-id="4ff99-125">Il letterSpacing tra ogni lettera viene ristretto di 200 unità.</span><span class="sxs-lookup"><span data-stu-id="4ff99-125">The letterspacing between each letter is tightened by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 