---
title: LA V-rotate-Letters (attributo)
description: LA V-rotate-Letters (attributo)
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117819"
---
# <a name="vml-v-rotate-letters-attribute"></a><span data-ttu-id="a46e8-103">LA V-rotate-Letters (attributo)</span><span class="sxs-lookup"><span data-stu-id="a46e8-103">VML V-Rotate-Letters Attribute</span></span>

<span data-ttu-id="a46e8-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a46e8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a46e8-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a46e8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a46e8-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a46e8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a46e8-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a46e8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a46e8-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a46e8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a46e8-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a46e8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a46e8-110">Determina se le lettere del testo vengono ruotate.</span><span class="sxs-lookup"><span data-stu-id="a46e8-110">Determines whether the letters of the text are rotated.</span></span> <span data-ttu-id="a46e8-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a46e8-111">Read/write.</span></span> <span data-ttu-id="a46e8-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a46e8-112">**VgTriState**.</span></span>

<span data-ttu-id="a46e8-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="a46e8-113">**Applies To**</span></span>

[<span data-ttu-id="a46e8-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="a46e8-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="a46e8-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="a46e8-115">**Tag Syntax**</span></span>

<span data-ttu-id="a46e8-116"><v: *elemento* Style = "v-rotate-Letters: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a46e8-116"><v: *element* style="v-rotate-letters: *expression* "></span></span>

<span data-ttu-id="a46e8-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="a46e8-117">**Script Syntax**</span></span>

<span data-ttu-id="a46e8-118">*element* . Style. v-rotate-Letters = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="a46e8-118">*element* .style.v-rotate-letters="*expression*"</span></span>

<span data-ttu-id="a46e8-119">*espressione* = *element*. Style. v-rotate-lettere</span><span class="sxs-lookup"><span data-stu-id="a46e8-119">*expression*=*element*.style.v-rotate-letters</span></span>

<span data-ttu-id="a46e8-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="a46e8-120">**Remarks**</span></span>

<span data-ttu-id="a46e8-121">Se **true**, le lettere del testo vengono ruotate di 90 gradi.</span><span class="sxs-lookup"><span data-stu-id="a46e8-121">If **True**, the letters of the text are rotated 90 degrees.</span></span> <span data-ttu-id="a46e8-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="a46e8-122">The default value is **False**.</span></span>

<span data-ttu-id="a46e8-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="a46e8-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="a46e8-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="a46e8-124">**Example**</span></span>

<span data-ttu-id="a46e8-125">Le lettere vengono ruotate di 90 gradi.</span><span class="sxs-lookup"><span data-stu-id="a46e8-125">The letters are rotated 90 degrees.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 