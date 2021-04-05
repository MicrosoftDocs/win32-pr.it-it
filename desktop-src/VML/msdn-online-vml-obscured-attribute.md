---
title: LA-attributo oscurato
description: LA-attributo oscurato
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046948"
---
# <a name="vml-obscured-attribute"></a><span data-ttu-id="622e1-103">LA-attributo oscurato</span><span class="sxs-lookup"><span data-stu-id="622e1-103">VML Obscured Attribute</span></span>

<span data-ttu-id="622e1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="622e1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="622e1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="622e1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="622e1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="622e1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="622e1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="622e1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="622e1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="622e1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="622e1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="622e1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="622e1-110">Determina se un'ombreggiatura è trasparente.</span><span class="sxs-lookup"><span data-stu-id="622e1-110">Determines whether a shadow is transparent.</span></span> <span data-ttu-id="622e1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="622e1-111">Read/write.</span></span> <span data-ttu-id="622e1-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="622e1-112">**VgTriState**.</span></span>

<span data-ttu-id="622e1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="622e1-113">**Applies To**</span></span>

[<span data-ttu-id="622e1-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="622e1-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="622e1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="622e1-115">**Tag Syntax**</span></span>

<span data-ttu-id="622e1-116"><v: *element* Obscured = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="622e1-116"><v: *element* obscured=" *expression* "></span></span>

<span data-ttu-id="622e1-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="622e1-117">**Script Syntax**</span></span>

<span data-ttu-id="622e1-118">*element* . Obscured = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="622e1-118">*element* .obscured="*expression*"</span></span>

<span data-ttu-id="622e1-119">*espressione* = *elemento*. Obscured</span><span class="sxs-lookup"><span data-stu-id="622e1-119">*expression*=*element*.obscured</span></span>

<span data-ttu-id="622e1-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="622e1-120">**Remarks**</span></span>

<span data-ttu-id="622e1-121">Se **true**, consente di visualizzare l'ombreggiatura se non è presente alcun riempimento della forma.</span><span class="sxs-lookup"><span data-stu-id="622e1-121">If **True**, lets you see through the shadow if there is no fill on the shape.</span></span> <span data-ttu-id="622e1-122">L'impostazione predefinita è **False**.</span><span class="sxs-lookup"><span data-stu-id="622e1-122">Default is **False**.</span></span>

<span data-ttu-id="622e1-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="622e1-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="622e1-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="622e1-124">**Example**</span></span>

<span data-ttu-id="622e1-125">Lo sfondo viene visualizzato attraverso l'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="622e1-125">The background shows through the shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 