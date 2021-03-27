---
title: Formato BC6H
description: Il formato BC6H è un formato di compressione di trama progettato per supportare spazi dei colori HDR (High Dynamic Range) nei dati di origine.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed4b934df742a4d2c99e20b52b7172b64e598dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047101"
---
# <a name="bc6h-format"></a><span data-ttu-id="2c5db-105">Formato BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-105">BC6H Format</span></span>

<span data-ttu-id="2c5db-106">Il formato BC6H è un formato di compressione di trama progettato per supportare spazi dei colori HDR (High Dynamic Range) nei dati di origine.</span><span class="sxs-lookup"><span data-stu-id="2c5db-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="2c5db-107">Informazioni sul formato BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="2c5db-108">Implementazione di BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="2c5db-109">Decodifica del formato BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="2c5db-110">Formato dell'endpoint compresso BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="2c5db-111">Estensione del segno per i valori dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="2c5db-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="2c5db-112">Trasforma Inversion per i valori dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="2c5db-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="2c5db-113">Dequantizzazione degli endpoint dei colori</span><span class="sxs-lookup"><span data-stu-id="2c5db-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="2c5db-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c5db-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="2c5db-115">Informazioni sul formato BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="2c5db-116">Il formato BC6H offre una compressione di alta qualità per le immagini che utilizzano tre canali di colore HDR, con un valore a 16 bit per ogni canale di colore del valore (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="2c5db-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="2c5db-117">Non è disponibile alcun supporto per un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="2c5db-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="2c5db-118">BC6H viene specificato dai valori di enumerazione del formato DXGI seguenti \_ :</span><span class="sxs-lookup"><span data-stu-id="2c5db-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="2c5db-119">**DXGI \_ FORMATTARE \_ BC6H con \_ tipo**.</span><span class="sxs-lookup"><span data-stu-id="2c5db-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="2c5db-120">**DXGI \_ FORMATTARE \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="2c5db-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="2c5db-121">Questo formato BC6H non usa un bit di segno nei valori dei canali a virgola mobile a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="2c5db-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="2c5db-122">**DXGI \_ FORMATTARE \_ BC6H \_ SF16**. Questo formato BC6H utilizza un bit di segno nei valori dei canali a virgola mobile a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="2c5db-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="2c5db-123">Il formato a virgola mobile a 16 bit per i canali dei colori è spesso definito formato a virgola mobile "metà".</span><span class="sxs-lookup"><span data-stu-id="2c5db-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="2c5db-124">Questo formato presenta il layout di bit seguente:</span><span class="sxs-lookup"><span data-stu-id="2c5db-124">This format has the following bit layout:</span></span>
>
> |                       |                                                 |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="2c5db-125">UF16 (float senza segno)</span><span class="sxs-lookup"><span data-stu-id="2c5db-125">UF16 (unsigned float)</span></span> | <span data-ttu-id="2c5db-126">5 bit esponente + 11 bit mantissa</span><span class="sxs-lookup"><span data-stu-id="2c5db-126">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="2c5db-127">SF16 (float con segno)</span><span class="sxs-lookup"><span data-stu-id="2c5db-127">SF16 (signed float)</span></span>   | <span data-ttu-id="2c5db-128">1 bit di segno + 5 bit esponente + 10 mantissa bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-128">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="2c5db-129">Il formato BC6H può essere usato per le risorse di trama [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluse le matrici), Texture3D o TextureCube (incluse le matrici).</span><span class="sxs-lookup"><span data-stu-id="2c5db-129">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="2c5db-130">Analogamente, questo formato si applica a qualsiasi superficie mappa MIP associata a tali risorse.</span><span class="sxs-lookup"><span data-stu-id="2c5db-130">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="2c5db-131">BC6H usa una dimensione fissa a blocchi di 16 byte (128 bit) e una dimensione del riquadro fissa di Texel 4x4.</span><span class="sxs-lookup"><span data-stu-id="2c5db-131">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="2c5db-132">Come per i formati BC precedenti, le immagini di trama più grandi delle dimensioni del riquadro supportate (4x4) vengono compresse usando più blocchi.</span><span class="sxs-lookup"><span data-stu-id="2c5db-132">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="2c5db-133">Questa identità di indirizzamento si applica anche alle immagini tridimensionali, alle mappe MIP, CubeMaps e alle matrici di trama.</span><span class="sxs-lookup"><span data-stu-id="2c5db-133">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="2c5db-134">Tutti i riquadri immagine devono avere lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="2c5db-134">All image tiles must be of the same format.</span></span>

