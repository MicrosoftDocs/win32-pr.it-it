---
description: Transizione della chiave
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transizione della chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876202"
---
# <a name="key-transition"></a><span data-ttu-id="94dd7-103">Transizione della chiave</span><span class="sxs-lookup"><span data-stu-id="94dd7-103">Key Transition</span></span>

> [!Note]  
> <span data-ttu-id="94dd7-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="94dd7-104">\[Deprecated.</span></span> <span data-ttu-id="94dd7-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="94dd7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="94dd7-106">La transizione della chiave esegue la digitazione in base al valore RGB, al valore alfa, alla tonalità o alla luminosità.</span><span class="sxs-lookup"><span data-stu-id="94dd7-106">The Key transition performs keying based on RGB value, alpha value, hue or luminance.</span></span>

<span data-ttu-id="94dd7-107">Nell'immagine seguente viene illustrata la transizione della chiave:</span><span class="sxs-lookup"><span data-stu-id="94dd7-107">The following image shows the key transition:</span></span>

![transizione della chiave](images/trans-key.png)

<span data-ttu-id="94dd7-109">ID classe (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="94dd7-109">Class ID (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}</span></span>

<span data-ttu-id="94dd7-110">Nome variabile CLSID: CLSID \_ DxtKey</span><span class="sxs-lookup"><span data-stu-id="94dd7-110">CLSID Variable Name: CLSID\_DxtKey</span></span>

<span data-ttu-id="94dd7-111">Nome descrittivo: "DxtKey"</span><span class="sxs-lookup"><span data-stu-id="94dd7-111">Friendly Name: "DxtKey"</span></span>

<span data-ttu-id="94dd7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94dd7-112">Properties</span></span>



| <span data-ttu-id="94dd7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="94dd7-113">Property</span></span>   | <span data-ttu-id="94dd7-114">Type</span><span class="sxs-lookup"><span data-stu-id="94dd7-114">Type</span></span>  | <span data-ttu-id="94dd7-115">Intervallo valido</span><span class="sxs-lookup"><span data-stu-id="94dd7-115">Valid range</span></span>           | <span data-ttu-id="94dd7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94dd7-116">Description</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="94dd7-117">Si applica a</span><span class="sxs-lookup"><span data-stu-id="94dd7-117">Applies To</span></span>                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="94dd7-118">Tonalità</span><span class="sxs-lookup"><span data-stu-id="94dd7-118">Hue</span></span>        | <span data-ttu-id="94dd7-119">INT</span><span class="sxs-lookup"><span data-stu-id="94dd7-119">int</span></span>   | <span data-ttu-id="94dd7-120">0 – 360</span><span class="sxs-lookup"><span data-stu-id="94dd7-120">0–360</span></span>                 | <span data-ttu-id="94dd7-121">Valore di tonalità su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="94dd7-121">The hue value on which to key.</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="94dd7-122">Tonalità</span><span class="sxs-lookup"><span data-stu-id="94dd7-122">Hue</span></span>                            |
| <span data-ttu-id="94dd7-123">Inverti</span><span class="sxs-lookup"><span data-stu-id="94dd7-123">Invert</span></span>     | <span data-ttu-id="94dd7-124">BOOL</span><span class="sxs-lookup"><span data-stu-id="94dd7-124">BOOL</span></span>  | <span data-ttu-id="94dd7-125">**False** o **true**</span><span class="sxs-lookup"><span data-stu-id="94dd7-125">**FALSE** or **TRUE**</span></span> | <span data-ttu-id="94dd7-126">Valore booleano che indica se invertire l'operazione predefinita della chiave.</span><span class="sxs-lookup"><span data-stu-id="94dd7-126">Boolean value indicating whether to invert the default operation of the key.</span></span> <span data-ttu-id="94dd7-127">Se **false**, i pixel nell'immagine di sovrastanti vengono resi trasparenti nel modo predefinito.</span><span class="sxs-lookup"><span data-stu-id="94dd7-127">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span> <span data-ttu-id="94dd7-128">Se **true**, l'operazione viene invertita.</span><span class="sxs-lookup"><span data-stu-id="94dd7-128">If **TRUE**, the operation inverts.</span></span>                                                   | <span data-ttu-id="94dd7-129">Chroma, Hue, Luminance, Nonred</span><span class="sxs-lookup"><span data-stu-id="94dd7-129">Chroma, Hue, Luminance, Nonred</span></span> |
| <span data-ttu-id="94dd7-130">KeyType</span><span class="sxs-lookup"><span data-stu-id="94dd7-130">KeyType</span></span>    | <span data-ttu-id="94dd7-131">INT</span><span class="sxs-lookup"><span data-stu-id="94dd7-131">int</span></span>   | <span data-ttu-id="94dd7-132">Vedere la sezione Osservazioni</span><span class="sxs-lookup"><span data-stu-id="94dd7-132">See Remarks</span></span>           | <span data-ttu-id="94dd7-133">Specifica il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="94dd7-133">Specifies the type of key.</span></span> <span data-ttu-id="94dd7-134">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="94dd7-134">For more information, see Remarks.</span></span>                                                                                                                                                                                              | <span data-ttu-id="94dd7-135">Tutti</span><span class="sxs-lookup"><span data-stu-id="94dd7-135">All</span></span>                            |
| <span data-ttu-id="94dd7-136">Luminance</span><span class="sxs-lookup"><span data-stu-id="94dd7-136">Luminance</span></span>  | <span data-ttu-id="94dd7-137">INT</span><span class="sxs-lookup"><span data-stu-id="94dd7-137">int</span></span>   | <span data-ttu-id="94dd7-138">0 – 100</span><span class="sxs-lookup"><span data-stu-id="94dd7-138">0–100</span></span>                 | <span data-ttu-id="94dd7-139">Valore di luminanza su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="94dd7-139">The luminance value on which to key.</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="94dd7-140">Luminance</span><span class="sxs-lookup"><span data-stu-id="94dd7-140">Luminance</span></span>                      |
| <span data-ttu-id="94dd7-141">RGB</span><span class="sxs-lookup"><span data-stu-id="94dd7-141">RGB</span></span>        | <span data-ttu-id="94dd7-142">DWORD</span><span class="sxs-lookup"><span data-stu-id="94dd7-142">DWORD</span></span> | <span data-ttu-id="94dd7-143">0x0-0xFFFFFF</span><span class="sxs-lookup"><span data-stu-id="94dd7-143">0x0 – 0xFFFFFF</span></span>        | <span data-ttu-id="94dd7-144">Colore su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="94dd7-144">The color on which to key.</span></span> <span data-ttu-id="94dd7-145">Il valore è un numero esadecimale con formato 0x *RRGGBB*, dove *RR* è il valore rosso, *GG* è il valore verde e *BB* è il valore blu.</span><span class="sxs-lookup"><span data-stu-id="94dd7-145">The value is a hexadecimal number with the format 0x *RRGGBB*, where *RR* is the red value, *GG* is the green value, and *BB* is the blue value.</span></span> <span data-ttu-id="94dd7-146">I puri rossi, verdi e blu sono rispettivamente 0xFF0000, 0x00FF00 e 0x0000FF.</span><span class="sxs-lookup"><span data-stu-id="94dd7-146">(Pure red, green, and blue are 0xFF0000, 0x00FF00, and 0x0000FF, respectively.)</span></span> | <span data-ttu-id="94dd7-147">Croma</span><span class="sxs-lookup"><span data-stu-id="94dd7-147">Chroma</span></span>                         |
| <span data-ttu-id="94dd7-148">Similarity</span><span class="sxs-lookup"><span data-stu-id="94dd7-148">Similarity</span></span> | <span data-ttu-id="94dd7-149">INT</span><span class="sxs-lookup"><span data-stu-id="94dd7-149">int</span></span>   | <span data-ttu-id="94dd7-150">0 – 100</span><span class="sxs-lookup"><span data-stu-id="94dd7-150">0–100</span></span>                 | <span data-ttu-id="94dd7-151">Intervallo di dati del colore che diventa trasparente.</span><span class="sxs-lookup"><span data-stu-id="94dd7-151">The range of color data that becomes transparent.</span></span> <span data-ttu-id="94dd7-152">Con valori superiori, una gamma più ampia di colori simili è trasparente.</span><span class="sxs-lookup"><span data-stu-id="94dd7-152">At higher values, a wider range of similar colors is transparent.</span></span>                                                                                                                                        | <span data-ttu-id="94dd7-153">Chroma, Nonred</span><span class="sxs-lookup"><span data-stu-id="94dd7-153">Chroma, Nonred</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="94dd7-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="94dd7-154">Remarks</span></span>

<span data-ttu-id="94dd7-155">Il tipo di chiave eseguita dipende dal valore della proprietà del **tipo** di chiave, che deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="94dd7-155">The type of key that is performed depends on the value of the **KeyType** property, which must be one of the following:</span></span>



| <span data-ttu-id="94dd7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="94dd7-156">Value</span></span> | <span data-ttu-id="94dd7-157">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="94dd7-157">Enumeration</span></span>       | <span data-ttu-id="94dd7-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94dd7-158">Description</span></span>                                           |
|-------|-------------------|-------------------------------------------------------|
| <span data-ttu-id="94dd7-159">0</span><span class="sxs-lookup"><span data-stu-id="94dd7-159">0</span></span>     | <span data-ttu-id="94dd7-160">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="94dd7-160">DXTKEY\_RGB</span></span>       | <span data-ttu-id="94dd7-161">Chroma Key (chiave per valore RGB).</span><span class="sxs-lookup"><span data-stu-id="94dd7-161">Chroma key (key by RGB value).</span></span>                        |
| <span data-ttu-id="94dd7-162">1</span><span class="sxs-lookup"><span data-stu-id="94dd7-162">1</span></span>     | <span data-ttu-id="94dd7-163">\_NONRED DXTKEY</span><span class="sxs-lookup"><span data-stu-id="94dd7-163">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="94dd7-164">Chiave di Nonred.</span><span class="sxs-lookup"><span data-stu-id="94dd7-164">Nonred key.</span></span> <span data-ttu-id="94dd7-165">(Rende trasparenti le aree blu e verde).</span><span class="sxs-lookup"><span data-stu-id="94dd7-165">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="94dd7-166">2</span><span class="sxs-lookup"><span data-stu-id="94dd7-166">2</span></span>     | <span data-ttu-id="94dd7-167">\_luminanza DXTKEY</span><span class="sxs-lookup"><span data-stu-id="94dd7-167">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="94dd7-168">Chiave di luminanza.</span><span class="sxs-lookup"><span data-stu-id="94dd7-168">Luminance key.</span></span>                                        |
| <span data-ttu-id="94dd7-169">3</span><span class="sxs-lookup"><span data-stu-id="94dd7-169">3</span></span>     | <span data-ttu-id="94dd7-170">DXTKEY \_ alfa</span><span class="sxs-lookup"><span data-stu-id="94dd7-170">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="94dd7-171">Chiave per valore alfa.</span><span class="sxs-lookup"><span data-stu-id="94dd7-171">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="94dd7-172">4</span><span class="sxs-lookup"><span data-stu-id="94dd7-172">4</span></span>     | <span data-ttu-id="94dd7-173">\_tonalità DXTKEY</span><span class="sxs-lookup"><span data-stu-id="94dd7-173">DXTKEY\_HUE</span></span>       | <span data-ttu-id="94dd7-174">Chiave per tonalità.</span><span class="sxs-lookup"><span data-stu-id="94dd7-174">Key by hue.</span></span>                                           |



 

<span data-ttu-id="94dd7-175">Il valore predefinito del tipo di chiave è DXTKEY \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="94dd7-175">The key type defaults to DXTKEY\_ALPHA.</span></span>

 

 



