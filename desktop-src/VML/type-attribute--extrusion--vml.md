---
title: Attributo Type (estrusione) (la)
description: Attributo Type (estrusione) (la)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872730"
---
# <a name="type-attribute-extrusionvml"></a><span data-ttu-id="164a1-103">Attributo Type (estrusione) (la)</span><span class="sxs-lookup"><span data-stu-id="164a1-103">Type Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="164a1-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="164a1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="164a1-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="164a1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="164a1-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="164a1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="164a1-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="164a1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="164a1-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="164a1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="164a1-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="164a1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="164a1-110">Definisce il modo in cui viene estrusa la forma.</span><span class="sxs-lookup"><span data-stu-id="164a1-110">Defines the way that the shape is extruded.</span></span> <span data-ttu-id="164a1-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="164a1-111">Read/write.</span></span> <span data-ttu-id="164a1-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="164a1-112">**String**.</span></span>

<span data-ttu-id="164a1-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="164a1-113">**Applies To**</span></span>

[<span data-ttu-id="164a1-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="164a1-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="164a1-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="164a1-115">**Tag Syntax**</span></span>

<span data-ttu-id="164a1-116"><o: tipo di *elemento* = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="164a1-116"><o: *element* type=" *expression* "></span></span>

<span data-ttu-id="164a1-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="164a1-117">**Script Syntax**</span></span>

<span data-ttu-id="164a1-118">*element* . Type = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="164a1-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="164a1-119">*espressione* = *element*. Type</span><span class="sxs-lookup"><span data-stu-id="164a1-119">*expression*=*element*.type</span></span>

<span data-ttu-id="164a1-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="164a1-120">**Remarks**</span></span>

<span data-ttu-id="164a1-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="164a1-121">Values include:</span></span>



| <span data-ttu-id="164a1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="164a1-122">Value</span></span>       | <span data-ttu-id="164a1-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="164a1-123">Description</span></span>                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="164a1-124">parallel</span><span class="sxs-lookup"><span data-stu-id="164a1-124">parallel</span></span>    | <span data-ttu-id="164a1-125">Viene eseguito il rendering dell'estrusione in modo che il centro della proiezione sia infinitamente lontano; in altre termini, le linee di estrusione non sono convergenti, a differenza delle proiezioni prospettiche.</span><span class="sxs-lookup"><span data-stu-id="164a1-125">Extrusion is rendered so that the center of projection is infinitely far away; that is, the extrusion lines do not converge (unlike perspective projections).</span></span> <span data-ttu-id="164a1-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="164a1-126">Default.</span></span> |
| <span data-ttu-id="164a1-127">prospettiva</span><span class="sxs-lookup"><span data-stu-id="164a1-127">perspective</span></span> | <span data-ttu-id="164a1-128">Viene eseguito il rendering dell'estrusione in un centro di proiezione, che corrisponde al punto di dissolvenza per gli oggetti non ruotati.</span><span class="sxs-lookup"><span data-stu-id="164a1-128">Extrusion is rendered to a center of projection, which is the same as the vanishing point for unrotated objects.</span></span>                                                       |



 

<span data-ttu-id="164a1-129">**Attributo Microsoft Office Extensions**</span><span class="sxs-lookup"><span data-stu-id="164a1-129">**Microsoft Office Extensions Attribute**</span></span>

 

 