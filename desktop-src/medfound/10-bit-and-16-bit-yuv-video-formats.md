---
description: Questo argomento descrive i formati YUV a 10 e 16 bit consigliati per l'acquisizione, l'elaborazione e la visualizzazione di video nel sistema operativo Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formati video YUV a 10 bit e a 16 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129559"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a><span data-ttu-id="3b0ee-103">Formati video YUV a 10 bit e a 16 bit</span><span class="sxs-lookup"><span data-stu-id="3b0ee-103">10-bit and 16-bit YUV Video Formats</span></span>

<span data-ttu-id="3b0ee-104">Questo argomento descrive i formati YUV a 10 e 16 bit consigliati per l'acquisizione, l'elaborazione e la visualizzazione di video nel sistema operativo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-104">This topic describes the 10- and 16-bit YUV formats that are recommended for capturing, processing, and displaying video in the Microsoft Windows operating system.</span></span>

<span data-ttu-id="3b0ee-105">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b0ee-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3b0ee-106">Overview</span><span class="sxs-lookup"><span data-stu-id="3b0ee-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="3b0ee-107">Codici FOURCC per YUV a 10 bit e a 16 bit</span><span class="sxs-lookup"><span data-stu-id="3b0ee-107">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [<span data-ttu-id="3b0ee-108">Definizioni di superficie</span><span class="sxs-lookup"><span data-stu-id="3b0ee-108">Surface Definitions</span></span>](#surface-definitions)
    -   [<span data-ttu-id="3b0ee-109">formati 4:2:0</span><span class="sxs-lookup"><span data-stu-id="3b0ee-109">4:2:0 Formats</span></span>](#420-formats)
    -   [<span data-ttu-id="3b0ee-110">formati 4:2:2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-110">4:2:2 Formats</span></span>](#422-formats)
    -   [<span data-ttu-id="3b0ee-111">formati 4:4:4</span><span class="sxs-lookup"><span data-stu-id="3b0ee-111">4:4:4 Formats</span></span>](#444-formats)
-   [<span data-ttu-id="3b0ee-112">Formati YUV Preferiti</span><span class="sxs-lookup"><span data-stu-id="3b0ee-112">Preferred YUV Formats</span></span>](#preferred-yuv-formats)
-   [<span data-ttu-id="3b0ee-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b0ee-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="3b0ee-114">Panoramica</span><span class="sxs-lookup"><span data-stu-id="3b0ee-114">Overview</span></span>

<span data-ttu-id="3b0ee-115">Questi formati usano una rappresentazione a virgola fissa per i canali Luma Channel e Chroma (C'b e C'r).</span><span class="sxs-lookup"><span data-stu-id="3b0ee-115">These formats use a fixed-point representation for both the luma channel and the chroma (C'b and C'r) channels.</span></span> <span data-ttu-id="3b0ee-116">I valori di esempio vengono ridimensionati a 8 bit, usando un fattore di scala 2 ^ (n − 8), dove n è 10 o 16, come per le sezioni 7,7-7,8 e 7.11-7.12 di SMPTE 274M.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-116">Sample values are scaled 8-bit values, using a scaling factor of 2^(n − 8), where n is either 10 or 16, as per sections 7.7-7.8 and 7.11-7.12 of SMPTE 274M.</span></span> <span data-ttu-id="3b0ee-117">Le conversioni di precisione possono essere eseguite utilizzando semplici turni di bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-117">Precision conversions can be performed using simple bit shifts.</span></span> <span data-ttu-id="3b0ee-118">Se, ad esempio, il punto bianco di un formato a 8 bit è 235, il formato a 10 bit corrispondente è costituito da un punto bianco a 940 (235 × 4).</span><span class="sxs-lookup"><span data-stu-id="3b0ee-118">For example, if the white point of an 8-bit format is 235, the corresponding 10-bit format has a white point at 940 (235 × 4).</span></span>

<span data-ttu-id="3b0ee-119">Le rappresentazioni a 16 bit descritte di seguito usano valori di **parola** little-endian per ogni canale.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-119">The 16-bit representations described here use little-endian **WORD** values for each channel.</span></span> <span data-ttu-id="3b0ee-120">I formati a 10 bit utilizzano anche 16 bit per ogni canale, con i 6 bit più bassi impostati su zero, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-120">The 10-bit formats also use 16 bits for each channel, with the lowest 6 bits set to zero, as shown in the following diagram.</span></span>

![diagramma che mostra la rappresentazione a 10 bit](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

<span data-ttu-id="3b0ee-122">Poiché le rappresentazioni a 10 bit e a 16 bit dello stesso formato YUV hanno lo stesso layout di memoria, è possibile eseguire il cast di una rappresentazione a 10 bit a una rappresentazione a 16 senza perdita di precisione.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-122">Because the 10-bit and 16-bit representations of the same YUV format have the same memory layout, it is possible to cast a 10-bit representation to a 16-representation with no loss of precision.</span></span> <span data-ttu-id="3b0ee-123">È anche possibile eseguire il cast di una rappresentazione a 16 bit fino a una rappresentazione a 10 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-123">It is also possible to cast a 16-bit representation down to a 10-bit representation.</span></span> <span data-ttu-id="3b0ee-124">I formati Y416 e Y410 rappresentano un'eccezione a questa regola generale, tuttavia, poiché non condividono lo stesso layout di memoria.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-124">(The Y416 and Y410 formats are an exception to this general rule, however, because they do not share the same memory layout.)</span></span>

<span data-ttu-id="3b0ee-125">Quando l'hardware grafico legge una superficie che contiene una rappresentazione a 10 bit, deve ignorare i 6 bit di ordine inferiore di ogni canale.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-125">When the graphics hardware reads a surface that contains a 10-bit representation, it should ignore the low-order 6 bits of each channel.</span></span> <span data-ttu-id="3b0ee-126">Se una superficie contiene dati a 16 bit validi, tuttavia, deve essere identificata come una superficie a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-126">If a surface contains valid 16-bit data, however, it should be identified as a 16-bit surface.</span></span>

<span data-ttu-id="3b0ee-127">Nei formati che contengono Alpha, un pixel completamente trasparente ha un valore alfa pari a zero e un pixel completamente opaco ha un valore alfa pari a (2 ^ n)-1, dove n è il numero di bit alfa.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-127">In the formats that contain alpha, a completely transparent pixel has an alpha value of zero, and a completely opaque pixel has an alpha value of (2^n) – 1, where n is the number of alpha bits.</span></span> <span data-ttu-id="3b0ee-128">Si presuppone che Alpha sia un valore lineare applicato a ogni componente dopo che il componente è stato convertito in un formato lineare normalizzato.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-128">Alpha is assumed to be a linear value that is applied to each component after the component has been converted into its normalized linear form.</span></span>

<span data-ttu-id="3b0ee-129">Per le immagini nella memoria video, il driver di grafica seleziona l'allineamento della memoria della superficie.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-129">For images in video memory, the graphics driver selects the memory alignment of the surface.</span></span> <span data-ttu-id="3b0ee-130">L'area deve essere **DWORD** allineata.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-130">The surface must be **DWORD** aligned.</span></span> <span data-ttu-id="3b0ee-131">Ovvero le singole righe all'interno di una superficie vengono avviate a un limite di 32 bit, anche se l'allineamento può essere maggiore di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-131">That is, individual lines within a surface are guaranteed to start at a 32-bit boundary, although the alignment can be larger than 32 bits.</span></span> <span data-ttu-id="3b0ee-132">L'origine (0, 0) è sempre l'angolo superiore sinistro della superficie.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-132">The origin (0,0) is always the upper-left corner of the surface.</span></span>

<span data-ttu-id="3b0ee-133">Ai fini di questa documentazione, il termine *U* è equivalente a *CB* e il termine *V* è equivalente a *CR*.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-133">For the purposes of this documentation, the term *U* is equivalent to *Cb*, and the term *V* is equivalent to *Cr*.</span></span>

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a><span data-ttu-id="3b0ee-134">Codici FOURCC per YUV a 10 bit e a 16 bit</span><span class="sxs-lookup"><span data-stu-id="3b0ee-134">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>

<span data-ttu-id="3b0ee-135">I codici FOURCC per i formati descritti in questa sezione usano la convenzione seguente:</span><span class="sxs-lookup"><span data-stu-id="3b0ee-135">The FOURCC codes for the formats described here use the following convention:</span></span>

-   <span data-ttu-id="3b0ee-136">Se il formato è planare, il primo carattere nel codice FOURCC è "P".</span><span class="sxs-lookup"><span data-stu-id="3b0ee-136">If the format is planar, the first character in the FOURCC code is 'P'.</span></span> <span data-ttu-id="3b0ee-137">Se il formato è compresso, il primo carattere è "Y".</span><span class="sxs-lookup"><span data-stu-id="3b0ee-137">If the format is packed, the first character is 'Y'.</span></span>
-   <span data-ttu-id="3b0ee-138">Il secondo carattere nel codice FOURCC è determinato dal campionamento Chroma, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-138">The second character in the FOURCC code is determined by the chroma sampling, as shown in the following table.</span></span>

    

    | <span data-ttu-id="3b0ee-139">Campionamento Chroma</span><span class="sxs-lookup"><span data-stu-id="3b0ee-139">Chroma sampling</span></span> | <span data-ttu-id="3b0ee-140">Lettera di codice FOURCC</span><span class="sxs-lookup"><span data-stu-id="3b0ee-140">FOURCC code letter</span></span> |
    |-----------------|--------------------|
    | <span data-ttu-id="3b0ee-141">4:4:4</span><span class="sxs-lookup"><span data-stu-id="3b0ee-141">4:4:4</span></span>           | <span data-ttu-id="3b0ee-142">4</span><span class="sxs-lookup"><span data-stu-id="3b0ee-142">'4'</span></span>                |
    | <span data-ttu-id="3b0ee-143">4:2:2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-143">4:2:2</span></span>           | <span data-ttu-id="3b0ee-144">2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-144">'2'</span></span>                |
    | <span data-ttu-id="3b0ee-145">4:2:1</span><span class="sxs-lookup"><span data-stu-id="3b0ee-145">4:2:1</span></span>           | <span data-ttu-id="3b0ee-146">'1'</span><span class="sxs-lookup"><span data-stu-id="3b0ee-146">'1'</span></span>                |
    | <span data-ttu-id="3b0ee-147">4:2:0</span><span class="sxs-lookup"><span data-stu-id="3b0ee-147">4:2:0</span></span>           | <span data-ttu-id="3b0ee-148">'0'</span><span class="sxs-lookup"><span data-stu-id="3b0ee-148">'0'</span></span>                |

    

     

-   <span data-ttu-id="3b0ee-149">I due caratteri finali in FOURCC indicano il numero di bit per canale, ovvero "16" per 16 bit o "10" per 10 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-149">The final two characters in the FOURCC indicate the number of bits per channel, either '16' for 16 bits or '10' for 10 bits.</span></span>

<span data-ttu-id="3b0ee-150">Utilizzando questo schema, sono stati definiti i seguenti codici FOURCC.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-150">Using this scheme, the following FOURCC codes have been defined.</span></span> <span data-ttu-id="3b0ee-151">In questo momento non sono stati definiti formati 4:2:1 per YUV a 10 bit o a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-151">No 4:2:1 formats for 10-bit or 16-bit YUV have been defined at this time.</span></span>



| <span data-ttu-id="3b0ee-152">FOURCC</span><span class="sxs-lookup"><span data-stu-id="3b0ee-152">FOURCC</span></span> | <span data-ttu-id="3b0ee-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b0ee-153">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="3b0ee-154">P016</span><span class="sxs-lookup"><span data-stu-id="3b0ee-154">P016</span></span>   | <span data-ttu-id="3b0ee-155">Planar, 4:2:0, a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-155">Planar, 4:2:0, 16-bit.</span></span> |
| <span data-ttu-id="3b0ee-156">P010</span><span class="sxs-lookup"><span data-stu-id="3b0ee-156">P010</span></span>   | <span data-ttu-id="3b0ee-157">Planar, 4:2:0, a 10 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-157">Planar, 4:2:0, 10-bit.</span></span> |
| <span data-ttu-id="3b0ee-158">P216</span><span class="sxs-lookup"><span data-stu-id="3b0ee-158">P216</span></span>   | <span data-ttu-id="3b0ee-159">Planar, 4:2:2, a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-159">Planar, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="3b0ee-160">P210</span><span class="sxs-lookup"><span data-stu-id="3b0ee-160">P210</span></span>   | <span data-ttu-id="3b0ee-161">Planar, 4:2:2, a 10 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-161">Planar, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="3b0ee-162">Y216</span><span class="sxs-lookup"><span data-stu-id="3b0ee-162">Y216</span></span>   | <span data-ttu-id="3b0ee-163">Compresso, 4:2:2, a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-163">Packed, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="3b0ee-164">Y210</span><span class="sxs-lookup"><span data-stu-id="3b0ee-164">Y210</span></span>   | <span data-ttu-id="3b0ee-165">Compresso, 4:2:2, a 10 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-165">Packed, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="3b0ee-166">Y416</span><span class="sxs-lookup"><span data-stu-id="3b0ee-166">Y416</span></span>   | <span data-ttu-id="3b0ee-167">Compresso, 4:4:4, a 16 bit</span><span class="sxs-lookup"><span data-stu-id="3b0ee-167">Packed, 4:4:4, 16-bit</span></span>  |
| <span data-ttu-id="3b0ee-168">Y410</span><span class="sxs-lookup"><span data-stu-id="3b0ee-168">Y410</span></span>   | <span data-ttu-id="3b0ee-169">Compresso, 4:4:4, a 10 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-169">Packed, 4:4:4, 10-bit.</span></span> |



 

<span data-ttu-id="3b0ee-170">I GUID del sottotipo sono stati anche definiti da questi FourCC; vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3b0ee-170">Subtype GUIDs have also been defined from these FOURCCs; see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="3b0ee-171">Definizioni di superficie</span><span class="sxs-lookup"><span data-stu-id="3b0ee-171">Surface Definitions</span></span>

<span data-ttu-id="3b0ee-172">In questa sezione viene descritto il layout della memoria di ogni formato.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-172">This section describes the memory layout of each format.</span></span> <span data-ttu-id="3b0ee-173">Nelle descrizioni che seguono il termine **Word** si riferisce a un valore a 16 bit Little-endian e il termine **DWORD** si riferisce a un valore little endian a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-173">In the descriptions that follow, the term **WORD** refers to a little-endian 16-bit value, and the term **DWORD** refers to a little-endian 32-bit value.</span></span>

### <a name="420-formats"></a><span data-ttu-id="3b0ee-174">formati 4:2:0</span><span class="sxs-lookup"><span data-stu-id="3b0ee-174">4:2:0 Formats</span></span>

<span data-ttu-id="3b0ee-175">Sono definiti due formati 4:2:0, con i codici FOURCC P016 e P010.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-175">Two 4:2:0 formats are defined, with the FOURCC codes P016 and P010.</span></span> <span data-ttu-id="3b0ee-176">Condividono lo stesso layout di memoria, ma P016 USA 16 bit per canale e P010 USA 10 bit per canale.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-176">They share the same memory layout, but P016 uses 16 bits per channel and P010 uses 10 bits per channel.</span></span>

### <a name="p016-and-p010"></a><span data-ttu-id="3b0ee-177">P016 e P010</span><span class="sxs-lookup"><span data-stu-id="3b0ee-177">P016 and P010</span></span>

<span data-ttu-id="3b0ee-178">In questi due formati, tutti i campioni Y vengono visualizzati prima in memoria come una matrice di **Word** s con un numero pari di righe.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-178">In these two formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="3b0ee-179">Lo stride della superficie può essere maggiore della larghezza del piano Y.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-179">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="3b0ee-180">Questa matrice è seguita immediatamente da una matrice di **Word** che contiene esempi Interleaved e V, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-180">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![diagramma che mostra il layout di P016 e P010 pixel](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

<span data-ttu-id="3b0ee-182">Se la matrice di U-V combinata viene considerata come una matrice di **DWORD**, la parola meno significativa (LSW) contiene il valore U e la parola più significativa (RSU) contiene il valore V.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-182">If the combined U-V array is addressed as an array of **DWORD** s, the least significant word (LSW) contains the U value and the most significant word (MSW) contains the V value.</span></span> <span data-ttu-id="3b0ee-183">Lo stride del piano combinato U-V è uguale allo stride del piano Y.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-183">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="3b0ee-184">Il piano U-V ha un numero di righe pari a metà del piano Y.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-184">The U-V plane has half as many lines as the Y plane.</span></span>

<span data-ttu-id="3b0ee-185">Questi due formati sono i formati di pixel planari 4:2:0 preferiti per le rappresentazioni YUV con precisione più elevata.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-185">These two formats are the preferred 4:2:0 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="3b0ee-186">Si presuppone che si tratta di un requisito a breve termine per gli acceleratori DXVA (DirectX Video Acceleration) che supportano il video 4:2:0 a 10 bit o a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-186">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:0 video.</span></span>

### <a name="422-formats"></a><span data-ttu-id="3b0ee-187">formati 4:2:2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-187">4:2:2 Formats</span></span>

<span data-ttu-id="3b0ee-188">Sono definiti quattro formati 4:2:2, due planari e due compressi.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-188">Four 4:2:2 formats are defined, two planar and two packed.</span></span> <span data-ttu-id="3b0ee-189">Hanno i codici FOURCC seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b0ee-189">They have the following FOURCC codes:</span></span>

-   <span data-ttu-id="3b0ee-190">P216</span><span class="sxs-lookup"><span data-stu-id="3b0ee-190">P216</span></span>
-   <span data-ttu-id="3b0ee-191">P210</span><span class="sxs-lookup"><span data-stu-id="3b0ee-191">P210</span></span>
-   <span data-ttu-id="3b0ee-192">Y216</span><span class="sxs-lookup"><span data-stu-id="3b0ee-192">Y216</span></span>
-   <span data-ttu-id="3b0ee-193">Y210</span><span class="sxs-lookup"><span data-stu-id="3b0ee-193">Y210</span></span>

### <a name="p216-and-p210"></a><span data-ttu-id="3b0ee-194">P216 e P210</span><span class="sxs-lookup"><span data-stu-id="3b0ee-194">P216 and P210</span></span>

<span data-ttu-id="3b0ee-195">In questi due formati planari tutti i campioni Y vengono visualizzati prima in memoria come una matrice di **Word** s con un numero pari di righe.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-195">In these two planar formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="3b0ee-196">Lo stride della superficie può essere maggiore della larghezza del piano Y.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-196">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="3b0ee-197">Questa matrice è seguita immediatamente da una matrice di **Word** che contiene esempi Interleaved e V, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-197">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![diagramma che mostra il layout di p216 e P210 pixel](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

<span data-ttu-id="3b0ee-199">Se l'array U-V combinato viene considerato come una matrice di **DWORD** s, LSW contiene il valore U e il RSU contiene il valore V.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-199">If the combined U-V array is addressed as an array of **DWORD** s, the LSW contains the U value and the MSW contains the V value.</span></span> <span data-ttu-id="3b0ee-200">Lo stride del piano combinato U-V è uguale allo stride del piano Y.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-200">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="3b0ee-201">Il piano U-V ha lo stesso numero di righe del piano Y.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-201">The U-V plane has the same number of lines as the Y plane.</span></span>

<span data-ttu-id="3b0ee-202">Questi due formati sono i formati di pixel planari 4:2:2 Preferiti per le rappresentazioni YUV con precisione più elevata.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-202">These two formats are the preferred 4:2:2 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="3b0ee-203">Si presuppone che si tratta di un requisito a breve termine per gli acceleratori DXVA (DirectX Video Acceleration) che supportano il video 4:2:2 a 10 bit o a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-203">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:2 video.</span></span>

### <a name="y216-and-y210"></a><span data-ttu-id="3b0ee-204">Y216 e Y210</span><span class="sxs-lookup"><span data-stu-id="3b0ee-204">Y216 and Y210</span></span>

<span data-ttu-id="3b0ee-205">In questi due formati compressi ogni coppia di pixel viene archiviata come matrice di quattro **Word** s, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-205">In these two packed formats, each pair of pixels is stored as an array of four **WORD** s, as shown in the following illustration.</span></span>

![diagramma che illustra il layout di y216 e Y210 pixel.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

<span data-ttu-id="3b0ee-207">La prima **parola** nella matrice contiene il primo campione y nella coppia, la seconda **parola** contiene l'esempio U, la terza **parola** contiene il secondo campione y e la quarta **parola** contiene l'esempio V.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-207">The first **WORD** in the array contains the first Y sample in the pair, the second **WORD** contains the U sample, the third **WORD** contains the second Y sample, and the fourth **WORD** contains the V sample.</span></span>

<span data-ttu-id="3b0ee-208">Y210 è identico a y216 ad eccezione del fatto che ogni campione contiene solo 10 bit di dati significativi.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-208">Y210 is identical to Y216 except that each sample contains only 10 bits of significant data.</span></span> <span data-ttu-id="3b0ee-209">I 6 bit meno significativi sono impostati su zero, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-209">The least significant 6 bits are set to zero, as described previously.</span></span>

### <a name="444-formats"></a><span data-ttu-id="3b0ee-210">formati 4:4:4</span><span class="sxs-lookup"><span data-stu-id="3b0ee-210">4:4:4 Formats</span></span>

<span data-ttu-id="3b0ee-211">Sono definiti due formati 4:4:4, con i codici FOURCC Y410 e Y416.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-211">Two 4:4:4 formats are defined, with the FOURCC codes Y410 and Y416.</span></span> <span data-ttu-id="3b0ee-212">Entrambi i formati sono compressi.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-212">Both are packed formats.</span></span>

### <a name="y410"></a><span data-ttu-id="3b0ee-213">Y410</span><span class="sxs-lookup"><span data-stu-id="3b0ee-213">Y410</span></span>

<span data-ttu-id="3b0ee-214">Questo formato è una rappresentazione a 10 bit compressa che include 2 bit di alfa.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-214">This format is a packed 10-bit representation that includes 2 bits of alpha.</span></span> <span data-ttu-id="3b0ee-215">Ogni pixel è codificato come **valore DWORD** singolo con il layout di memoria illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-215">Each pixel is encoded as a single **DWORD** with the memory layout shown in the following diagram.</span></span>

![diagramma che mostra il layout del pixel y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

<span data-ttu-id="3b0ee-217">BITS 0-9 contengono l'esempio U, bits 10-19 contengono l'esempio Y, BITS 20-29 contiene l'esempio V e BITS 30-31 contengono il valore alfa.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-217">Bits 0-9 contain the U sample, bits 10-19 contain the Y sample, bits 20-29 contain the V sample, and bits 30-31 contain the alpha value.</span></span> <span data-ttu-id="3b0ee-218">Per indicare che un pixel è completamente opaco, un'applicazione deve impostare i due bit alfa uguali a 0x03.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-218">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0x03.</span></span>

### <a name="y416"></a><span data-ttu-id="3b0ee-219">Y416</span><span class="sxs-lookup"><span data-stu-id="3b0ee-219">Y416</span></span>

<span data-ttu-id="3b0ee-220">Questo formato è una rappresentazione a 16 bit compresso che include 16 bit di alfa.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-220">This format is a packed 16-bit representation that includes 16 bits of alpha.</span></span> <span data-ttu-id="3b0ee-221">Ogni pixel è codificato come coppia di **DWORD**, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-221">Each pixel is encoded as a pair of **DWORD** s, as shown in the following illustration.</span></span>

![diagramma che mostra il layout del pixel Y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

<span data-ttu-id="3b0ee-223">BITS 0-15 contengono l'esempio U, BITS 16-31 contengono l'esempio Y, BITS 32-47 contiene l'esempio V e BITS 48-63 contengono il valore alfa.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-223">Bits 0-15 contain the U sample, bits 16-31 contain the Y sample, bits 32-47 contain the V sample, and bits 48-63 contain the alpha value.</span></span>

<span data-ttu-id="3b0ee-224">Per indicare che un pixel è completamente opaco, un'applicazione deve impostare i due bit alfa uguali a 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-224">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0xFFFF.</span></span> <span data-ttu-id="3b0ee-225">Questo formato è destinato principalmente a un formato intermedio durante l'elaborazione di immagini per evitare l'accumulo di errori.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-225">This format is intended primarily as an intermediate format during image processing to avoid the accumulation of errors.</span></span>

## <a name="preferred-yuv-formats"></a><span data-ttu-id="3b0ee-226">Formati YUV Preferiti</span><span class="sxs-lookup"><span data-stu-id="3b0ee-226">Preferred YUV Formats</span></span>

<span data-ttu-id="3b0ee-227">La tabella seguente elenca i formati YUV preferiti, inclusi i formati a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-227">The following table lists the preferred YUV formats, including 8-bit formats.</span></span>



| <span data-ttu-id="3b0ee-228">Formato</span><span class="sxs-lookup"><span data-stu-id="3b0ee-228">Format</span></span> | <span data-ttu-id="3b0ee-229">Campionamento Chroma</span><span class="sxs-lookup"><span data-stu-id="3b0ee-229">Chroma sampling</span></span> | <span data-ttu-id="3b0ee-230">Compresso o planare</span><span class="sxs-lookup"><span data-stu-id="3b0ee-230">Packed or planar</span></span> | <span data-ttu-id="3b0ee-231">BITS per canale</span><span class="sxs-lookup"><span data-stu-id="3b0ee-231">Bits per channel</span></span> |
|--------|-----------------|------------------|------------------|
| <span data-ttu-id="3b0ee-232">AYUV</span><span class="sxs-lookup"><span data-stu-id="3b0ee-232">AYUV</span></span>   | <span data-ttu-id="3b0ee-233">4:4:4</span><span class="sxs-lookup"><span data-stu-id="3b0ee-233">4:4:4</span></span>           | <span data-ttu-id="3b0ee-234">Compressi</span><span class="sxs-lookup"><span data-stu-id="3b0ee-234">Packed</span></span>           | <span data-ttu-id="3b0ee-235">8</span><span class="sxs-lookup"><span data-stu-id="3b0ee-235">8</span></span>                |
| <span data-ttu-id="3b0ee-236">Y410</span><span class="sxs-lookup"><span data-stu-id="3b0ee-236">Y410</span></span>   | <span data-ttu-id="3b0ee-237">4:4:4</span><span class="sxs-lookup"><span data-stu-id="3b0ee-237">4:4:4</span></span>           | <span data-ttu-id="3b0ee-238">Compressi</span><span class="sxs-lookup"><span data-stu-id="3b0ee-238">Packed</span></span>           | <span data-ttu-id="3b0ee-239">10</span><span class="sxs-lookup"><span data-stu-id="3b0ee-239">10</span></span>               |
| <span data-ttu-id="3b0ee-240">Y416</span><span class="sxs-lookup"><span data-stu-id="3b0ee-240">Y416</span></span>   | <span data-ttu-id="3b0ee-241">4:4:4</span><span class="sxs-lookup"><span data-stu-id="3b0ee-241">4:4:4</span></span>           | <span data-ttu-id="3b0ee-242">Compressi</span><span class="sxs-lookup"><span data-stu-id="3b0ee-242">Packed</span></span>           | <span data-ttu-id="3b0ee-243">16</span><span class="sxs-lookup"><span data-stu-id="3b0ee-243">16</span></span>               |
| <span data-ttu-id="3b0ee-244">AI44</span><span class="sxs-lookup"><span data-stu-id="3b0ee-244">AI44</span></span>   | <span data-ttu-id="3b0ee-245">4:4:4</span><span class="sxs-lookup"><span data-stu-id="3b0ee-245">4:4:4</span></span>           | <span data-ttu-id="3b0ee-246">Compressi</span><span class="sxs-lookup"><span data-stu-id="3b0ee-246">Packed</span></span>           | <span data-ttu-id="3b0ee-247">Pallettizzati</span><span class="sxs-lookup"><span data-stu-id="3b0ee-247">Palettized</span></span>       |
| <span data-ttu-id="3b0ee-248">YUY2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-248">YUY2</span></span>   | <span data-ttu-id="3b0ee-249">4:2:2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-249">4:2:2</span></span>           | <span data-ttu-id="3b0ee-250">Compressi</span><span class="sxs-lookup"><span data-stu-id="3b0ee-250">Packed</span></span>           | <span data-ttu-id="3b0ee-251">8</span><span class="sxs-lookup"><span data-stu-id="3b0ee-251">8</span></span>                |
| <span data-ttu-id="3b0ee-252">Y210</span><span class="sxs-lookup"><span data-stu-id="3b0ee-252">Y210</span></span>   | <span data-ttu-id="3b0ee-253">4:2:2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-253">4:2:2</span></span>           | <span data-ttu-id="3b0ee-254">Compressi</span><span class="sxs-lookup"><span data-stu-id="3b0ee-254">Packed</span></span>           | <span data-ttu-id="3b0ee-255">10</span><span class="sxs-lookup"><span data-stu-id="3b0ee-255">10</span></span>               |
| <span data-ttu-id="3b0ee-256">Y216</span><span class="sxs-lookup"><span data-stu-id="3b0ee-256">Y216</span></span>   | <span data-ttu-id="3b0ee-257">4:2:2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-257">4:2:2</span></span>           | <span data-ttu-id="3b0ee-258">Compressi</span><span class="sxs-lookup"><span data-stu-id="3b0ee-258">Packed</span></span>           | <span data-ttu-id="3b0ee-259">16</span><span class="sxs-lookup"><span data-stu-id="3b0ee-259">16</span></span>               |
| <span data-ttu-id="3b0ee-260">P210</span><span class="sxs-lookup"><span data-stu-id="3b0ee-260">P210</span></span>   | <span data-ttu-id="3b0ee-261">4:2:2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-261">4:2:2</span></span>           | <span data-ttu-id="3b0ee-262">Planare</span><span class="sxs-lookup"><span data-stu-id="3b0ee-262">Planar</span></span>           | <span data-ttu-id="3b0ee-263">10</span><span class="sxs-lookup"><span data-stu-id="3b0ee-263">10</span></span>               |
| <span data-ttu-id="3b0ee-264">P216</span><span class="sxs-lookup"><span data-stu-id="3b0ee-264">P216</span></span>   | <span data-ttu-id="3b0ee-265">4:2:2</span><span class="sxs-lookup"><span data-stu-id="3b0ee-265">4:2:2</span></span>           | <span data-ttu-id="3b0ee-266">Planare</span><span class="sxs-lookup"><span data-stu-id="3b0ee-266">Planar</span></span>           | <span data-ttu-id="3b0ee-267">16</span><span class="sxs-lookup"><span data-stu-id="3b0ee-267">16</span></span>               |
| <span data-ttu-id="3b0ee-268">NV12</span><span class="sxs-lookup"><span data-stu-id="3b0ee-268">NV12</span></span>   | <span data-ttu-id="3b0ee-269">4:2:0</span><span class="sxs-lookup"><span data-stu-id="3b0ee-269">4:2:0</span></span>           | <span data-ttu-id="3b0ee-270">Planare</span><span class="sxs-lookup"><span data-stu-id="3b0ee-270">Planar</span></span>           | <span data-ttu-id="3b0ee-271">8</span><span class="sxs-lookup"><span data-stu-id="3b0ee-271">8</span></span>                |
| <span data-ttu-id="3b0ee-272">P010</span><span class="sxs-lookup"><span data-stu-id="3b0ee-272">P010</span></span>   | <span data-ttu-id="3b0ee-273">4:2:0</span><span class="sxs-lookup"><span data-stu-id="3b0ee-273">4:2:0</span></span>           | <span data-ttu-id="3b0ee-274">Planare</span><span class="sxs-lookup"><span data-stu-id="3b0ee-274">Planar</span></span>           | <span data-ttu-id="3b0ee-275">10</span><span class="sxs-lookup"><span data-stu-id="3b0ee-275">10</span></span>               |
| <span data-ttu-id="3b0ee-276">P016</span><span class="sxs-lookup"><span data-stu-id="3b0ee-276">P016</span></span>   | <span data-ttu-id="3b0ee-277">4:2:0</span><span class="sxs-lookup"><span data-stu-id="3b0ee-277">4:2:0</span></span>           | <span data-ttu-id="3b0ee-278">Planare</span><span class="sxs-lookup"><span data-stu-id="3b0ee-278">Planar</span></span>           | <span data-ttu-id="3b0ee-279">16</span><span class="sxs-lookup"><span data-stu-id="3b0ee-279">16</span></span>               |
| <span data-ttu-id="3b0ee-280">NV11</span><span class="sxs-lookup"><span data-stu-id="3b0ee-280">NV11</span></span>   | <span data-ttu-id="3b0ee-281">4:1:1</span><span class="sxs-lookup"><span data-stu-id="3b0ee-281">4:1:1</span></span>           | <span data-ttu-id="3b0ee-282">Planare</span><span class="sxs-lookup"><span data-stu-id="3b0ee-282">Planar</span></span>           | <span data-ttu-id="3b0ee-283">8</span><span class="sxs-lookup"><span data-stu-id="3b0ee-283">8</span></span>                |



 

<span data-ttu-id="3b0ee-284">È consigliabile che se un oggetto supporta uno schema di campionamento di profondità di bit e Chroma, deve supportare i formati YUV corrispondenti elencati in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-284">It is recommended that if an object supports a given bit depth and chroma sampling scheme, it should support the corresponding YUV formats listed in this table.</span></span> <span data-ttu-id="3b0ee-285">Gli oggetti potrebbero supportare formati aggiuntivi non elencati qui.</span><span class="sxs-lookup"><span data-stu-id="3b0ee-285">(Objects might support additional formats not listed here.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b0ee-286">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b0ee-286">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b0ee-287">Formati YUV a 8 bit consigliati per il rendering video</span><span class="sxs-lookup"><span data-stu-id="3b0ee-287">Recommended 8-Bit YUV Formats for Video Rendering</span></span>](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[<span data-ttu-id="3b0ee-288">GUID del sottotipo video</span><span class="sxs-lookup"><span data-stu-id="3b0ee-288">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> <dt>

[<span data-ttu-id="3b0ee-289">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="3b0ee-289">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



