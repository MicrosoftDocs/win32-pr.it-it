---
title: Attributo AutoRotationCenter di la
description: Attributo AutoRotationCenter di la
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624ab3f2c37e043a6d478ca8e422a714a83d157
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728319"
---
# <a name="vml-autorotationcenter-attribute"></a><span data-ttu-id="66e25-103">Attributo AutoRotationCenter di la</span><span class="sxs-lookup"><span data-stu-id="66e25-103">VML AutoRotationCenter Attribute</span></span>

<span data-ttu-id="66e25-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="66e25-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="66e25-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="66e25-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="66e25-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="66e25-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="66e25-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="66e25-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="66e25-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="66e25-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="66e25-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="66e25-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="66e25-110">Determina se il centro della rotazione sarà il centro geometrico dell'estrusione.</span><span class="sxs-lookup"><span data-stu-id="66e25-110">Determines whether the center of rotation will be the geometric center of the extrusion.</span></span> <span data-ttu-id="66e25-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="66e25-111">Read/write.</span></span> <span data-ttu-id="66e25-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="66e25-112">**VgTriState**.</span></span>

<span data-ttu-id="66e25-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="66e25-113">**Applies To**</span></span>

[<span data-ttu-id="66e25-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="66e25-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="66e25-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="66e25-115">**Tag Syntax**</span></span>

<span data-ttu-id="66e25-116"><o: *element* autorotationcenter = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="66e25-116"><o: *element* autorotationcenter=" *expression* "></span></span>

<span data-ttu-id="66e25-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="66e25-117">**Script Syntax**</span></span>

<span data-ttu-id="66e25-118">*element* . autorotationcenter = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="66e25-118">*element* .autorotationcenter="*expression*"</span></span>

<span data-ttu-id="66e25-119">*espressione* = *elemento*. autorotationcenter</span><span class="sxs-lookup"><span data-stu-id="66e25-119">*expression*=*element*.autorotationcenter</span></span>

<span data-ttu-id="66e25-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="66e25-120">**Remarks**</span></span>

<span data-ttu-id="66e25-121">Il centro geometrico di una forma estrusa è 0, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="66e25-121">The geometric center of an extruded shape is 0,0,0.</span></span> <span data-ttu-id="66e25-122">Se il valore di questo attributo è **false**, il centro di rotazione è determinato dall'attributo [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="66e25-122">If the value of this attribute is **False**, the center of rotation is determined by the [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) attribute.</span></span> <span data-ttu-id="66e25-123">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="66e25-123">The default is **False**.</span></span>

<span data-ttu-id="66e25-124">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="66e25-124">*Microsoft Office Extensions Attribute*</span></span>

 

 