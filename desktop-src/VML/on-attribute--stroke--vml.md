---
title: Attributo on (Stroke) (la)
description: Attributo on (Stroke) (la)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300137"
---
# <a name="on-attribute-strokevml"></a><span data-ttu-id="e926b-103">Attributo on (Stroke) (la)</span><span class="sxs-lookup"><span data-stu-id="e926b-103">On Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="e926b-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e926b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e926b-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e926b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e926b-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e926b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e926b-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e926b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e926b-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e926b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e926b-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e926b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e926b-110">Determina se il tratto verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e926b-110">Determines whether the stroke will be displayed.</span></span> <span data-ttu-id="e926b-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e926b-111">Read/write.</span></span> <span data-ttu-id="e926b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e926b-112">**VgTriState**.</span></span>

<span data-ttu-id="e926b-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e926b-113">**Applies To**</span></span>

[<span data-ttu-id="e926b-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="e926b-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="e926b-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e926b-115">**Tag Syntax**</span></span>

<span data-ttu-id="e926b-116"><v: *element* on = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e926b-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="e926b-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e926b-117">**Script Syntax**</span></span>

<span data-ttu-id="e926b-118">*element* . on = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e926b-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="e926b-119">*espressione* = *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="e926b-119">*expression*=*element*.on</span></span>

<span data-ttu-id="e926b-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e926b-120">**Remarks**</span></span>

<span data-ttu-id="e926b-121">Se **false**, il tratto non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e926b-121">If **False**, the stroke is not displayed.</span></span> <span data-ttu-id="e926b-122">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="e926b-122">The default is **True**.</span></span>

<span data-ttu-id="e926b-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="e926b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="e926b-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e926b-124">**Example**</span></span>

<span data-ttu-id="e926b-125">Il tratto non verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e926b-125">The stroke will not be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 