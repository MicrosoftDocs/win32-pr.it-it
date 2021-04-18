---
title: Attributo UserHidden di la
description: Attributo UserHidden di la
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 519857d53cbec985afae31a5e7dea8811773dc43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299918"
---
# <a name="vml-userhidden-attribute"></a><span data-ttu-id="c56b1-103">Attributo UserHidden di la</span><span class="sxs-lookup"><span data-stu-id="c56b1-103">VML UserHidden Attribute</span></span>

<span data-ttu-id="c56b1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c56b1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c56b1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c56b1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c56b1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c56b1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c56b1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="c56b1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c56b1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c56b1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c56b1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c56b1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c56b1-110">Determina se un ancoraggio di script è nascosto.</span><span class="sxs-lookup"><span data-stu-id="c56b1-110">Determines whether a script anchor is hidden.</span></span> <span data-ttu-id="c56b1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c56b1-111">Read/write.</span></span> <span data-ttu-id="c56b1-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c56b1-112">**VgTriState**.</span></span>

<span data-ttu-id="c56b1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="c56b1-113">**Applies To**</span></span>

[<span data-ttu-id="c56b1-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="c56b1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c56b1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="c56b1-115">**Tag Syntax**</span></span>

<span data-ttu-id="c56b1-116"><v: *element* o:userhidden = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="c56b1-116"><v: *element* o:userhidden=" *expression* "></span></span>

<span data-ttu-id="c56b1-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="c56b1-117">**Remarks**</span></span>

<span data-ttu-id="c56b1-118">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="c56b1-118">The default is **False**.</span></span> <span data-ttu-id="c56b1-119">Se **true**, gli ancoraggi degli script rimaneno nascosti anche se la forma è altrimenti visibile.</span><span class="sxs-lookup"><span data-stu-id="c56b1-119">If **True**, script anchors stay hidden even if the shape is otherwise visible.</span></span>

<span data-ttu-id="c56b1-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="c56b1-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="c56b1-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="c56b1-121">**Example**</span></span>

<span data-ttu-id="c56b1-122">L'ancoraggio dello script della forma è nascosto.</span><span class="sxs-lookup"><span data-stu-id="c56b1-122">The script anchor of the shape is hidden.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 