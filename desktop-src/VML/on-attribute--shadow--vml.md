---
title: Attributo on (Shadow) (la)
description: Attributo on (Shadow) (la)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963291"
---
# <a name="on-attribute-shadowvml"></a><span data-ttu-id="89fac-103">Attributo on (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="89fac-103">On Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="89fac-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="89fac-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="89fac-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="89fac-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="89fac-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="89fac-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="89fac-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="89fac-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="89fac-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="89fac-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="89fac-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="89fac-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="89fac-110">Determina se verrà visualizzata un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="89fac-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="89fac-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="89fac-111">Read/write.</span></span> <span data-ttu-id="89fac-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="89fac-112">**VgTriState**.</span></span>

<span data-ttu-id="89fac-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="89fac-113">**Applies To**</span></span>

[<span data-ttu-id="89fac-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="89fac-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="89fac-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="89fac-115">**Tag Syntax**</span></span>

<span data-ttu-id="89fac-116"><v: *element* on = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="89fac-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="89fac-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="89fac-117">**Script Syntax**</span></span>

<span data-ttu-id="89fac-118">*element* . on = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="89fac-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="89fac-119">*espressione* = *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="89fac-119">*expression*=*element*.on</span></span>

<span data-ttu-id="89fac-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="89fac-120">**Remarks**</span></span>

<span data-ttu-id="89fac-121">Se **true**, verrà visualizzata l'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="89fac-121">If **True**, the shadow will be displayed.</span></span> <span data-ttu-id="89fac-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="89fac-122">The default value is **False**.</span></span>

<span data-ttu-id="89fac-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="89fac-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="89fac-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="89fac-124">**Example**</span></span>

<span data-ttu-id="89fac-125">Verrà visualizzata l'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="89fac-125">The shadow will be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 