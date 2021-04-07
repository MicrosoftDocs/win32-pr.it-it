---
title: LA trim-attributo
description: LA trim-attributo
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f7aa2ce17d5b2b8df772954cee323e3d5ea2db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872882"
---
# <a name="vml-trim-attribute"></a><span data-ttu-id="2f15e-103">LA trim-attributo</span><span class="sxs-lookup"><span data-stu-id="2f15e-103">VML Trim Attribute</span></span>

<span data-ttu-id="2f15e-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2f15e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2f15e-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="2f15e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2f15e-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="2f15e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2f15e-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="2f15e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2f15e-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2f15e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2f15e-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2f15e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2f15e-110">Determina se lo spazio aggiuntivo viene rimosso sopra e sotto il testo.</span><span class="sxs-lookup"><span data-stu-id="2f15e-110">Determines whether extra space is removed above and below the text.</span></span> <span data-ttu-id="2f15e-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2f15e-111">Read/write.</span></span> <span data-ttu-id="2f15e-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="2f15e-112">**VgTriState**.</span></span>

<span data-ttu-id="2f15e-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="2f15e-113">**Applies To**</span></span>

[<span data-ttu-id="2f15e-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="2f15e-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="2f15e-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="2f15e-115">**Tag Syntax**</span></span>

<span data-ttu-id="2f15e-116"><v: *elemento* Style = "Trim: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="2f15e-116"><v: *element* style="trim: *expression* "></span></span>

<span data-ttu-id="2f15e-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="2f15e-117">**Script Syntax**</span></span>

<span data-ttu-id="2f15e-118">*element* . Style. Trim = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="2f15e-118">*element* .style.trim="*expression*"</span></span>

<span data-ttu-id="2f15e-119">*espressione* = *element*. Style. Trim</span><span class="sxs-lookup"><span data-stu-id="2f15e-119">*expression*=*element*.style.trim</span></span>

<span data-ttu-id="2f15e-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="2f15e-120">**Remarks**</span></span>

<span data-ttu-id="2f15e-121">Se **true**, lo spazio riservato per gli elementi ascenders e Descendants viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="2f15e-121">If **True**, space reserved for ascenders and descenders is removed.</span></span> <span data-ttu-id="2f15e-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="2f15e-122">The default value is **False**.</span></span>

<span data-ttu-id="2f15e-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="2f15e-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="2f15e-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="2f15e-124">**Example**</span></span>

<span data-ttu-id="2f15e-125">Lo spazio aggiuntivo sopra e sotto viene tagliato.</span><span class="sxs-lookup"><span data-stu-id="2f15e-125">The extra space above and below is trimmed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 