---
title: Attributo di estremità la
description: Attributo di estremità la
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339183"
---
# <a name="vml-endcap-attribute"></a><span data-ttu-id="0b49c-103">Attributo di estremità la</span><span class="sxs-lookup"><span data-stu-id="0b49c-103">VML EndCap Attribute</span></span>

<span data-ttu-id="0b49c-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0b49c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0b49c-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="0b49c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0b49c-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="0b49c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0b49c-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="0b49c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0b49c-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0b49c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0b49c-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0b49c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0b49c-110">Definisce lo stile della terminazione per la fine di un tratto.</span><span class="sxs-lookup"><span data-stu-id="0b49c-110">Defines the cap style for the end of a stroke.</span></span> <span data-ttu-id="0b49c-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0b49c-111">Read/write.</span></span> <span data-ttu-id="0b49c-112">**VgLineEndCapStyle**.</span><span class="sxs-lookup"><span data-stu-id="0b49c-112">**VgLineEndCapStyle**.</span></span>

<span data-ttu-id="0b49c-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="0b49c-113">**Applies To**</span></span>

[<span data-ttu-id="0b49c-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="0b49c-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="0b49c-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="0b49c-115">**Tag Syntax**</span></span>

<span data-ttu-id="0b49c-116"><v: *element* mazzet = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0b49c-116"><v: *element* endcap=" *expression* "></span></span>

<span data-ttu-id="0b49c-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="0b49c-117">**Script Syntax**</span></span>

<span data-ttu-id="0b49c-118">*element* . estremità = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="0b49c-118">*element* .endcap="*expression*"</span></span>

<span data-ttu-id="0b49c-119">*espressione* = *elemento*. estremità</span><span class="sxs-lookup"><span data-stu-id="0b49c-119">*expression*=*element*.endcap</span></span>

<span data-ttu-id="0b49c-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="0b49c-120">**Remarks**</span></span>

<span data-ttu-id="0b49c-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="0b49c-121">Values include:</span></span>

-   <span data-ttu-id="0b49c-122">Flat (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b49c-122">Flat (default)</span></span>
-   <span data-ttu-id="0b49c-123">Square</span><span class="sxs-lookup"><span data-stu-id="0b49c-123">Square</span></span>
-   <span data-ttu-id="0b49c-124">Round</span><span class="sxs-lookup"><span data-stu-id="0b49c-124">Round</span></span>

<span data-ttu-id="0b49c-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="0b49c-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="0b49c-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0b49c-126">**Example**</span></span>

<span data-ttu-id="0b49c-127">Una linea viene disegnata con un perno fisso alla fine del tratto.</span><span class="sxs-lookup"><span data-stu-id="0b49c-127">A line is drawn with a flat cap on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 