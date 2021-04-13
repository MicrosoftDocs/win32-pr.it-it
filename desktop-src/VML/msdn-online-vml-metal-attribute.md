---
title: Attributo Metal la
description: Attributo Metal la
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399064"
---
# <a name="vml-metal-attribute"></a><span data-ttu-id="e606f-103">Attributo Metal la</span><span class="sxs-lookup"><span data-stu-id="e606f-103">VML Metal Attribute</span></span>

<span data-ttu-id="e606f-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e606f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e606f-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e606f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e606f-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e606f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e606f-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e606f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e606f-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e606f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e606f-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e606f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e606f-110">Determina se la superficie della forma estrusa sarà simile a metal.</span><span class="sxs-lookup"><span data-stu-id="e606f-110">Determines whether the surface of the extruded shape will resemble metal.</span></span> <span data-ttu-id="e606f-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e606f-111">Read/write.</span></span> <span data-ttu-id="e606f-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e606f-112">**VgTriState**.</span></span>

<span data-ttu-id="e606f-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e606f-113">**Applies To**</span></span>

[<span data-ttu-id="e606f-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="e606f-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="e606f-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e606f-115">**Tag Syntax**</span></span>

<span data-ttu-id="e606f-116"><o: *element* Metal = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e606f-116"><o: *element* metal=" *expression* "></span></span>

<span data-ttu-id="e606f-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e606f-117">**Script Syntax**</span></span>

<span data-ttu-id="e606f-118">*element* . metal = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e606f-118">*element* .metal="*expression*"</span></span>

<span data-ttu-id="e606f-119">*espressione* = *element*. Metal</span><span class="sxs-lookup"><span data-stu-id="e606f-119">*expression*=*element*.metal</span></span>

<span data-ttu-id="e606f-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e606f-120">**Remarks**</span></span>

<span data-ttu-id="e606f-121">Se impostato su **true**, questo attributo fa sì che la luce riflessa in modo speculare sia il colore del materiale anziché il colore della sorgente di luce, rendendo l'oggetto apparentemente più metallico. Per approssimare un materiale metallico è necessario che la specularità sia relativamente alta (circa 1,2) e che la diffusione sia relativamente bassa (circa 0,6).</span><span class="sxs-lookup"><span data-stu-id="e606f-121">If set to **True**, this attribute causes the specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.To further approximate a metallic material requires that specularity be relatively high (about 1.2) and diffusity be relatively low (about 0.6).</span></span> <span data-ttu-id="e606f-122">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="e606f-122">The default value is **False**.</span></span>

<span data-ttu-id="e606f-123">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="e606f-123">*Microsoft Office Extensions Attribute*</span></span>

 

 