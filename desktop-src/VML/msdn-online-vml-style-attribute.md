---
title: Attributo di stile la
description: Attributo di stile la
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473206"
---
# <a name="vml-style-attribute"></a><span data-ttu-id="ddacb-103">Attributo di stile la</span><span class="sxs-lookup"><span data-stu-id="ddacb-103">VML Style Attribute</span></span>

<span data-ttu-id="ddacb-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ddacb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ddacb-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ddacb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ddacb-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ddacb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ddacb-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ddacb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ddacb-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ddacb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ddacb-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ddacb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ddacb-110">Definisce lo stile del frame.</span><span class="sxs-lookup"><span data-stu-id="ddacb-110">Defines the style of the frame.</span></span> <span data-ttu-id="ddacb-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ddacb-111">Read/write.</span></span> <span data-ttu-id="ddacb-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="ddacb-112">**String**.</span></span>

<span data-ttu-id="ddacb-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ddacb-113">**Applies To**</span></span>

[<span data-ttu-id="ddacb-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="ddacb-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="ddacb-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ddacb-115">**Tag Syntax**</span></span>

<span data-ttu-id="ddacb-116"><v: *elemento* Style = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ddacb-116"><v: *element* style=" *expression* "></span></span>

<span data-ttu-id="ddacb-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="ddacb-117">**Script Syntax**</span></span>

<span data-ttu-id="ddacb-118">*element* . Style = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="ddacb-118">*element* .style="*expression*"</span></span>

<span data-ttu-id="ddacb-119">*espressione* = *element*. Style</span><span class="sxs-lookup"><span data-stu-id="ddacb-119">*expression*=*element*.style</span></span>

<span data-ttu-id="ddacb-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ddacb-120">**Remarks**</span></span>

<span data-ttu-id="ddacb-121">Questo attributo usa i normali attributi di stile CSS per il posizionamento.</span><span class="sxs-lookup"><span data-stu-id="ddacb-121">This attribute uses the normal CSS style attributes for positioning.</span></span>

<span data-ttu-id="ddacb-122">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="ddacb-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="ddacb-123">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="ddacb-123">**Example**</span></span>

<span data-ttu-id="ddacb-124">Lo stile definisce la posizione effettiva del frame.</span><span class="sxs-lookup"><span data-stu-id="ddacb-124">The style defines the actual position of the frame.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 