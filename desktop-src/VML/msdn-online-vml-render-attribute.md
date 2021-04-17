---
title: Attributo render la
description: Attributo render la
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300194"
---
# <a name="vml-render-attribute"></a><span data-ttu-id="8703b-103">Attributo render la</span><span class="sxs-lookup"><span data-stu-id="8703b-103">VML Render Attribute</span></span>

<span data-ttu-id="8703b-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8703b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8703b-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="8703b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8703b-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="8703b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8703b-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="8703b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8703b-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8703b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8703b-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8703b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8703b-110">Definisce la modalità di rendering dell'estrusione.</span><span class="sxs-lookup"><span data-stu-id="8703b-110">Defines the rendering mode of the extrusion.</span></span> <span data-ttu-id="8703b-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8703b-111">Read/write.</span></span> <span data-ttu-id="8703b-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="8703b-112">**String**.</span></span>

<span data-ttu-id="8703b-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="8703b-113">**Applies To**</span></span>

[<span data-ttu-id="8703b-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="8703b-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="8703b-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="8703b-115">**Tag Syntax**</span></span>

<span data-ttu-id="8703b-116"><o: *elemento* render = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="8703b-116"><o: *element* render=" *expression* "></span></span>

<span data-ttu-id="8703b-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="8703b-117">**Script Syntax**</span></span>

<span data-ttu-id="8703b-118">*element* . Render = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="8703b-118">*element* .render="*expression*"</span></span>

<span data-ttu-id="8703b-119">*espressione* = *elemento*. Render</span><span class="sxs-lookup"><span data-stu-id="8703b-119">*expression*=*element*.render</span></span>

<span data-ttu-id="8703b-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="8703b-120">**Remarks**</span></span>

<span data-ttu-id="8703b-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="8703b-121">Values include:</span></span>



| <span data-ttu-id="8703b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8703b-122">Value</span></span>        | <span data-ttu-id="8703b-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8703b-123">Description</span></span>                                                   |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="8703b-124">solido</span><span class="sxs-lookup"><span data-stu-id="8703b-124">solid</span></span>        | <span data-ttu-id="8703b-125">Il rendering Visualizza una forma a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="8703b-125">Rendering displays a solid shape.</span></span> <span data-ttu-id="8703b-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8703b-126">Default.</span></span>                    |
| <span data-ttu-id="8703b-127">wireframe</span><span class="sxs-lookup"><span data-stu-id="8703b-127">wireframe</span></span>    | <span data-ttu-id="8703b-128">Il rendering Visualizza una forma wireframe.</span><span class="sxs-lookup"><span data-stu-id="8703b-128">Rendering displays a wireframe shape.</span></span>                         |
| <span data-ttu-id="8703b-129">boundingcube</span><span class="sxs-lookup"><span data-stu-id="8703b-129">boundingcube</span></span> | <span data-ttu-id="8703b-130">Rendering consente di visualizzare il cubo delimitatore che contiene la forma.</span><span class="sxs-lookup"><span data-stu-id="8703b-130">Rendering displays the bounding cube that contains the shape.</span></span> |



 

<span data-ttu-id="8703b-131">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="8703b-131">*Microsoft Office Extensions Attribute*</span></span>

 

 