---
title: Attributo InvY di la
description: Attributo InvY di la
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338007"
---
# <a name="vml-invy-attribute"></a><span data-ttu-id="80e67-103">Attributo InvY di la</span><span class="sxs-lookup"><span data-stu-id="80e67-103">VML InvY Attribute</span></span>

<span data-ttu-id="80e67-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="80e67-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="80e67-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="80e67-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="80e67-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="80e67-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="80e67-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="80e67-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="80e67-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="80e67-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="80e67-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="80e67-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="80e67-110">Determina se la posizione y dell'handle è invertita.</span><span class="sxs-lookup"><span data-stu-id="80e67-110">Determines whether the y position of the handle is inverted.</span></span> <span data-ttu-id="80e67-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="80e67-111">Read/write.</span></span> <span data-ttu-id="80e67-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="80e67-112">**VgTriState**.</span></span>

<span data-ttu-id="80e67-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="80e67-113">**Applies To**</span></span>

<span data-ttu-id="80e67-114">[H](msdn-online-vml-h-element.md) (sottoelemento di [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="80e67-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="80e67-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="80e67-115">**Tag Syntax**</span></span>

<span data-ttu-id="80e67-116"><v: *element* invy = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="80e67-116"><v: *element* invy=" *expression* "></span></span>

<span data-ttu-id="80e67-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="80e67-117">**Remarks**</span></span>

<span data-ttu-id="80e67-118">Se è **true**, la posizione y dell'handle viene invertita sottraendo il valore y dal valore y di **CoordOrigin** aggiunto al valore y di **CoordSize**.</span><span class="sxs-lookup"><span data-stu-id="80e67-118">If **True**, the y position of the handle is inverted by subtracting the y value from the y value of **CoordOrigin** added to the y value of **CoordSize**.</span></span> <span data-ttu-id="80e67-119">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="80e67-119">The default value is **False**.</span></span>

<span data-ttu-id="80e67-120">Questo attributo è l'equivalente di</span><span class="sxs-lookup"><span data-stu-id="80e67-120">This attribute is the equivalent of</span></span>


```HTML
coordorigin.y + coordsize.y - h.position.y
```



<span data-ttu-id="80e67-121">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="80e67-121">*VML Standard Attribute*</span></span>

 

 