<span data-ttu-id="2c5db-135">Di seguito sono riportate alcune note importanti sul formato BC6H:</span><span class="sxs-lookup"><span data-stu-id="2c5db-135">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="2c5db-136">BC6H supporta la denormalizzazione a virgola mobile, ma non supporta INF (Infinity) e NaN (non un numero).</span><span class="sxs-lookup"><span data-stu-id="2c5db-136">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="2c5db-137">L'eccezione è la modalità con segno di BC6H (DXGI \_ Format \_ BC6H \_ SF16), che supporta-inf (Infinity negativo).</span><span class="sxs-lookup"><span data-stu-id="2c5db-137">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="2c5db-138">Si noti che questo supporto per-INF è semplicemente un elemento del formato stesso e non è supportato in modo specifico dai codificatori per questo formato.</span><span class="sxs-lookup"><span data-stu-id="2c5db-138">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="2c5db-139">In generale, quando i codificatori incontrano i dati di input INF (positivi o negativi) o NaN, devono \\ convertire i dati nel valore di rappresentazione non inf massimo consentito ed eseguire il mapping di Nan a 0 prima della compressione.</span><span class="sxs-lookup"><span data-stu-id="2c5db-139">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="2c5db-140">BC6H non supporta un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="2c5db-140">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="2c5db-141">Il decodificatore BC6H esegue la decompressione prima di eseguire il filtro della trama.</span><span class="sxs-lookup"><span data-stu-id="2c5db-141">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="2c5db-142">La decompressione di BC6H deve essere leggermente precisa; ovvero, l'hardware deve restituire risultati identici a quelli descritti in questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="2c5db-142">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="2c5db-143">Implementazione di BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-143">BC6H Implementation</span></span>

<span data-ttu-id="2c5db-144">Un blocco BC6H è costituito da bit in modalità, endpoint compressi, indici compressi e un indice di partizione facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2c5db-144">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="2c5db-145">Questo formato specifica 14 modalità diverse.</span><span class="sxs-lookup"><span data-stu-id="2c5db-145">This format specifies 14 different modes.</span></span>

<span data-ttu-id="2c5db-146">Il colore di un endpoint viene archiviato come tripletta RGB.</span><span class="sxs-lookup"><span data-stu-id="2c5db-146">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="2c5db-147">BC6H definisce una tavolozza di colori su una linea approssimativa tra diversi endpoint di colore definiti.</span><span class="sxs-lookup"><span data-stu-id="2c5db-147">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="2c5db-148">Inoltre, a seconda della modalità, un riquadro può essere suddiviso in due aree o trattato come una singola area, in cui un riquadro a due aree dispone di un set separato di endpoint dei colori per ogni area.</span><span class="sxs-lookup"><span data-stu-id="2c5db-148">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="2c5db-149">BC6H archivia un indice tavolozza per Texel.</span><span class="sxs-lookup"><span data-stu-id="2c5db-149">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="2c5db-150">Nel caso di due aree sono disponibili 32 partizioni possibili.</span><span class="sxs-lookup"><span data-stu-id="2c5db-150">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="2c5db-151">Decodifica del formato BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-151">Decoding the BC6H Format</span></span>

<span data-ttu-id="2c5db-152">Lo pseudocodice seguente illustra i passaggi per decomprimere il pixel in corrispondenza di (x, y) in base al blocco BC6H a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="2c5db-152">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

