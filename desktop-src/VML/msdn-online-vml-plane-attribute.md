---
title: Attributo piano la
description: Attributo piano la
ms.assetid: e1de630b-8e25-4052-b316-251046f73e98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f279f008adf8f12f78d6edd790cc533678adc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963183"
---
# <a name="vml-plane-attribute"></a><span data-ttu-id="d4da9-103">Attributo piano la</span><span class="sxs-lookup"><span data-stu-id="d4da9-103">VML Plane Attribute</span></span>

<span data-ttu-id="d4da9-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d4da9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d4da9-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d4da9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d4da9-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d4da9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d4da9-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d4da9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d4da9-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d4da9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d4da9-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d4da9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d4da9-110">Specifica il piano che si trova negli angoli destro dell'estrusione.</span><span class="sxs-lookup"><span data-stu-id="d4da9-110">Specifies the plane that is at right angles to the extrusion.</span></span> <span data-ttu-id="d4da9-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d4da9-111">Read/write.</span></span> <span data-ttu-id="d4da9-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="d4da9-112">**String**.</span></span>

<span data-ttu-id="d4da9-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d4da9-113">**Applies To**</span></span>

[<span data-ttu-id="d4da9-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="d4da9-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="d4da9-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d4da9-115">**Tag Syntax**</span></span>

<span data-ttu-id="d4da9-116"><o: *element* Plane = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d4da9-116"><o: *element* plane=" *expression* "></span></span>

<span data-ttu-id="d4da9-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d4da9-117">**Script Syntax**</span></span>

<span data-ttu-id="d4da9-118">*element* . plane = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d4da9-118">*element* .plane="*expression*"</span></span>

<span data-ttu-id="d4da9-119">*espressione* = *element*. Plane</span><span class="sxs-lookup"><span data-stu-id="d4da9-119">*expression*=*element*.plane</span></span>

<span data-ttu-id="d4da9-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d4da9-120">**Remarks**</span></span>

<span data-ttu-id="d4da9-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="d4da9-121">Values include:</span></span>



| <span data-ttu-id="d4da9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d4da9-122">Value</span></span> | <span data-ttu-id="d4da9-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4da9-123">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="d4da9-124">xy</span><span class="sxs-lookup"><span data-stu-id="d4da9-124">xy</span></span>    | <span data-ttu-id="d4da9-125">L'estrusione è ad angolo retto rispetto al piano XY.</span><span class="sxs-lookup"><span data-stu-id="d4da9-125">Extrusion is at right angles to the xy -plane.</span></span> <span data-ttu-id="d4da9-126">Predefinito</span><span class="sxs-lookup"><span data-stu-id="d4da9-126">Default</span></span> |
| <span data-ttu-id="d4da9-127">ZX</span><span class="sxs-lookup"><span data-stu-id="d4da9-127">zx</span></span>    | <span data-ttu-id="d4da9-128">L'estrusione è ad angolo retto rispetto alla ZX-Plane.</span><span class="sxs-lookup"><span data-stu-id="d4da9-128">Extrusion is at right angles to the zx -plane.</span></span>         |
| <span data-ttu-id="d4da9-129">YZ</span><span class="sxs-lookup"><span data-stu-id="d4da9-129">yz</span></span>    | <span data-ttu-id="d4da9-130">L'estrusione è ad angolo retto del piano YZ.</span><span class="sxs-lookup"><span data-stu-id="d4da9-130">Extrusion is at right angles to the yz -plane.</span></span>         |



 

<span data-ttu-id="d4da9-131">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="d4da9-131">*Microsoft Office Extensions Attribute*</span></span>

 

 