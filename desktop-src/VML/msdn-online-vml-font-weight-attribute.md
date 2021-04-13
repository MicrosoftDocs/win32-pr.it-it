---
title: Attributo Font-Weight la
description: Attributo Font-Weight la
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e4de8a1bb4132c75d4520dcacc661fbbc97eef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399238"
---
# <a name="vml-font-weight-attribute"></a><span data-ttu-id="5e116-103">Attributo Font-Weight la</span><span class="sxs-lookup"><span data-stu-id="5e116-103">VML Font-Weight Attribute</span></span>

<span data-ttu-id="5e116-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5e116-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5e116-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="5e116-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5e116-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="5e116-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5e116-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="5e116-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5e116-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5e116-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5e116-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5e116-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5e116-110">Definisce lo spessore delle lettere del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="5e116-110">Defines the thickness of the letters of the font.</span></span> <span data-ttu-id="5e116-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5e116-111">Read/write.</span></span> <span data-ttu-id="5e116-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="5e116-112">**String**.</span></span>

<span data-ttu-id="5e116-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="5e116-113">**Applies To**</span></span>

[<span data-ttu-id="5e116-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="5e116-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="5e116-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="5e116-115">**Tag Syntax**</span></span>

<span data-ttu-id="5e116-116"><v: *elemento* Style = "font-weight: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="5e116-116"><v: *element* style="font-weight: *expression* "></span></span>

<span data-ttu-id="5e116-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="5e116-117">**Script Syntax**</span></span>

<span data-ttu-id="5e116-118">*element* . Style. FontWeight = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="5e116-118">*element* .style.fontweight="*expression*"</span></span>

<span data-ttu-id="5e116-119">*espressione* = *element*. Style. FontWeight</span><span class="sxs-lookup"><span data-stu-id="5e116-119">*expression*=*element*.style.fontweight</span></span>

<span data-ttu-id="5e116-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="5e116-120">**Remarks**</span></span>

<span data-ttu-id="5e116-121">I valori corrispondono agli attributi di stile HTML standard.</span><span class="sxs-lookup"><span data-stu-id="5e116-121">The values are the same as the standard HTML style attributes.</span></span> <span data-ttu-id="5e116-122">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="5e116-122">Values include:</span></span>



| <span data-ttu-id="5e116-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5e116-123">Value</span></span>   | <span data-ttu-id="5e116-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e116-124">Description</span></span>                                                                 |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5e116-125">normale</span><span class="sxs-lookup"><span data-stu-id="5e116-125">normal</span></span>  | <span data-ttu-id="5e116-126">Normale.</span><span class="sxs-lookup"><span data-stu-id="5e116-126">Normal.</span></span> <span data-ttu-id="5e116-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5e116-127">Default.</span></span>                                                            |
| <span data-ttu-id="5e116-128">Grassetto</span><span class="sxs-lookup"><span data-stu-id="5e116-128">bold</span></span>    | <span data-ttu-id="5e116-129">Grassetto.</span><span class="sxs-lookup"><span data-stu-id="5e116-129">Bold.</span></span>                                                                       |
| <span data-ttu-id="5e116-130">bolder</span><span class="sxs-lookup"><span data-stu-id="5e116-130">bolder</span></span>  | <span data-ttu-id="5e116-131">Più pesante del normale.</span><span class="sxs-lookup"><span data-stu-id="5e116-131">Heavier than normal.</span></span>                                                        |
| <span data-ttu-id="5e116-132">lighter</span><span class="sxs-lookup"><span data-stu-id="5e116-132">lighter</span></span> | <span data-ttu-id="5e116-133">Più chiaro del normale.</span><span class="sxs-lookup"><span data-stu-id="5e116-133">Lighter than normal.</span></span>                                                        |
| <span data-ttu-id="5e116-134">100</span><span class="sxs-lookup"><span data-stu-id="5e116-134">100</span></span>     | <span data-ttu-id="5e116-135">Almeno leggero come 200 peso.</span><span class="sxs-lookup"><span data-stu-id="5e116-135">At least as light as the 200 weight.</span></span>                                        |
| <span data-ttu-id="5e116-136">200</span><span class="sxs-lookup"><span data-stu-id="5e116-136">200</span></span>     | <span data-ttu-id="5e116-137">Almeno come grassetto come 100 e almeno come il peso 300.</span><span class="sxs-lookup"><span data-stu-id="5e116-137">At least as bold as the 100 weight and at least as light as the 300 weight.</span></span> |
| <span data-ttu-id="5e116-138">300</span><span class="sxs-lookup"><span data-stu-id="5e116-138">300</span></span>     | <span data-ttu-id="5e116-139">Almeno come grassetto come 200 e almeno come il peso 400.</span><span class="sxs-lookup"><span data-stu-id="5e116-139">At least as bold as the 200 weight and at least as light as the 400 weight.</span></span> |
| <span data-ttu-id="5e116-140">400</span><span class="sxs-lookup"><span data-stu-id="5e116-140">400</span></span>     | <span data-ttu-id="5e116-141">Normale.</span><span class="sxs-lookup"><span data-stu-id="5e116-141">Normal.</span></span>                                                                     |
| <span data-ttu-id="5e116-142">500</span><span class="sxs-lookup"><span data-stu-id="5e116-142">500</span></span>     | <span data-ttu-id="5e116-143">Almeno come grassetto come 400 e almeno come il peso 600.</span><span class="sxs-lookup"><span data-stu-id="5e116-143">At least as bold as the 400 weight and at least as light as the 600 weight.</span></span> |
| <span data-ttu-id="5e116-144">600</span><span class="sxs-lookup"><span data-stu-id="5e116-144">600</span></span>     | <span data-ttu-id="5e116-145">Almeno come grassetto come 500 e almeno come il peso 700.</span><span class="sxs-lookup"><span data-stu-id="5e116-145">At least as bold as the 500 weight and at least as light as the 700 weight.</span></span> |
| <span data-ttu-id="5e116-146">700</span><span class="sxs-lookup"><span data-stu-id="5e116-146">700</span></span>     | <span data-ttu-id="5e116-147">Grassetto.</span><span class="sxs-lookup"><span data-stu-id="5e116-147">Bold.</span></span>                                                                       |
| <span data-ttu-id="5e116-148">800</span><span class="sxs-lookup"><span data-stu-id="5e116-148">800</span></span>     | <span data-ttu-id="5e116-149">Almeno come grassetto come 700 e almeno come il peso 900.</span><span class="sxs-lookup"><span data-stu-id="5e116-149">At least as bold as the 700 weight and at least as light as the 900 weight.</span></span> |
| <span data-ttu-id="5e116-150">900</span><span class="sxs-lookup"><span data-stu-id="5e116-150">900</span></span>     | <span data-ttu-id="5e116-151">Almeno in grassetto come 800 peso.</span><span class="sxs-lookup"><span data-stu-id="5e116-151">At least as bold as the 800 weight.</span></span>                                         |



 

<span data-ttu-id="5e116-152">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="5e116-152">*VML Standard Attribute*</span></span>

<span data-ttu-id="5e116-153">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="5e116-153">**Example**</span></span>

<span data-ttu-id="5e116-154">Lo spessore del carattere è in grassetto.</span><span class="sxs-lookup"><span data-stu-id="5e116-154">The font weight is bold.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 