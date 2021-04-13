---
title: Attributo StartArrowLength di la
description: Attributo StartArrowLength di la
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399294"
---
# <a name="vml-startarrowlength-attribute"></a><span data-ttu-id="d765a-103">Attributo StartArrowLength di la</span><span class="sxs-lookup"><span data-stu-id="d765a-103">VML StartArrowLength Attribute</span></span>

<span data-ttu-id="d765a-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d765a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d765a-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d765a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d765a-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d765a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d765a-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d765a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d765a-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d765a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d765a-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d765a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d765a-110">Definisce la lunghezza della freccia per l'inizio di una riga.</span><span class="sxs-lookup"><span data-stu-id="d765a-110">Defines the arrowhead length for the start of a line.</span></span> <span data-ttu-id="d765a-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d765a-111">Read/write.</span></span> <span data-ttu-id="d765a-112">**VgArrowheadLength**.</span><span class="sxs-lookup"><span data-stu-id="d765a-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="d765a-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d765a-113">**Applies To**</span></span>

[<span data-ttu-id="d765a-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="d765a-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="d765a-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d765a-115">**Tag Syntax**</span></span>

<span data-ttu-id="d765a-116"><v: *element* startarrowlength = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d765a-116"><v: *element* startarrowlength=" *expression* "></span></span>

<span data-ttu-id="d765a-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d765a-117">**Script Syntax**</span></span>

<span data-ttu-id="d765a-118">*element* . startarrowlength = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d765a-118">*element* .startarrowlength="*expression*"</span></span>

<span data-ttu-id="d765a-119">*espressione* = *elemento*. startarrowlength</span><span class="sxs-lookup"><span data-stu-id="d765a-119">*expression*=*element*.startarrowlength</span></span>

<span data-ttu-id="d765a-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d765a-120">**Remarks**</span></span>

<span data-ttu-id="d765a-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="d765a-121">Values include:</span></span>

-   <span data-ttu-id="d765a-122">Short</span><span class="sxs-lookup"><span data-stu-id="d765a-122">Short</span></span>
-   <span data-ttu-id="d765a-123">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d765a-123">Medium (default)</span></span>
-   <span data-ttu-id="d765a-124">long</span><span class="sxs-lookup"><span data-stu-id="d765a-124">Long</span></span>

<span data-ttu-id="d765a-125">Attributo standard la</span><span class="sxs-lookup"><span data-stu-id="d765a-125">VML Standard Attribute</span></span>

<span data-ttu-id="d765a-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d765a-126">**Example**</span></span>

<span data-ttu-id="d765a-127">Viene disegnata una linea con una breve freccia classica all'inizio del tratto.</span><span class="sxs-lookup"><span data-stu-id="d765a-127">A line is drawn with a short classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 