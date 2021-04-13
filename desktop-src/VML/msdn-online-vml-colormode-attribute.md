---
title: Attributo ColorMode di la
description: Attributo ColorMode di la
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399241"
---
# <a name="vml-colormode-attribute"></a><span data-ttu-id="1beb9-103">Attributo ColorMode di la</span><span class="sxs-lookup"><span data-stu-id="1beb9-103">VML ColorMode Attribute</span></span>

<span data-ttu-id="1beb9-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1beb9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1beb9-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="1beb9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1beb9-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="1beb9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1beb9-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="1beb9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1beb9-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1beb9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1beb9-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1beb9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1beb9-110">Determina la modalità di colore dell'estrusione.</span><span class="sxs-lookup"><span data-stu-id="1beb9-110">Determines the mode of extrusion color.</span></span> <span data-ttu-id="1beb9-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1beb9-111">Read/write.</span></span> <span data-ttu-id="1beb9-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="1beb9-112">**VgTriState**.</span></span>

<span data-ttu-id="1beb9-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="1beb9-113">**Applies To**</span></span>

[<span data-ttu-id="1beb9-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="1beb9-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="1beb9-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="1beb9-115">**Tag Syntax**</span></span>

<span data-ttu-id="1beb9-116"><o: *element* ColorMode = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="1beb9-116"><o: *element* colormode=" *expression* "></span></span>

<span data-ttu-id="1beb9-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="1beb9-117">**Script Syntax**</span></span>

<span data-ttu-id="1beb9-118">*element* . ColorMode = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="1beb9-118">*element* .colormode="*expression*"</span></span>

<span data-ttu-id="1beb9-119">*espressione* = *elemento*. ColorMode</span><span class="sxs-lookup"><span data-stu-id="1beb9-119">*expression*=*element*.colormode</span></span>

<span data-ttu-id="1beb9-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="1beb9-120">**Remarks**</span></span>

<span data-ttu-id="1beb9-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="1beb9-121">Values include:</span></span>



| <span data-ttu-id="1beb9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1beb9-122">Value</span></span>  | <span data-ttu-id="1beb9-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1beb9-123">Description</span></span>                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1beb9-124">auto</span><span class="sxs-lookup"><span data-stu-id="1beb9-124">auto</span></span>   | <span data-ttu-id="1beb9-125">Specifica che il colore dell'estrusione è uguale al colore di riempimento della forma.</span><span class="sxs-lookup"><span data-stu-id="1beb9-125">Specifies that the color of the extrusion is the same as the fill color of the shape.</span></span> <span data-ttu-id="1beb9-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="1beb9-126">Default.</span></span>                |
| <span data-ttu-id="1beb9-127">custom</span><span class="sxs-lookup"><span data-stu-id="1beb9-127">custom</span></span> | <span data-ttu-id="1beb9-128">Specifica che l'estrusione sarà il colore dell'attributo [color](color-attribute--extrusion--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="1beb9-128">Specifies that the extrusion will be the color of the [Color](color-attribute--extrusion--vml.md) attribute.</span></span> |



 

<span data-ttu-id="1beb9-129">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="1beb9-129">*Microsoft Office Extensions Attribute*</span></span>

 

 