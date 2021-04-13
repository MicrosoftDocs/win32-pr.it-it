---
title: Attributo ArrowOK di la
description: Attributo ArrowOK di la
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399253"
---
# <a name="vml-arrowok-attribute"></a><span data-ttu-id="a2f8e-103">Attributo ArrowOK di la</span><span class="sxs-lookup"><span data-stu-id="a2f8e-103">VML ArrowOK Attribute</span></span>

<span data-ttu-id="a2f8e-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a2f8e-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a2f8e-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a2f8e-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a2f8e-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a2f8e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a2f8e-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a2f8e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a2f8e-110">Determina se le frecce verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-110">Determines whether arrowheads will be displayed.</span></span> <span data-ttu-id="a2f8e-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-111">Read/write.</span></span> <span data-ttu-id="a2f8e-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-112">**VgTriState**.</span></span>

<span data-ttu-id="a2f8e-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="a2f8e-113">**Applies To**</span></span>

[<span data-ttu-id="a2f8e-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="a2f8e-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="a2f8e-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="a2f8e-115">**Tag Syntax**</span></span>

<span data-ttu-id="a2f8e-116"><v: *element* arrowok = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="a2f8e-116"><v: *element* arrowok=" *expression* "></span></span>

<span data-ttu-id="a2f8e-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="a2f8e-117">**Script Syntax**</span></span>

<span data-ttu-id="a2f8e-118">*element* . arrowok = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="a2f8e-118">*element* .arrowok="*expression*"</span></span>

<span data-ttu-id="a2f8e-119">*espressione* = *elemento*. arrowok</span><span class="sxs-lookup"><span data-stu-id="a2f8e-119">*expression*=*element*.arrowok</span></span>

<span data-ttu-id="a2f8e-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="a2f8e-120">**Remarks**</span></span>

<span data-ttu-id="a2f8e-121">Se **false**, il percorso non avrà frecce.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-121">If **False**, the path will not have arrowheads.</span></span> <span data-ttu-id="a2f8e-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-122">The default is **False**.</span></span> <span data-ttu-id="a2f8e-123">Questo attributo esegue l'override di tutti gli altri attributi della freccia nell'elemento padre o **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="a2f8e-123">This attribute overrides all other arrowhead attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="a2f8e-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="a2f8e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a2f8e-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="a2f8e-125">**Example**</span></span>

<span data-ttu-id="a2f8e-126">Il percorso non avrà una freccia.</span><span class="sxs-lookup"><span data-stu-id="a2f8e-126">The path will not have an arrowhead.</span></span>


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 