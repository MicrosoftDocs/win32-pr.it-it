---
title: Attributo InvX di la
description: Attributo InvX di la
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728074"
---
# <a name="vml-invx-attribute"></a><span data-ttu-id="8d2c3-103">Attributo InvX di la</span><span class="sxs-lookup"><span data-stu-id="8d2c3-103">VML InvX Attribute</span></span>

<span data-ttu-id="8d2c3-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8d2c3-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8d2c3-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8d2c3-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8d2c3-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8d2c3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8d2c3-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8d2c3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8d2c3-110">Determina se la posizione x dell'handle è invertita.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-110">Determines whether the x position of the handle is inverted.</span></span> <span data-ttu-id="8d2c3-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-111">Read/write.</span></span> <span data-ttu-id="8d2c3-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-112">**VgTriState**.</span></span>

<span data-ttu-id="8d2c3-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="8d2c3-113">**Applies To**</span></span>

<span data-ttu-id="8d2c3-114">[H](msdn-online-vml-h-element.md) (sottoelemento di [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="8d2c3-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="8d2c3-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="8d2c3-115">**Tag Syntax**</span></span>

<span data-ttu-id="8d2c3-116"><v: *element* invx = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="8d2c3-116"><v: *element* invx=" *expression* "></span></span>

<span data-ttu-id="8d2c3-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="8d2c3-117">**Remarks**</span></span>

<span data-ttu-id="8d2c3-118">Se è **true**, la posizione x dell'handle viene invertita sottraendo il valore x dal valore x di **CoordOrigin** aggiunto al valore x di **CoordSize**.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-118">If **True**, the x position of the handle is inverted by subtracting the x value from the x value of **CoordOrigin** added to the x value of **CoordSize**.</span></span> <span data-ttu-id="8d2c3-119">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-119">The default value is **False**.</span></span>

<span data-ttu-id="8d2c3-120">Questo attributo è l'equivalente di</span><span class="sxs-lookup"><span data-stu-id="8d2c3-120">This attribute is the equivalent of</span></span>

<span data-ttu-id="8d2c3-121">coordorigin. x + coordsize. x-h. Position. x</span><span class="sxs-lookup"><span data-stu-id="8d2c3-121">coordorigin.x + coordsize.x - h.position.x</span></span>

<span data-ttu-id="8d2c3-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="8d2c3-122">*VML Standard Attribute*</span></span>

 

 