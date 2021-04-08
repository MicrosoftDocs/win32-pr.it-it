---
title: Attributo ID (VMLFrame) (la)
description: Attributo ID (VMLFrame) (la)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046958"
---
# <a name="id-attribute-vmlframevml"></a><span data-ttu-id="6d23d-103">Attributo ID (VMLFrame) (la)</span><span class="sxs-lookup"><span data-stu-id="6d23d-103">ID Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="6d23d-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6d23d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6d23d-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="6d23d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6d23d-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="6d23d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6d23d-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="6d23d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6d23d-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6d23d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6d23d-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6d23d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6d23d-110">Definisce un identificatore univoco per il frame.</span><span class="sxs-lookup"><span data-stu-id="6d23d-110">Defines a unique identifier for the frame.</span></span> <span data-ttu-id="6d23d-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6d23d-111">Read/write.</span></span> <span data-ttu-id="6d23d-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="6d23d-112">**String**.</span></span>

<span data-ttu-id="6d23d-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="6d23d-113">**Applies To**</span></span>

[<span data-ttu-id="6d23d-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="6d23d-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="6d23d-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="6d23d-115">**Tag Syntax**</span></span>

<span data-ttu-id="6d23d-116"><v: *element* ID = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="6d23d-116"><v: *element* ID=" *expression* "></span></span>

<span data-ttu-id="6d23d-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="6d23d-117">**Script Syntax**</span></span>

<span data-ttu-id="6d23d-118">*element* . ID = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="6d23d-118">*element* .ID="*expression*"</span></span>

<span data-ttu-id="6d23d-119">*espressione* = *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="6d23d-119">*expression*=*element*.ID</span></span>

<span data-ttu-id="6d23d-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="6d23d-120">**Remarks**</span></span>

<span data-ttu-id="6d23d-121">Usare **ID** per fare riferimento a un frame.</span><span class="sxs-lookup"><span data-stu-id="6d23d-121">Use **ID** to reference a frame.</span></span> <span data-ttu-id="6d23d-122">È ad esempio possibile spostare il frame nella pagina modificando la posizione del frame a cui fa riferimento l' **ID**.</span><span class="sxs-lookup"><span data-stu-id="6d23d-122">For example, you can move the frame around on the page by changing the frame position referenced by the **ID**.</span></span>

<span data-ttu-id="6d23d-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="6d23d-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="6d23d-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="6d23d-124">**Example**</span></span>

<span data-ttu-id="6d23d-125">L' **ID** del frame è "Frame01".</span><span class="sxs-lookup"><span data-stu-id="6d23d-125">The **ID** of the frame is "frame01".</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 