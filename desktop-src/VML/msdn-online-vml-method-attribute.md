---
title: Attributo del metodo la
description: Attributo del metodo la
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300140"
---
# <a name="vml-method-attribute"></a><span data-ttu-id="0f5e7-103">Attributo del metodo la</span><span class="sxs-lookup"><span data-stu-id="0f5e7-103">VML Method Attribute</span></span>

<span data-ttu-id="0f5e7-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0f5e7-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0f5e7-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0f5e7-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0f5e7-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0f5e7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0f5e7-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0f5e7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0f5e7-110">Definisce il metodo utilizzato per generare un riempimento sfumato.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-110">Defines the method used to generate a gradient fill.</span></span> <span data-ttu-id="0f5e7-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-111">Read/write.</span></span> <span data-ttu-id="0f5e7-112">**VgSigmaType**.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-112">**VgSigmaType**.</span></span>

<span data-ttu-id="0f5e7-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="0f5e7-113">**Applies To**</span></span>

[<span data-ttu-id="0f5e7-114">Fill</span><span class="sxs-lookup"><span data-stu-id="0f5e7-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="0f5e7-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="0f5e7-115">**Tag Syntax**</span></span>

<span data-ttu-id="0f5e7-116"><v: *element* Method = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="0f5e7-116"><v: *element* method=" *expression* "></span></span>

<span data-ttu-id="0f5e7-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="0f5e7-117">**Script Syntax**</span></span>

<span data-ttu-id="0f5e7-118">*element* . Method = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="0f5e7-118">*element* .method="*expression*"</span></span>

<span data-ttu-id="0f5e7-119">*espressione* = *element*. Method</span><span class="sxs-lookup"><span data-stu-id="0f5e7-119">*expression*=*element*.method</span></span>

<span data-ttu-id="0f5e7-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="0f5e7-120">**Remarks**</span></span>

<span data-ttu-id="0f5e7-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="0f5e7-121">Values include:</span></span>



| <span data-ttu-id="0f5e7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0f5e7-122">Value</span></span>  | <span data-ttu-id="0f5e7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f5e7-123">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="0f5e7-124">nessuno</span><span class="sxs-lookup"><span data-stu-id="0f5e7-124">None</span></span>   | <span data-ttu-id="0f5e7-125">Nessun riempimento Sigma.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-125">No sigma fill.</span></span>       |
| <span data-ttu-id="0f5e7-126">Lineari</span><span class="sxs-lookup"><span data-stu-id="0f5e7-126">Linear</span></span> | <span data-ttu-id="0f5e7-127">Riempimento Sigma lineare.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-127">Linear sigma fill.</span></span>   |
| <span data-ttu-id="0f5e7-128">Sigma</span><span class="sxs-lookup"><span data-stu-id="0f5e7-128">Sigma</span></span>  | <span data-ttu-id="0f5e7-129">Riempimento Sigma.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-129">Sigma fill.</span></span> <span data-ttu-id="0f5e7-130">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-130">Default.</span></span> |
| <span data-ttu-id="0f5e7-131">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="0f5e7-131">Any</span></span>    | <span data-ttu-id="0f5e7-132">Qualsiasi riempimento Sigma.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-132">Any sigma fill.</span></span>      |



 

<span data-ttu-id="0f5e7-133">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="0f5e7-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="0f5e7-134">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="0f5e7-134">**Example**</span></span>

<span data-ttu-id="0f5e7-135">La forma avrà un riempimento sfumato lineare rosso.</span><span class="sxs-lookup"><span data-stu-id="0f5e7-135">The shape will have a red linear gradient fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 