---
title: Attributo ViewpointOrigin di la
description: Attributo ViewpointOrigin di la
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473387"
---
# <a name="vml-viewpointorigin-attribute"></a><span data-ttu-id="d411f-103">Attributo ViewpointOrigin di la</span><span class="sxs-lookup"><span data-stu-id="d411f-103">VML ViewpointOrigin Attribute</span></span>

<span data-ttu-id="d411f-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d411f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d411f-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d411f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d411f-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d411f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d411f-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d411f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d411f-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d411f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d411f-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d411f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d411f-110">Definisce l'origine del punto di vista all'interno del rettangolo di delimitazione della forma.</span><span class="sxs-lookup"><span data-stu-id="d411f-110">Defines the origin of the viewpoint within the bounding box of the shape.</span></span> <span data-ttu-id="d411f-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d411f-111">Read/write.</span></span> <span data-ttu-id="d411f-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="d411f-112">**VgVector2D**.</span></span>

<span data-ttu-id="d411f-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d411f-113">**Applies To**</span></span>

[<span data-ttu-id="d411f-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="d411f-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="d411f-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d411f-115">**Tag Syntax**</span></span>

<span data-ttu-id="d411f-116"><o: *element* viewpointorigin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d411f-116"><o: *element* viewpointorigin=" *expression* "></span></span>

<span data-ttu-id="d411f-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d411f-117">**Script Syntax**</span></span>

<span data-ttu-id="d411f-118">*element* . viewpointorigin = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d411f-118">*element* .viewpointorigin="*expression*"</span></span>

<span data-ttu-id="d411f-119">*espressione* = *elemento*. viewpointorigin</span><span class="sxs-lookup"><span data-stu-id="d411f-119">*expression*=*element*.viewpointorigin</span></span>

<span data-ttu-id="d411f-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d411f-120">**Remarks**</span></span>

<span data-ttu-id="d411f-121">Definisce il punto di vista in termini di valori x e y della forma originale.</span><span class="sxs-lookup"><span data-stu-id="d411f-121">Defines the viewpoint in terms of the x and y values of the original shape.</span></span> <span data-ttu-id="d411f-122">I valori x e y sono compresi tra 0,5 e-0,5 (da 50% a-50% dell'origine della coordinata della forma).</span><span class="sxs-lookup"><span data-stu-id="d411f-122">The x and y values range from 0.5 to -0.5 (50% to -50% of the shape's coordinate origin).</span></span> <span data-ttu-id="d411f-123">Il valore predefinito è 0, 0.</span><span class="sxs-lookup"><span data-stu-id="d411f-123">The default is 0,0.</span></span>

<span data-ttu-id="d411f-124">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="d411f-124">*Microsoft Office Extensions Attribute*</span></span>

 

 