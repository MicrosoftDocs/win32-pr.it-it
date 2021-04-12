---
title: Attributo EXT (asimmetria) (la)
description: Attributo EXT (asimmetria) (la)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223951"
---
# <a name="ext-attribute-skewvml"></a><span data-ttu-id="e851f-103">Attributo EXT (asimmetria) (la)</span><span class="sxs-lookup"><span data-stu-id="e851f-103">Ext Attribute (Skew)(VML)</span></span>

<span data-ttu-id="e851f-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e851f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e851f-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e851f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e851f-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e851f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e851f-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e851f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e851f-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e851f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e851f-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e851f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e851f-110">Definisce la modalità di visualizzazione di una asimmetria.</span><span class="sxs-lookup"><span data-stu-id="e851f-110">Defines the way a skew is displayed.</span></span> <span data-ttu-id="e851f-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e851f-111">Read/write.</span></span> <span data-ttu-id="e851f-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="e851f-112">**String**.</span></span>

<span data-ttu-id="e851f-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e851f-113">**Applies To**</span></span>

[<span data-ttu-id="e851f-114">Sfasamento</span><span class="sxs-lookup"><span data-stu-id="e851f-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="e851f-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e851f-115">**Tag Syntax**</span></span>

<span data-ttu-id="e851f-116"><o: *element* v:EXT = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e851f-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="e851f-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e851f-117">**Script Syntax**</span></span>

<span data-ttu-id="e851f-118">*element* . ext = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e851f-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="e851f-119">*espressione* = *elemento*. ext</span><span class="sxs-lookup"><span data-stu-id="e851f-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="e851f-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e851f-120">**Remarks**</span></span>

<span data-ttu-id="e851f-121">Questo attributo viene utilizzato per indicare agli editor grafici come elaborare l'elemento di **inclinazione** .</span><span class="sxs-lookup"><span data-stu-id="e851f-121">This attribute is used to tell graphical editors how to process the **Skew** element.</span></span> <span data-ttu-id="e851f-122">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="e851f-122">Values include:</span></span>

-   <span data-ttu-id="e851f-123">**edit**</span><span class="sxs-lookup"><span data-stu-id="e851f-123">**edit**</span></span>
-   <span data-ttu-id="e851f-124">**Visualizza** (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e851f-124">**view** (default)</span></span>
-   <span data-ttu-id="e851f-125">**backwardCompatible**</span><span class="sxs-lookup"><span data-stu-id="e851f-125">**backwardCompatible**</span></span>

<span data-ttu-id="e851f-126">Se un'estensione è impostata per la **modifica**, può essere ignorata da un visualizzatore di software.</span><span class="sxs-lookup"><span data-stu-id="e851f-126">If an extension is set to **edit**, it can be ignored by a software viewer.</span></span> <span data-ttu-id="e851f-127">Se impostato su **View**, il visualizzatore deve invece eseguire il rendering della rappresentazione bitmap.</span><span class="sxs-lookup"><span data-stu-id="e851f-127">If set to **view**, the viewer must render the bitmap representation instead.</span></span>

<span data-ttu-id="e851f-128">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="e851f-128">*Microsoft Office Extensions Attribute*</span></span>

 

 