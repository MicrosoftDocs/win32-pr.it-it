---
title: Attributo lucentezza di la
description: Attributo lucentezza di la
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337598"
---
# <a name="vml-shininess-attribute"></a><span data-ttu-id="23946-103">Attributo lucentezza di la</span><span class="sxs-lookup"><span data-stu-id="23946-103">VML Shininess Attribute</span></span>

<span data-ttu-id="23946-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="23946-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="23946-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="23946-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="23946-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="23946-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="23946-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="23946-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="23946-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="23946-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="23946-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="23946-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="23946-110">Definisce la concentrazione della luce riflessa su una superficie di estrusione.</span><span class="sxs-lookup"><span data-stu-id="23946-110">Defines the concentration of the reflected light on an extrusion surface.</span></span> <span data-ttu-id="23946-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="23946-111">Read/write.</span></span> <span data-ttu-id="23946-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="23946-112">**VgNumber**.</span></span>

<span data-ttu-id="23946-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="23946-113">**Applies To**</span></span>

[<span data-ttu-id="23946-114">Estrusione</span><span class="sxs-lookup"><span data-stu-id="23946-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="23946-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="23946-115">**Tag Syntax**</span></span>

<span data-ttu-id="23946-116"><o: *element* lucentezza = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="23946-116"><o: *element* shininess=" *expression* "></span></span>

<span data-ttu-id="23946-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="23946-117">**Script Syntax**</span></span>

<span data-ttu-id="23946-118">*element* . lucentezza = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="23946-118">*element* .shininess="*expression*"</span></span>

<span data-ttu-id="23946-119">*espressione* = *elemento*. lucentezza</span><span class="sxs-lookup"><span data-stu-id="23946-119">*expression*=*element*.shininess</span></span>

<span data-ttu-id="23946-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="23946-120">**Remarks**</span></span>

<span data-ttu-id="23946-121">Valori elevati (8-10) approssimano il lucentezza di un mirror e i valori bassi (2-3) si avvicinano a un effetto punteggiato.</span><span class="sxs-lookup"><span data-stu-id="23946-121">High values (8-10) would approximate the shininess of a mirror and low values (2-3) would approximate a speckled effect.</span></span> <span data-ttu-id="23946-122">I valori di 4-7 sono tipici.</span><span class="sxs-lookup"><span data-stu-id="23946-122">Values of 4-7 are typical.</span></span> <span data-ttu-id="23946-123">I riflessi non eseguono il mirroring di altri oggetti; vengono riflesse solo le origini luce Pinpoint.</span><span class="sxs-lookup"><span data-stu-id="23946-123">Reflections do not mirror other objects; only pinpoint light sources are reflected.</span></span> <span data-ttu-id="23946-124">Il valore predefinito è 5.</span><span class="sxs-lookup"><span data-stu-id="23946-124">Default value is 5.</span></span>

<span data-ttu-id="23946-125">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="23946-125">*Microsoft Office Extensions Attribute*</span></span>

 

 