<span data-ttu-id="2c5db-153">La tabella seguente contiene il numero di bit e i valori per ognuno dei 14 formati possibili per i blocchi BC6H.</span><span class="sxs-lookup"><span data-stu-id="2c5db-153">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="2c5db-154">Modalità</span><span class="sxs-lookup"><span data-stu-id="2c5db-154">Mode</span></span> | <span data-ttu-id="2c5db-155">Indici di partizione</span><span class="sxs-lookup"><span data-stu-id="2c5db-155">Partition Indices</span></span> | <span data-ttu-id="2c5db-156">Partition</span><span class="sxs-lookup"><span data-stu-id="2c5db-156">Partition</span></span> | <span data-ttu-id="2c5db-157">Endpoint colori</span><span class="sxs-lookup"><span data-stu-id="2c5db-157">Color Endpoints</span></span>                  | <span data-ttu-id="2c5db-158">Bit della modalità</span><span class="sxs-lookup"><span data-stu-id="2c5db-158">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="2c5db-159">1</span><span class="sxs-lookup"><span data-stu-id="2c5db-159">1</span></span>    | <span data-ttu-id="2c5db-160">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-160">46 bits</span></span>           | <span data-ttu-id="2c5db-161">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-161">5 bits</span></span>    | <span data-ttu-id="2c5db-162">75 bit (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="2c5db-162">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="2c5db-163">2 bit (00)</span><span class="sxs-lookup"><span data-stu-id="2c5db-163">2 bits (00)</span></span>    |
| <span data-ttu-id="2c5db-164">2</span><span class="sxs-lookup"><span data-stu-id="2c5db-164">2</span></span>    | <span data-ttu-id="2c5db-165">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-165">46 bits</span></span>           | <span data-ttu-id="2c5db-166">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-166">5 bits</span></span>    | <span data-ttu-id="2c5db-167">75 bit (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="2c5db-167">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="2c5db-168">2 bit (01)</span><span class="sxs-lookup"><span data-stu-id="2c5db-168">2 bits (01)</span></span>    |
| <span data-ttu-id="2c5db-169">3</span><span class="sxs-lookup"><span data-stu-id="2c5db-169">3</span></span>    | <span data-ttu-id="2c5db-170">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-170">46 bits</span></span>           | <span data-ttu-id="2c5db-171">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-171">5 bits</span></span>    | <span data-ttu-id="2c5db-172">72 bit (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="2c5db-172">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="2c5db-173">5 bit (00010)</span><span class="sxs-lookup"><span data-stu-id="2c5db-173">5 bits (00010)</span></span> |
| <span data-ttu-id="2c5db-174">4</span><span class="sxs-lookup"><span data-stu-id="2c5db-174">4</span></span>    | <span data-ttu-id="2c5db-175">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-175">46 bits</span></span>           | <span data-ttu-id="2c5db-176">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-176">5 bits</span></span>    | <span data-ttu-id="2c5db-177">72 bit (11,444, 11,555, 11,444)</span><span class="sxs-lookup"><span data-stu-id="2c5db-177">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="2c5db-178">5 bit (00110)</span><span class="sxs-lookup"><span data-stu-id="2c5db-178">5 bits (00110)</span></span> |
| <span data-ttu-id="2c5db-179">5</span><span class="sxs-lookup"><span data-stu-id="2c5db-179">5</span></span>    | <span data-ttu-id="2c5db-180">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-180">46 bits</span></span>           | <span data-ttu-id="2c5db-181">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-181">5 bits</span></span>    | <span data-ttu-id="2c5db-182">72 bit (11,444, 11,444, 11,555)</span><span class="sxs-lookup"><span data-stu-id="2c5db-182">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="2c5db-183">5 bit (01010)</span><span class="sxs-lookup"><span data-stu-id="2c5db-183">5 bits (01010)</span></span> |
| <span data-ttu-id="2c5db-184">6</span><span class="sxs-lookup"><span data-stu-id="2c5db-184">6</span></span>    | <span data-ttu-id="2c5db-185">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-185">46 bits</span></span>           | <span data-ttu-id="2c5db-186">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-186">5 bits</span></span>    | <span data-ttu-id="2c5db-187">72 bit (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="2c5db-187">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="2c5db-188">5 bit (01110)</span><span class="sxs-lookup"><span data-stu-id="2c5db-188">5 bits (01110)</span></span> |
| <span data-ttu-id="2c5db-189">7</span><span class="sxs-lookup"><span data-stu-id="2c5db-189">7</span></span>    | <span data-ttu-id="2c5db-190">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-190">46 bits</span></span>           | <span data-ttu-id="2c5db-191">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-191">5 bits</span></span>    | <span data-ttu-id="2c5db-192">72 bit (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="2c5db-192">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="2c5db-193">5 bit (10010)</span><span class="sxs-lookup"><span data-stu-id="2c5db-193">5 bits (10010)</span></span> |
| <span data-ttu-id="2c5db-194">8</span><span class="sxs-lookup"><span data-stu-id="2c5db-194">8</span></span>    | <span data-ttu-id="2c5db-195">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-195">46 bits</span></span>           | <span data-ttu-id="2c5db-196">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-196">5 bits</span></span>    | <span data-ttu-id="2c5db-197">72 bit (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="2c5db-197">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="2c5db-198">5 bit (10110)</span><span class="sxs-lookup"><span data-stu-id="2c5db-198">5 bits (10110)</span></span> |
| <span data-ttu-id="2c5db-199">9</span><span class="sxs-lookup"><span data-stu-id="2c5db-199">9</span></span>    | <span data-ttu-id="2c5db-200">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-200">46 bits</span></span>           | <span data-ttu-id="2c5db-201">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-201">5 bits</span></span>    | <span data-ttu-id="2c5db-202">72 bit (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="2c5db-202">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="2c5db-203">5 bit (11010)</span><span class="sxs-lookup"><span data-stu-id="2c5db-203">5 bits (11010)</span></span> |
| <span data-ttu-id="2c5db-204">10</span><span class="sxs-lookup"><span data-stu-id="2c5db-204">10</span></span>   | <span data-ttu-id="2c5db-205">46 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-205">46 bits</span></span>           | <span data-ttu-id="2c5db-206">5 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-206">5 bits</span></span>    | <span data-ttu-id="2c5db-207">72 bit (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="2c5db-207">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="2c5db-208">5 bit (11110)</span><span class="sxs-lookup"><span data-stu-id="2c5db-208">5 bits (11110)</span></span> |
| <span data-ttu-id="2c5db-209">11</span><span class="sxs-lookup"><span data-stu-id="2c5db-209">11</span></span>   | <span data-ttu-id="2c5db-210">63 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-210">63 bits</span></span>           | <span data-ttu-id="2c5db-211">0 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-211">0 bits</span></span>    | <span data-ttu-id="2c5db-212">60 bit (10,10, 10,10, 10,10)</span><span class="sxs-lookup"><span data-stu-id="2c5db-212">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="2c5db-213">5 bit (00011)</span><span class="sxs-lookup"><span data-stu-id="2c5db-213">5 bits (00011)</span></span> |
| <span data-ttu-id="2c5db-214">12</span><span class="sxs-lookup"><span data-stu-id="2c5db-214">12</span></span>   | <span data-ttu-id="2c5db-215">63 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-215">63 bits</span></span>           | <span data-ttu-id="2c5db-216">0 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-216">0 bits</span></span>    | <span data-ttu-id="2c5db-217">60 bit (11,9, 11,9, 11,9)</span><span class="sxs-lookup"><span data-stu-id="2c5db-217">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="2c5db-218">5 bit (00111)</span><span class="sxs-lookup"><span data-stu-id="2c5db-218">5 bits (00111)</span></span> |
| <span data-ttu-id="2c5db-219">13</span><span class="sxs-lookup"><span data-stu-id="2c5db-219">13</span></span>   | <span data-ttu-id="2c5db-220">63 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-220">63 bits</span></span>           | <span data-ttu-id="2c5db-221">0 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-221">0 bits</span></span>    | <span data-ttu-id="2c5db-222">60 bit (12,8, 12,8, 12,8)</span><span class="sxs-lookup"><span data-stu-id="2c5db-222">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="2c5db-223">5 bit (01011)</span><span class="sxs-lookup"><span data-stu-id="2c5db-223">5 bits (01011)</span></span> |
| <span data-ttu-id="2c5db-224">14</span><span class="sxs-lookup"><span data-stu-id="2c5db-224">14</span></span>   | <span data-ttu-id="2c5db-225">63 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-225">63 bits</span></span>           | <span data-ttu-id="2c5db-226">0 bit</span><span class="sxs-lookup"><span data-stu-id="2c5db-226">0 bits</span></span>    | <span data-ttu-id="2c5db-227">60 bit (16,4, 16,4, 16,4)</span><span class="sxs-lookup"><span data-stu-id="2c5db-227">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="2c5db-228">5 bit (01111)</span><span class="sxs-lookup"><span data-stu-id="2c5db-228">5 bits (01111)</span></span> |



 

<span data-ttu-id="2c5db-229">Ogni formato in questa tabella può essere identificato in modo univoco dai bit in modalità.</span><span class="sxs-lookup"><span data-stu-id="2c5db-229">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="2c5db-230">Le prime dieci modalità vengono usate per i riquadri a due aree e il campo di bit della modalità può essere lungo due o cinque bit.</span><span class="sxs-lookup"><span data-stu-id="2c5db-230">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="2c5db-231">Questi blocchi hanno anche campi per gli endpoint dei colori compressi (72 o 75 bit), la partizione (5 bit) e gli indici di partizione (46 bit).</span><span class="sxs-lookup"><span data-stu-id="2c5db-231">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="2c5db-232">Per gli endpoint di colore compressi, i valori della tabella precedente annotano la precisione degli endpoint RGB archiviati e il numero di bit usati per ogni valore di colore.</span><span class="sxs-lookup"><span data-stu-id="2c5db-232">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="2c5db-233">La modalità 3, ad esempio, specifica un livello di precisione dell'endpoint di colore 11 e il numero di bit utilizzati per archiviare i valori Delta degli endpoint trasformati per i colori rosso, blu e verde (5, 4 e 4 rispettivamente).</span><span class="sxs-lookup"><span data-stu-id="2c5db-233">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="2c5db-234">La modalità 10 non utilizza la compressione delta e archivia invece tutti e quattro gli endpoint dei colori in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="2c5db-234">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="2c5db-235">Le ultime quattro modalità di blocco vengono usate per i riquadri di un'area, in cui il campo modalità è a 5 bit.</span><span class="sxs-lookup"><span data-stu-id="2c5db-235">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="2c5db-236">Questi blocchi hanno campi per gli endpoint (60 bit) e gli indici compressi (63 bit).</span><span class="sxs-lookup"><span data-stu-id="2c5db-236">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="2c5db-237">La modalità 11 (come la modalità 10) non usa la compressione delta e archivia invece entrambi gli endpoint dei colori in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="2c5db-237">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="2c5db-238">Le modalità 10011, 10111, 11011 e 11111 (non visualizzate) sono riservate.</span><span class="sxs-lookup"><span data-stu-id="2c5db-238">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="2c5db-239">Non usarli nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="2c5db-239">Do not use these in your encoder.</span></span> <span data-ttu-id="2c5db-240">Se all'hardware vengono passati blocchi con una di queste modalità, il blocco decompresso risultante deve contenere tutti gli zeri in tutti i canali tranne il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="2c5db-240">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="2c5db-241">Per BC6H, il canale alfa deve sempre restituire 1,0 indipendentemente dalla modalità.</span><span class="sxs-lookup"><span data-stu-id="2c5db-241">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="2c5db-242">Set di partizioni BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-242">BC6H Partition Set</span></span>

<span data-ttu-id="2c5db-243">Sono disponibili 32 set di partizioni possibili per un riquadro a due aree, definiti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2c5db-243">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="2c5db-244">Ogni blocco 4x4 rappresenta una singola forma.</span><span class="sxs-lookup"><span data-stu-id="2c5db-244">Each 4x4 block represents a single shape.</span></span>

![tabella dei set di partizioni bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="2c5db-246">In questa tabella di set di partizioni, la voce in grassetto e sottolineata è il percorso dell'indice di correzione per il subset 1 (specificato con un bit meno).</span><span class="sxs-lookup"><span data-stu-id="2c5db-246">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="2c5db-247">L'indice di correzione per il subset 0 è sempre indice 0, perché il partizionamento è sempre disposto in modo che l'indice 0 sia sempre nel subset 0.</span><span class="sxs-lookup"><span data-stu-id="2c5db-247">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="2c5db-248">L'ordine della partizione va dalla parte superiore sinistra alla parte inferiore destra, andando verso sinistra verso destra e quindi dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="2c5db-248">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="2c5db-249">Formato dell'endpoint compresso BC6H</span><span class="sxs-lookup"><span data-stu-id="2c5db-249">BC6H Compressed Endpoint Format</span></span>

![campi di bit per i formati di endpoint compressi bc6h](images/bc6h-headers-med.png)

<span data-ttu-id="2c5db-251">Questa tabella mostra i campi di bit per gli endpoint compressi come funzione del formato dell'endpoint, con ogni colonna che specifica una codifica e ogni riga che specifica un campo di bit.</span><span class="sxs-lookup"><span data-stu-id="2c5db-251">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="2c5db-252">Questo approccio richiede 82 bit per i riquadri a due aree e 65 bit per i riquadri di un'area.</span><span class="sxs-lookup"><span data-stu-id="2c5db-252">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="2c5db-253">Ad esempio, i primi 5 bit per la codifica 1-Region \[ 16 4 \] precedente (in particolare la colonna più a destra) sono bits m \[ 4:0 \] , i 10 bit successivi sono bits RW \[ 9:0 \] e così via con gli ultimi 6 bit che contengono BW \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="2c5db-253">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="2c5db-254">I nomi dei campi nella tabella precedente sono definiti come segue:</span><span class="sxs-lookup"><span data-stu-id="2c5db-254">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="2c5db-255">Campo</span><span class="sxs-lookup"><span data-stu-id="2c5db-255">Field</span></span> | <span data-ttu-id="2c5db-256">Variabile</span><span class="sxs-lookup"><span data-stu-id="2c5db-256">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="2c5db-257">m</span><span class="sxs-lookup"><span data-stu-id="2c5db-257">m</span></span>     | <span data-ttu-id="2c5db-258">mode</span><span class="sxs-lookup"><span data-stu-id="2c5db-258">mode</span></span>              |
| <span data-ttu-id="2c5db-259">d</span><span class="sxs-lookup"><span data-stu-id="2c5db-259">d</span></span>     | <span data-ttu-id="2c5db-260">Indice delle forme</span><span class="sxs-lookup"><span data-stu-id="2c5db-260">shape index</span></span>       |
| <span data-ttu-id="2c5db-261">RW</span><span class="sxs-lookup"><span data-stu-id="2c5db-261">rw</span></span>    | <span data-ttu-id="2c5db-262">endpt \[ 0 \] . \[0\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-262">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="2c5db-263">RX</span><span class="sxs-lookup"><span data-stu-id="2c5db-263">rx</span></span>    | <span data-ttu-id="2c5db-264">endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-264">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="2c5db-265">Ry</span><span class="sxs-lookup"><span data-stu-id="2c5db-265">ry</span></span>    | <span data-ttu-id="2c5db-266">endpt \[ 1 \] . \[0\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-266">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="2c5db-267">RZ</span><span class="sxs-lookup"><span data-stu-id="2c5db-267">rz</span></span>    | <span data-ttu-id="2c5db-268">endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-268">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="2c5db-269">GW</span><span class="sxs-lookup"><span data-stu-id="2c5db-269">gw</span></span>    | <span data-ttu-id="2c5db-270">endpt \[ 0 \] . \[1\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-270">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="2c5db-271">GX</span><span class="sxs-lookup"><span data-stu-id="2c5db-271">gx</span></span>    | <span data-ttu-id="2c5db-272">endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-272">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="2c5db-273">GY (</span><span class="sxs-lookup"><span data-stu-id="2c5db-273">gy</span></span>    | <span data-ttu-id="2c5db-274">endpt \[ 1 \] . \[1\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-274">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="2c5db-275">GZ</span><span class="sxs-lookup"><span data-stu-id="2c5db-275">gz</span></span>    | <span data-ttu-id="2c5db-276">endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-276">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="2c5db-277">BW</span><span class="sxs-lookup"><span data-stu-id="2c5db-277">bw</span></span>    | <span data-ttu-id="2c5db-278">endpt \[ 0 \] . \[2\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-278">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="2c5db-279">BX</span><span class="sxs-lookup"><span data-stu-id="2c5db-279">bx</span></span>    | <span data-ttu-id="2c5db-280">endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-280">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="2c5db-281">by</span><span class="sxs-lookup"><span data-stu-id="2c5db-281">by</span></span>    | <span data-ttu-id="2c5db-282">endpt \[ 1 \] . \[2\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-282">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="2c5db-283">BZ</span><span class="sxs-lookup"><span data-stu-id="2c5db-283">bz</span></span>    | <span data-ttu-id="2c5db-284">endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2c5db-284">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="2c5db-285">Endpt \[ i \] , dove i è 0 o 1, fa riferimento rispettivamente al 0A o al primo set di endpoint.</span><span class="sxs-lookup"><span data-stu-id="2c5db-285">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="2c5db-286">Estensione del segno per i valori dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="2c5db-286">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="2c5db-287">Per i riquadri a due aree sono disponibili quattro valori di endpoint che possono essere firmati come esteso.</span><span class="sxs-lookup"><span data-stu-id="2c5db-287">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="2c5db-288">Endpt \[ 0 \] . Un oggetto è firmato solo se il formato è firmato; gli altri endpoint sono firmati solo se l'endpoint è stato trasformato o se il formato è firmato.</span><span class="sxs-lookup"><span data-stu-id="2c5db-288">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="2c5db-289">Il codice seguente illustra l'algoritmo per estendere il segno dei valori degli endpoint a due aree.</span><span class="sxs-lookup"><span data-stu-id="2c5db-289">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

<span data-ttu-id="2c5db-290">Per i riquadri a una regione, il comportamento è lo stesso, ma solo con endpt \[ 1 \] rimosso.</span><span class="sxs-lookup"><span data-stu-id="2c5db-290">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="2c5db-291">Trasforma Inversion per i valori dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="2c5db-291">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="2c5db-292">Per i riquadri a due aree, la trasformazione applica l'inverso della codifica delle differenze, aggiungendo il valore di base in endpt \[ 0 \] . Un oggetto alle altre tre voci per un totale di 9 operazioni di aggiunta.</span><span class="sxs-lookup"><span data-stu-id="2c5db-292">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="2c5db-293">Nell'immagine seguente il valore di base è rappresentato come "a0" e presenta la massima precisione a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="2c5db-293">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="2c5db-294">"A1," B0 "e" B1 "sono tutti i Delta calcolati dal valore di ancoraggio e questi valori Delta sono rappresentati con una precisione inferiore.</span><span class="sxs-lookup"><span data-stu-id="2c5db-294">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="2c5db-295">(A0 corrisponde a endpt \[ 0 \] . , B0 corrisponde a endpt \[ 0 \] . B, a1 corrisponde a endpt \[ 1 \] . A e B1 corrisponde a endpt \[ 1 \] . B.</span><span class="sxs-lookup"><span data-stu-id="2c5db-295">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![calcolo dei valori degli endpoint di trasformazione inversione](images/bc6h-transform-inverse.png)

<span data-ttu-id="2c5db-297">Per i riquadri a una regione è presente un solo offset Delta e pertanto solo 3 operazioni di aggiunta.</span><span class="sxs-lookup"><span data-stu-id="2c5db-297">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="2c5db-298">Il decompressore deve garantire che i risultati della trasformazione inversa non ridurrà l'overflow della precisione di endpt \[ 0 \] . a.</span><span class="sxs-lookup"><span data-stu-id="2c5db-298">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="2c5db-299">In caso di overflow, i valori risultanti dalla trasformazione inversa devono essere racchiusi nello stesso numero di bit.</span><span class="sxs-lookup"><span data-stu-id="2c5db-299">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="2c5db-300">Se la precisione di a0 è "p" bit, l'algoritmo di trasformazione è:</span><span class="sxs-lookup"><span data-stu-id="2c5db-300">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="2c5db-301">Per i formati firmati, anche i risultati del calcolo delta devono essere con estensione Sign.</span><span class="sxs-lookup"><span data-stu-id="2c5db-301">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="2c5db-302">Se l'operazione di estensione del segno considera l'estensione di entrambi i segni, dove 0 è positivo e 1 è negativo, l'estensione del segno 0 gestisce il morsetto sopra riportato.</span><span class="sxs-lookup"><span data-stu-id="2c5db-302">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="2c5db-303">In modo analogo, dopo il morsetto precedente, solo un valore pari a 1 (negativo) deve essere firmato come esteso.</span><span class="sxs-lookup"><span data-stu-id="2c5db-303">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="2c5db-304">Dequantizzazione degli endpoint dei colori</span><span class="sxs-lookup"><span data-stu-id="2c5db-304">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="2c5db-305">Considerati gli endpoint non compressi, il passaggio successivo consiste nell'eseguire una dequantizzazione iniziale degli endpoint dei colori.</span><span class="sxs-lookup"><span data-stu-id="2c5db-305">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="2c5db-306">Questa operazione comporta tre passaggi:</span><span class="sxs-lookup"><span data-stu-id="2c5db-306">This involves three steps:</span></span>

-   <span data-ttu-id="2c5db-307">Un errore di quantizzazione delle tavolozze dei colori</span><span class="sxs-lookup"><span data-stu-id="2c5db-307">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="2c5db-308">Interpolazione delle tavolozze</span><span class="sxs-lookup"><span data-stu-id="2c5db-308">Interpolation of the palettes</span></span>
-   <span data-ttu-id="2c5db-309">Finalizzazione dell'unquantizzazione</span><span class="sxs-lookup"><span data-stu-id="2c5db-309">Unquantization finalization</span></span>

<span data-ttu-id="2c5db-310">Separando il processo di dequantizzazione in due parti (la dequantità della tavolozza dei colori prima dell'interpolazione e l'imquantizzazione finale dopo l'interpolazione) riduce il numero di operazioni di moltiplicazione richieste rispetto a un processo di unquantizzazione completo prima dell'interpolazione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2c5db-310">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="2c5db-311">Il codice seguente illustra il processo di recupero delle stime dei valori di colore originali a 16 bit e quindi l'uso dei valori di peso forniti per aggiungere 6 valori di colore aggiuntivi alla tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2c5db-311">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="2c5db-312">Viene eseguita la stessa operazione su ogni canale.</span><span class="sxs-lookup"><span data-stu-id="2c5db-312">The same operation is performed on each channel.</span></span>

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

<span data-ttu-id="2c5db-313">Nell'esempio di codice successivo viene illustrato il processo di interpolazione, con le osservazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c5db-313">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="2c5db-314">Poiché l'intervallo completo dei valori di colore per la funzione **unquantizzate** (sotto) è compreso tra-32768 e 65535, l'interpolatore viene implementato utilizzando l'aritmetica con segno a 17 bit.</span><span class="sxs-lookup"><span data-stu-id="2c5db-314">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="2c5db-315">Dopo l'interpolazione, i valori vengono passati alla funzione di **\_ unquantizzate Finish** (descritta nel terzo esempio in questa sezione), che applica il ridimensionamento finale.</span><span class="sxs-lookup"><span data-stu-id="2c5db-315">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="2c5db-316">Tutti i decompressori hardware sono necessari per restituire risultati con precisione in bit con queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="2c5db-316">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

<span data-ttu-id="2c5db-317">il **termine \_ unquantizzate** viene chiamato dopo l'interpolazione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2c5db-317">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="2c5db-318">La funzione **unquantizzate** posticipa il ridimensionamento di 31/32 per la firma di 31/64 per l'oggetto senza segno.</span><span class="sxs-lookup"><span data-stu-id="2c5db-318">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="2c5db-319">Questo comportamento è necessario per ottenere il valore finale in un intervallo di tempo valido (-0x7BFF ~ 0x7BFF) dopo che l'interpolazione della tavolozza è stata completata per ridurre il numero di moltiplicazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="2c5db-319">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="2c5db-320">**Finish \_ unquantizzate** applica il ridimensionamento finale e restituisce un valore **short senza segno** che viene reinterpretato in **metà**.</span><span class="sxs-lookup"><span data-stu-id="2c5db-320">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="2c5db-321">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c5db-321">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c5db-322">Compressione dei blocchi di trama in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2c5db-322">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 