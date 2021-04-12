---
title: Attributo MiterLimit di la
description: Attributo MiterLimit di la
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473430"
---
# <a name="vml-miterlimit-attribute"></a><span data-ttu-id="5dc64-103">Attributo MiterLimit di la</span><span class="sxs-lookup"><span data-stu-id="5dc64-103">VML MiterLimit Attribute</span></span>

<span data-ttu-id="5dc64-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5dc64-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5dc64-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="5dc64-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5dc64-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="5dc64-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5dc64-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="5dc64-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5dc64-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5dc64-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5dc64-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5dc64-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5dc64-110">Definisce la uniformità del giunto smussato.</span><span class="sxs-lookup"><span data-stu-id="5dc64-110">Defines the smoothness of the miter joint.</span></span> <span data-ttu-id="5dc64-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5dc64-111">Read/write.</span></span> <span data-ttu-id="5dc64-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="5dc64-112">**VgNumber**.</span></span>

<span data-ttu-id="5dc64-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="5dc64-113">**Applies To**</span></span>

[<span data-ttu-id="5dc64-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="5dc64-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="5dc64-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="5dc64-115">**Tag Syntax**</span></span>

<span data-ttu-id="5dc64-116"><v: *element* MiterLimit = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5dc64-116"><v: *element* miterlimit=" *expression* "></span></span>

<span data-ttu-id="5dc64-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="5dc64-117">**Script Syntax**</span></span>

<span data-ttu-id="5dc64-118">*element* . MiterLimit = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="5dc64-118">*element* .miterlimit="*expression*"</span></span>

<span data-ttu-id="5dc64-119">*espressione* = *elemento*. MiterLimit</span><span class="sxs-lookup"><span data-stu-id="5dc64-119">*expression*=*element*.miterlimit</span></span>

<span data-ttu-id="5dc64-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="5dc64-120">**Remarks**</span></span>

<span data-ttu-id="5dc64-121">Distanza massima tra il punto interno e il punto esterno di una giunzione.</span><span class="sxs-lookup"><span data-stu-id="5dc64-121">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="5dc64-122">Questo numero è un multiplo dello spessore della linea.</span><span class="sxs-lookup"><span data-stu-id="5dc64-122">This number is a multiple of the thickness of the line.</span></span>

<span data-ttu-id="5dc64-123">Il valore predefinito è 8.</span><span class="sxs-lookup"><span data-stu-id="5dc64-123">The default value is 8.</span></span>

<span data-ttu-id="5dc64-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="5dc64-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="5dc64-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="5dc64-125">**Example**</span></span>

<span data-ttu-id="5dc64-126">I giunti sulla polilinea sono sgolato con un limite di 10, ovvero 5 volte 2 punti.</span><span class="sxs-lookup"><span data-stu-id="5dc64-126">The joints on the polyline are mitered with a limit of 10, that is, 5 times 2 points.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 