---
title: Attributo size (VMLFrame)
description: Attributo size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046808"
---
# <a name="size-attribute-vmlframe"></a><span data-ttu-id="d90b0-103">Attributo size (VMLFrame)</span><span class="sxs-lookup"><span data-stu-id="d90b0-103">Size Attribute (VMLFrame)</span></span>

<span data-ttu-id="d90b0-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d90b0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d90b0-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d90b0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d90b0-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d90b0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d90b0-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d90b0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d90b0-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d90b0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d90b0-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d90b0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d90b0-110">Definisce le dimensioni dell'area di visualizzazione del frame.</span><span class="sxs-lookup"><span data-stu-id="d90b0-110">Defines the size of the clipping region of the frame.</span></span> <span data-ttu-id="d90b0-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d90b0-111">Read/write.</span></span> <span data-ttu-id="d90b0-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="d90b0-112">**VgVector2D**.</span></span>

<span data-ttu-id="d90b0-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d90b0-113">**Applies To**</span></span>

[<span data-ttu-id="d90b0-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="d90b0-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="d90b0-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d90b0-115">**Tag Syntax**</span></span>

<span data-ttu-id="d90b0-116"><v: *element* size = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d90b0-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="d90b0-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d90b0-117">**Script Syntax**</span></span>

<span data-ttu-id="d90b0-118">*element* . size = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d90b0-118">*element* .size="*expression*"</span></span>

<span data-ttu-id="d90b0-119">*espressione* = *element*. size</span><span class="sxs-lookup"><span data-stu-id="d90b0-119">*expression*=*element*.size</span></span>

<span data-ttu-id="d90b0-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d90b0-120">**Remarks**</span></span>

<span data-ttu-id="d90b0-121">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="d90b0-121">The default value is 0,0.</span></span> <span data-ttu-id="d90b0-122">Si noti che la **dimensione** funziona solo se il [clip](msdn-online-vml-clip-attribute.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="d90b0-122">Note that **Size** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="d90b0-123">In questo attributo, le dimensioni sono definite come larghezza e altezza del frame.</span><span class="sxs-lookup"><span data-stu-id="d90b0-123">In this attribute, the size is defined as the width and height of the frame.</span></span>

<span data-ttu-id="d90b0-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="d90b0-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d90b0-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d90b0-125">**Example**</span></span>

<span data-ttu-id="d90b0-126">Le dimensioni dell'area di ridimensionamento saranno 50pt, 50pt.</span><span class="sxs-lookup"><span data-stu-id="d90b0-126">The size of the clipping region will be 50pt, 50pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 