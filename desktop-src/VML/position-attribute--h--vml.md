---
title: Attributo position (H) (la)
description: Attributo position (H) (la)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300360"
---
# <a name="position-attribute-hvml"></a><span data-ttu-id="1599e-103">Attributo position (H) (la)</span><span class="sxs-lookup"><span data-stu-id="1599e-103">Position Attribute (H)(VML)</span></span>

<span data-ttu-id="1599e-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1599e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1599e-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="1599e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1599e-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="1599e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1599e-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="1599e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1599e-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1599e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1599e-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1599e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1599e-110">Specifica i valori theX e y dell'handle.</span><span class="sxs-lookup"><span data-stu-id="1599e-110">Specifies thex and y values of the handle.</span></span> <span data-ttu-id="1599e-111">**VgVector2D** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1599e-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="1599e-112">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="1599e-112">**Applies To**</span></span>

<span data-ttu-id="1599e-113">[H](msdn-online-vml-h-element.md) (sottoelemento di [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="1599e-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="1599e-114">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="1599e-114">**Tag Syntax**</span></span>

<span data-ttu-id="1599e-115"><v: *elemento* position = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="1599e-115"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="1599e-116">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="1599e-116">**Remarks**</span></span>

<span data-ttu-id="1599e-117">i valori x e y possono essere di uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1599e-117">x and y values can be one of the following types:</span></span>

-   <span data-ttu-id="1599e-118">constant</span><span class="sxs-lookup"><span data-stu-id="1599e-118">constant</span></span>
-   <span data-ttu-id="1599e-119">Formula (ad esempio, @2 )</span><span class="sxs-lookup"><span data-stu-id="1599e-119">formula (for example, @2)</span></span>
-   <span data-ttu-id="1599e-120">regolare (ad esempio, \# 3)</span><span class="sxs-lookup"><span data-stu-id="1599e-120">adjust (for example, \#3)</span></span>
-   <span data-ttu-id="1599e-121">center</span><span class="sxs-lookup"><span data-stu-id="1599e-121">center</span></span>
-   <span data-ttu-id="1599e-122">TopLeft</span><span class="sxs-lookup"><span data-stu-id="1599e-122">topleft</span></span>
-   <span data-ttu-id="1599e-123">BottomRight</span><span class="sxs-lookup"><span data-stu-id="1599e-123">bottomright</span></span>

<span data-ttu-id="1599e-124">Se viene specificato uno dei tipi precedenti eccetto *Adjust* , la posizione dell'handle è fissa in tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="1599e-124">If any of the above types except *adjust* are specified, the handle position is fixed in that dimension.</span></span> <span data-ttu-id="1599e-125">Se viene specificato un handle di regolazione, l'handle è libero di spostarsi in tale dimensione e il valore di regolazione è determinato dalla posizione dell'handle.</span><span class="sxs-lookup"><span data-stu-id="1599e-125">If an adjust handle is specified, the handle is free to move in that dimension and the adjust value is determined by the position of the handle.</span></span>

<span data-ttu-id="1599e-126">Se viene specificato un attributo [polare](msdn-online-vml-polar-attribute.md) , l'attributo **position** rappresenta il raggio e i valori angolo dell'handle anziché x e y.</span><span class="sxs-lookup"><span data-stu-id="1599e-126">If a [Polar](msdn-online-vml-polar-attribute.md) attribute is specified, the **Position** attribute represents the radius and angle values of the handle instead of x and y.</span></span>

<span data-ttu-id="1599e-127">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="1599e-127">The default value is 0,0.</span></span>

<span data-ttu-id="1599e-128">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="1599e-128">*VML Standard Attribute*</span></span>

 

 