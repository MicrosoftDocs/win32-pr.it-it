---
title: Attributo GradientShapeOK di la
description: Attributo GradientShapeOK di la
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399629"
---
# <a name="vml-gradientshapeok-attribute"></a><span data-ttu-id="e6055-103">Attributo GradientShapeOK di la</span><span class="sxs-lookup"><span data-stu-id="e6055-103">VML GradientShapeOK Attribute</span></span>

<span data-ttu-id="e6055-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e6055-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e6055-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e6055-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e6055-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e6055-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e6055-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e6055-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e6055-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e6055-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e6055-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e6055-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e6055-110">Determina se un percorso sfumato sarà costituito da percorsi concentrici ripetuti.</span><span class="sxs-lookup"><span data-stu-id="e6055-110">Determines whether a gradient path will be made up of repeated concentric paths.</span></span> <span data-ttu-id="e6055-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e6055-111">Read/write.</span></span> <span data-ttu-id="e6055-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e6055-112">**VgTriState**.</span></span>

<span data-ttu-id="e6055-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e6055-113">**Applies To**</span></span>

[<span data-ttu-id="e6055-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="e6055-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="e6055-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e6055-115">**Tag Syntax**</span></span>

<span data-ttu-id="e6055-116"><v: *element* gradientshapeok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e6055-116"><v: *element* gradientshapeok=" *expression* "></span></span>

<span data-ttu-id="e6055-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e6055-117">**Script Syntax**</span></span>

<span data-ttu-id="e6055-118">*element* . gradientshapeok = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e6055-118">*element* .gradientshapeok="*expression*"</span></span>

<span data-ttu-id="e6055-119">*espressione* = *elemento*. gradientshapeok</span><span class="sxs-lookup"><span data-stu-id="e6055-119">*expression*=*element*.gradientshapeok</span></span>

<span data-ttu-id="e6055-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e6055-120">**Remarks**</span></span>

<span data-ttu-id="e6055-121">Se **true**, il percorso verrà riempito con un riempimento di sfumatura concentrico usando il tracciato come forma ripetuta della sfumatura. Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="e6055-121">If **True**, the path will be filled with a concentric gradient fill using the path as the repeated shape of the gradient.The default is **False**.</span></span>

<span data-ttu-id="e6055-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="e6055-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="e6055-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e6055-123">**Example**</span></span>

<span data-ttu-id="e6055-124">Il percorso verrà riempito con un riempimento sfumato concentrico costituito da rettangoli ripetuti.</span><span class="sxs-lookup"><span data-stu-id="e6055-124">The path will be filled with a concentric gradient fill made up of repeated rectangles.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 