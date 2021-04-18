---
title: Attributo LockRotationCenter di la
description: Attributo LockRotationCenter di la
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300320"
---
# <a name="vml-lockrotationcenter-attribute"></a><span data-ttu-id="96e95-103">Attributo LockRotationCenter di la</span><span class="sxs-lookup"><span data-stu-id="96e95-103">VML LockRotationCenter Attribute</span></span>

<span data-ttu-id="96e95-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="96e95-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="96e95-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="96e95-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="96e95-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="96e95-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="96e95-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="96e95-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="96e95-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="96e95-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="96e95-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="96e95-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="96e95-110">Determina se la rotazione dell'oggetto estruso è specificata dall'attributo [RotationAngle](msdn-online-vml-rotationangle-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="96e95-110">Determines whether the rotation of the extruded object is specified by the [RotationAngle](msdn-online-vml-rotationangle-attribute.md) attribute.</span></span> <span data-ttu-id="96e95-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="96e95-111">Read/write.</span></span> <span data-ttu-id="96e95-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="96e95-112">**VgTriState**.</span></span>

<span data-ttu-id="96e95-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="96e95-113">**Applies To**</span></span>

[<span data-ttu-id="96e95-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="96e95-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="96e95-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="96e95-115">**Tag Syntax**</span></span>

<span data-ttu-id="96e95-116"><o: *element* lockrotationcenter = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="96e95-116"><o: *element* lockrotationcenter=" *expression* "></span></span>

<span data-ttu-id="96e95-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="96e95-117">**Script Syntax**</span></span>

<span data-ttu-id="96e95-118">*element* . lockrotationcenter = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="96e95-118">*element* .lockrotationcenter="*expression*"</span></span>

<span data-ttu-id="96e95-119">*espressione* = *elemento*. lockrotationcenter</span><span class="sxs-lookup"><span data-stu-id="96e95-119">*expression*=*element*.lockrotationcenter</span></span>

<span data-ttu-id="96e95-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="96e95-120">**Remarks**</span></span>

<span data-ttu-id="96e95-121">Se **false**, la rotazione viene specificata dall'attributo [Orientation](msdn-online-vml-orientation-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="96e95-121">If **False**, the rotation is specified by the [Orientation](msdn-online-vml-orientation-attribute.md) attribute.</span></span> <span data-ttu-id="96e95-122">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="96e95-122">The default is **True**.</span></span>

<span data-ttu-id="96e95-123">Tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="96e95-123">Note that:</span></span>


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



<span data-ttu-id="96e95-124">è lo stesso di:</span><span class="sxs-lookup"><span data-stu-id="96e95-124">is the same as:</span></span>


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



<span data-ttu-id="96e95-125">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="96e95-125">*Microsoft Office Extensions Attribute*</span></span>

 

 