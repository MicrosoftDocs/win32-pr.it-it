---
title: Attributo on (Fill) (la)
description: Attributo on (Fill) (la)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e25e805be23b4678b1be828b711365a8624f10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300312"
---
# <a name="on-attribute-fillvml"></a><span data-ttu-id="3f442-103">Attributo on (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="3f442-103">On Attribute (Fill)(VML)</span></span>

<span data-ttu-id="3f442-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3f442-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3f442-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3f442-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3f442-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3f442-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3f442-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3f442-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3f442-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3f442-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3f442-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3f442-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3f442-110">Determina se verrà visualizzato il riempimento.</span><span class="sxs-lookup"><span data-stu-id="3f442-110">Determines whether the fill will be displayed.</span></span> <span data-ttu-id="3f442-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3f442-111">Read/write.</span></span> <span data-ttu-id="3f442-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="3f442-112">**VgTriState**.</span></span>

<span data-ttu-id="3f442-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="3f442-113">**Applies To**</span></span>

[<span data-ttu-id="3f442-114">Fill</span><span class="sxs-lookup"><span data-stu-id="3f442-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="3f442-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="3f442-115">**Tag Syntax**</span></span>

<span data-ttu-id="3f442-116"><v: *element* on = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3f442-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="3f442-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="3f442-117">**Script Syntax**</span></span>

<span data-ttu-id="3f442-118">*element* . on = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="3f442-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="3f442-119">*espressione* = *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="3f442-119">*expression*=*element*.on</span></span>

<span data-ttu-id="3f442-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="3f442-120">**Remarks**</span></span>

<span data-ttu-id="3f442-121">Se **false**, il riempimento non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3f442-121">If **False**, the fill is not displayed.</span></span> <span data-ttu-id="3f442-122">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="3f442-122">The default is **True**.</span></span>

<span data-ttu-id="3f442-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="3f442-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3f442-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="3f442-124">**Example**</span></span>

<span data-ttu-id="3f442-125">Anche se il riempimento è definito come rosso, non viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3f442-125">Even though the fill is defined to be red, it is not displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 