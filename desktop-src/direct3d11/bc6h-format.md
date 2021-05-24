---
title: Formato BC6H
description: Il formato BC6H è un formato di compressione trame progettato per supportare spazi colori HDR (High Dynamic Range) nei dati di origine.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ea15e0275bc478c0708ce08f531d8888a3c84d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335225"
---
# <a name="bc6h-format"></a><span data-ttu-id="1f8f2-105">Formato BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-105">BC6H Format</span></span>

<span data-ttu-id="1f8f2-106">Il formato BC6H è un formato di compressione trame progettato per supportare spazi colori HDR (High Dynamic Range) nei dati di origine.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="1f8f2-107">Informazioni su BC6H/DXGI \_ FORMAT \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="1f8f2-108">Implementazione di BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="1f8f2-109">Decodifica del formato BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="1f8f2-110">Formato dell'endpoint compresso BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="1f8f2-111">Estensione della firma per i valori dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="1f8f2-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="1f8f2-112">Inversione della trasformazione per i valori dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="1f8f2-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="1f8f2-113">Unquantization of Color Endpoints</span><span class="sxs-lookup"><span data-stu-id="1f8f2-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="1f8f2-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f8f2-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="1f8f2-115">Informazioni su BC6H/DXGI \_ FORMAT \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="1f8f2-116">Il formato BC6H offre una compressione di alta qualità per le immagini che usano tre canali di colori HDR, con un valore a 16 bit per ogni canale di colore del valore (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="1f8f2-117">Non è disponibile alcun supporto per un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="1f8f2-118">BC6H è specificato dai valori di enumerazione DXGI \_ FORMAT seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="1f8f2-119">**DXGI \_ FORMAT \_ BC6H \_ TYPELESS**.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="1f8f2-120">**DXGI \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="1f8f2-121">Questo formato BC6H non usa un bit di segno nei valori del canale di colore a virgola mobile a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="1f8f2-122">**DXGI \_ FORMAT \_ BC6H \_ SF16**. Questo formato BC6H usa un bit di segno nei valori del canale di colore a virgola mobile a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="1f8f2-123">Il formato a virgola mobile a 16 bit per i canali di colori viene spesso definito formato a virgola mobile "a metà".</span><span class="sxs-lookup"><span data-stu-id="1f8f2-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="1f8f2-124">Questo formato ha il layout di bit seguente:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-124">This format has the following bit layout:</span></span>
>
> |  <span data-ttu-id="1f8f2-125">Formato</span><span class="sxs-lookup"><span data-stu-id="1f8f2-125">Format</span></span>                     | <span data-ttu-id="1f8f2-126">Layout di bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-126">Bit layout</span></span>                                                |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="1f8f2-127">UF16 (unsigned float)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-127">UF16 (unsigned float)</span></span> | <span data-ttu-id="1f8f2-128">5 bit dell'esponente + 11 bit di mantissa</span><span class="sxs-lookup"><span data-stu-id="1f8f2-128">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="1f8f2-129">SF16 (valore float con segno)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-129">SF16 (signed float)</span></span>   | <span data-ttu-id="1f8f2-130">Bit di 1 segno + 5 bit dell'esponente + 10 bit di mantissa</span><span class="sxs-lookup"><span data-stu-id="1f8f2-130">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="1f8f2-131">Il formato BC6H può essere usato per le risorse [trama Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluse le matrici), Texture3D o TextureCube (incluse le matrici).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-131">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="1f8f2-132">Analogamente, questo formato si applica a qualsiasi superficie mappa MIP associata a queste risorse.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-132">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="1f8f2-133">BC6H usa una dimensione di blocco fissa di 16 byte (128 bit) e una dimensione di riquadro fissa di 4x4 texel.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-133">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="1f8f2-134">Come per i formati BC precedenti, le immagini di trama di dimensioni superiori alle dimensioni del riquadro supportate (4x4) vengono compresse usando più blocchi.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-134">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="1f8f2-135">Questa identità di indirizzamento si applica anche a immagini tridimensionali, mappe MIP, mappe cubi e matrici di trame.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-135">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="1f8f2-136">Tutti i riquadri immagine devono avere lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-136">All image tiles must be of the same format.</span></span>

<span data-ttu-id="1f8f2-137">Alcune note importanti sul formato BC6H:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-137">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="1f8f2-138">BC6H supporta la denormalizzazione a virgola mobile, ma non supporta INF (infinito) e NaN (non un numero).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-138">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="1f8f2-139">L'eccezione è la modalità con segno di BC6H (DXGI \_ FORMAT \_ BC6H SF16), che supporta \_ -INF (infinito negativo).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-139">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="1f8f2-140">Si noti che questo supporto per -INF è semplicemente un artefatto del formato stesso e non è supportato in modo specifico dai codificatori per questo formato.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-140">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="1f8f2-141">In generale, quando i codificatori rilevano dati di input INF (positivi o negativi) o NaN, devono convertire tali dati nel valore massimo consentito per la rappresentazione non INF ed eseguire il mapping di NaN a 0 prima della \\ compressione.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-141">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="1f8f2-142">BC6H non supporta un canale alfa.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-142">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="1f8f2-143">Il decodificatore BC6H esegue la decompressione prima di eseguire il filtro trame.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-143">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="1f8f2-144">La decompressione BC6H deve essere bit accurata; ciò significa che l'hardware deve restituire risultati identici al decodificatore descritto in questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-144">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="1f8f2-145">Implementazione di BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-145">BC6H Implementation</span></span>

<span data-ttu-id="1f8f2-146">Un blocco BC6H è costituito da bit di modalità, endpoint compressi, indici compressi e un indice di partizione facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-146">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="1f8f2-147">Questo formato specifica 14 modalità diverse.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-147">This format specifies 14 different modes.</span></span>

<span data-ttu-id="1f8f2-148">Un colore dell'endpoint viene archiviato come tripletta RGB.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-148">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="1f8f2-149">BC6H definisce una tavolozza di colori su una linea approssimativa attraverso un numero di endpoint di colore definiti.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-149">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="1f8f2-150">Inoltre, a seconda della modalità, un riquadro può essere suddiviso in due aree o considerato come una singola area, in cui un riquadro a due aree ha un set separato di endpoint di colore per ogni area.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-150">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="1f8f2-151">BC6H archivia un indice della tavolozza per ogni texel.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-151">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="1f8f2-152">Nel caso di due aree, sono presenti 32 partizioni possibili.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-152">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="1f8f2-153">Decodifica del formato BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-153">Decoding the BC6H Format</span></span>

<span data-ttu-id="1f8f2-154">Lo pseudocodice seguente illustra i passaggi per decomprimere il pixel in corrispondenza di (x,y) dato il blocco BC6H a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-154">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

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

<span data-ttu-id="1f8f2-155">La tabella seguente contiene il numero di bit e i valori per ognuno dei 14 formati possibili per i blocchi BC6H.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-155">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="1f8f2-156">Mode</span><span class="sxs-lookup"><span data-stu-id="1f8f2-156">Mode</span></span> | <span data-ttu-id="1f8f2-157">Indici di partizione</span><span class="sxs-lookup"><span data-stu-id="1f8f2-157">Partition Indices</span></span> | <span data-ttu-id="1f8f2-158">Partition</span><span class="sxs-lookup"><span data-stu-id="1f8f2-158">Partition</span></span> | <span data-ttu-id="1f8f2-159">Endpoint di colore</span><span class="sxs-lookup"><span data-stu-id="1f8f2-159">Color Endpoints</span></span>                  | <span data-ttu-id="1f8f2-160">Bit di modalità</span><span class="sxs-lookup"><span data-stu-id="1f8f2-160">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="1f8f2-161">1</span><span class="sxs-lookup"><span data-stu-id="1f8f2-161">1</span></span>    | <span data-ttu-id="1f8f2-162">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-162">46 bits</span></span>           | <span data-ttu-id="1f8f2-163">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-163">5 bits</span></span>    | <span data-ttu-id="1f8f2-164">75 bit (10.555, 10.555, 10.555)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-164">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="1f8f2-165">2 bit (00)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-165">2 bits (00)</span></span>    |
| <span data-ttu-id="1f8f2-166">2</span><span class="sxs-lookup"><span data-stu-id="1f8f2-166">2</span></span>    | <span data-ttu-id="1f8f2-167">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-167">46 bits</span></span>           | <span data-ttu-id="1f8f2-168">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-168">5 bits</span></span>    | <span data-ttu-id="1f8f2-169">75 bit (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-169">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="1f8f2-170">2 bit (01)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-170">2 bits (01)</span></span>    |
| <span data-ttu-id="1f8f2-171">3</span><span class="sxs-lookup"><span data-stu-id="1f8f2-171">3</span></span>    | <span data-ttu-id="1f8f2-172">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-172">46 bits</span></span>           | <span data-ttu-id="1f8f2-173">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-173">5 bits</span></span>    | <span data-ttu-id="1f8f2-174">72 bit (11.555, 11.444, 11.444)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-174">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="1f8f2-175">5 bit (00010)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-175">5 bits (00010)</span></span> |
| <span data-ttu-id="1f8f2-176">4</span><span class="sxs-lookup"><span data-stu-id="1f8f2-176">4</span></span>    | <span data-ttu-id="1f8f2-177">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-177">46 bits</span></span>           | <span data-ttu-id="1f8f2-178">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-178">5 bits</span></span>    | <span data-ttu-id="1f8f2-179">72 bit (11.444, 11.555, 11.444)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-179">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="1f8f2-180">5 bit (00110)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-180">5 bits (00110)</span></span> |
| <span data-ttu-id="1f8f2-181">5</span><span class="sxs-lookup"><span data-stu-id="1f8f2-181">5</span></span>    | <span data-ttu-id="1f8f2-182">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-182">46 bits</span></span>           | <span data-ttu-id="1f8f2-183">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-183">5 bits</span></span>    | <span data-ttu-id="1f8f2-184">72 bit (11.444, 11.444, 11.555)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-184">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="1f8f2-185">5 bit (01010)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-185">5 bits (01010)</span></span> |
| <span data-ttu-id="1f8f2-186">6</span><span class="sxs-lookup"><span data-stu-id="1f8f2-186">6</span></span>    | <span data-ttu-id="1f8f2-187">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-187">46 bits</span></span>           | <span data-ttu-id="1f8f2-188">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-188">5 bits</span></span>    | <span data-ttu-id="1f8f2-189">72 bit (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-189">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="1f8f2-190">5 bit (01110)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-190">5 bits (01110)</span></span> |
| <span data-ttu-id="1f8f2-191">7</span><span class="sxs-lookup"><span data-stu-id="1f8f2-191">7</span></span>    | <span data-ttu-id="1f8f2-192">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-192">46 bits</span></span>           | <span data-ttu-id="1f8f2-193">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-193">5 bits</span></span>    | <span data-ttu-id="1f8f2-194">72 bit (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-194">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="1f8f2-195">5 bit (10010)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-195">5 bits (10010)</span></span> |
| <span data-ttu-id="1f8f2-196">8</span><span class="sxs-lookup"><span data-stu-id="1f8f2-196">8</span></span>    | <span data-ttu-id="1f8f2-197">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-197">46 bits</span></span>           | <span data-ttu-id="1f8f2-198">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-198">5 bits</span></span>    | <span data-ttu-id="1f8f2-199">72 bit (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-199">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="1f8f2-200">5 bit (10110)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-200">5 bits (10110)</span></span> |
| <span data-ttu-id="1f8f2-201">9</span><span class="sxs-lookup"><span data-stu-id="1f8f2-201">9</span></span>    | <span data-ttu-id="1f8f2-202">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-202">46 bits</span></span>           | <span data-ttu-id="1f8f2-203">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-203">5 bits</span></span>    | <span data-ttu-id="1f8f2-204">72 bit (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-204">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="1f8f2-205">5 bit (11010)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-205">5 bits (11010)</span></span> |
| <span data-ttu-id="1f8f2-206">10</span><span class="sxs-lookup"><span data-stu-id="1f8f2-206">10</span></span>   | <span data-ttu-id="1f8f2-207">46 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-207">46 bits</span></span>           | <span data-ttu-id="1f8f2-208">5 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-208">5 bits</span></span>    | <span data-ttu-id="1f8f2-209">72 bit (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-209">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="1f8f2-210">5 bit (11110)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-210">5 bits (11110)</span></span> |
| <span data-ttu-id="1f8f2-211">11</span><span class="sxs-lookup"><span data-stu-id="1f8f2-211">11</span></span>   | <span data-ttu-id="1f8f2-212">63 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-212">63 bits</span></span>           | <span data-ttu-id="1f8f2-213">0 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-213">0 bits</span></span>    | <span data-ttu-id="1f8f2-214">60 bit (10.10, 10.10, 10.10)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-214">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="1f8f2-215">5 bit (00011)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-215">5 bits (00011)</span></span> |
| <span data-ttu-id="1f8f2-216">12</span><span class="sxs-lookup"><span data-stu-id="1f8f2-216">12</span></span>   | <span data-ttu-id="1f8f2-217">63 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-217">63 bits</span></span>           | <span data-ttu-id="1f8f2-218">0 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-218">0 bits</span></span>    | <span data-ttu-id="1f8f2-219">60 bit (11.9, 11.9, 11.9)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-219">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="1f8f2-220">5 bit (00111)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-220">5 bits (00111)</span></span> |
| <span data-ttu-id="1f8f2-221">13</span><span class="sxs-lookup"><span data-stu-id="1f8f2-221">13</span></span>   | <span data-ttu-id="1f8f2-222">63 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-222">63 bits</span></span>           | <span data-ttu-id="1f8f2-223">0 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-223">0 bits</span></span>    | <span data-ttu-id="1f8f2-224">60 bit (12.8, 12.8, 12.8)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-224">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="1f8f2-225">5 bit (01011)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-225">5 bits (01011)</span></span> |
| <span data-ttu-id="1f8f2-226">14</span><span class="sxs-lookup"><span data-stu-id="1f8f2-226">14</span></span>   | <span data-ttu-id="1f8f2-227">63 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-227">63 bits</span></span>           | <span data-ttu-id="1f8f2-228">0 bit</span><span class="sxs-lookup"><span data-stu-id="1f8f2-228">0 bits</span></span>    | <span data-ttu-id="1f8f2-229">60 bit (16.4, 16.4, 16.4)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-229">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="1f8f2-230">5 bit (01111)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-230">5 bits (01111)</span></span> |



 

<span data-ttu-id="1f8f2-231">Ogni formato in questa tabella può essere identificato in modo univoco dai bit della modalità.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-231">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="1f8f2-232">Le prime dieci modalità vengono usate per i riquadri in due aree e il campo di bit mode può avere una lunghezza di due o cinque bit.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-232">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="1f8f2-233">Questi blocchi hanno anche campi per gli endpoint di colore compresso (72 o 75 bit), la partizione (5 bit) e gli indici di partizione (46 bit).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-233">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="1f8f2-234">Per gli endpoint di colore compressi, i valori nella tabella precedente annotare la precisione degli endpoint RGB archiviati e il numero di bit usati per ogni valore di colore.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-234">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="1f8f2-235">Ad esempio, la modalità 3 specifica un livello di precisione dell'endpoint del colore di 11 e il numero di bit usati per archiviare i valori differenziali degli endpoint trasformati per i colori rosso, blu e verde (rispettivamente 5, 4 e 4).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-235">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="1f8f2-236">La modalità 10 non usa la compressione differenziale e archivia invece tutti e quattro gli endpoint di colore in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-236">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="1f8f2-237">Le ultime quattro modalità di blocco vengono usate per i riquadri in un'area, dove il campo mode è a 5 bit.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-237">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="1f8f2-238">Questi blocchi hanno campi per gli endpoint (60 bit) e gli indici compressi (63 bit).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-238">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="1f8f2-239">La modalità 11 (come la modalità 10) non usa la compressione differenziale e archivia invece entrambi gli endpoint di colore in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-239">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="1f8f2-240">Le modalità 10011, 10111, 11011 e 11111 (non visualizzate) sono riservate.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-240">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="1f8f2-241">Non usarli nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-241">Do not use these in your encoder.</span></span> <span data-ttu-id="1f8f2-242">Se l'hardware viene passato a blocchi con una di queste modalità specificate, il blocco decompresso risultante deve contenere tutti gli zeri in tutti i canali ad eccezione del canale alfa.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-242">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="1f8f2-243">Per BC6H, il canale alfa deve sempre restituire 1.0 indipendentemente dalla modalità.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-243">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="1f8f2-244">Set di partizioni BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-244">BC6H Partition Set</span></span>

<span data-ttu-id="1f8f2-245">Sono disponibili 32 set di partizioni possibili per un riquadro a due aree e sono definiti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-245">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="1f8f2-246">Ogni blocco 4x4 rappresenta una singola forma.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-246">Each 4x4 block represents a single shape.</span></span>

![tabella dei set di partizioni bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="1f8f2-248">In questa tabella di set di partizioni, la voce in grassetto e sottolineata è la posizione dell'indice di correzione per il subset 1 (specificato con un bit in meno).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-248">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="1f8f2-249">L'indice di correzione per il subset 0 è sempre indice 0, perché il partizionamento è sempre organizzato in modo che l'indice 0 sia sempre nel subset 0.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-249">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="1f8f2-250">L'ordine delle partizioni va dall'alto a sinistra verso il basso a destra, spostandosi da sinistra a destra e quindi dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-250">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="1f8f2-251">Formato dell'endpoint compresso BC6H</span><span class="sxs-lookup"><span data-stu-id="1f8f2-251">BC6H Compressed Endpoint Format</span></span>

![campi di bit per i formati di endpoint compressi bc6h](images/bc6h-headers-med.png)

<span data-ttu-id="1f8f2-253">Questa tabella mostra i campi di bit per gli endpoint compressi come funzione del formato dell'endpoint, con ogni colonna che specifica una codifica e ogni riga che specifica un campo di bit.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-253">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="1f8f2-254">Questo approccio richiede 82 bit per i riquadri a due aree e 65 bit per i riquadri in un'area.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-254">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="1f8f2-255">Ad esempio, i primi 5 bit per la codifica a un'area 16 4 precedente (in particolare la colonna più a destra) sono bit m 4:0, i 10 bit successivi sono bit rw 9:0 e così via con gli ultimi 6 bit contenenti \[ \] \[ \] \[ \] bw \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="1f8f2-255">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="1f8f2-256">I nomi dei campi nella tabella precedente sono definiti come segue:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-256">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="1f8f2-257">Campo</span><span class="sxs-lookup"><span data-stu-id="1f8f2-257">Field</span></span> | <span data-ttu-id="1f8f2-258">Variabile</span><span class="sxs-lookup"><span data-stu-id="1f8f2-258">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="1f8f2-259">m</span><span class="sxs-lookup"><span data-stu-id="1f8f2-259">m</span></span>     | <span data-ttu-id="1f8f2-260">mode</span><span class="sxs-lookup"><span data-stu-id="1f8f2-260">mode</span></span>              |
| <span data-ttu-id="1f8f2-261">d</span><span class="sxs-lookup"><span data-stu-id="1f8f2-261">d</span></span>     | <span data-ttu-id="1f8f2-262">indice delle forme</span><span class="sxs-lookup"><span data-stu-id="1f8f2-262">shape index</span></span>       |
| <span data-ttu-id="1f8f2-263">Rw</span><span class="sxs-lookup"><span data-stu-id="1f8f2-263">rw</span></span>    | <span data-ttu-id="1f8f2-264">endpt \[ 0 \] . A \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-264">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="1f8f2-265">Rx</span><span class="sxs-lookup"><span data-stu-id="1f8f2-265">rx</span></span>    | <span data-ttu-id="1f8f2-266">endpt \[ 0 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-266">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="1f8f2-267">Ry</span><span class="sxs-lookup"><span data-stu-id="1f8f2-267">ry</span></span>    | <span data-ttu-id="1f8f2-268">endpt \[ 1 \] . A \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-268">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="1f8f2-269">Rz</span><span class="sxs-lookup"><span data-stu-id="1f8f2-269">rz</span></span>    | <span data-ttu-id="1f8f2-270">endpt \[ 1 \] . B \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-270">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="1f8f2-271">Gw</span><span class="sxs-lookup"><span data-stu-id="1f8f2-271">gw</span></span>    | <span data-ttu-id="1f8f2-272">endpt \[ 0 \] . A \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-272">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="1f8f2-273">Gx</span><span class="sxs-lookup"><span data-stu-id="1f8f2-273">gx</span></span>    | <span data-ttu-id="1f8f2-274">endpt \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-274">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="1f8f2-275">Gy</span><span class="sxs-lookup"><span data-stu-id="1f8f2-275">gy</span></span>    | <span data-ttu-id="1f8f2-276">endpt \[ 1 \] . A \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-276">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="1f8f2-277">Gz</span><span class="sxs-lookup"><span data-stu-id="1f8f2-277">gz</span></span>    | <span data-ttu-id="1f8f2-278">endpt \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-278">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="1f8f2-279">Bw</span><span class="sxs-lookup"><span data-stu-id="1f8f2-279">bw</span></span>    | <span data-ttu-id="1f8f2-280">endpt \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-280">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="1f8f2-281">Bx</span><span class="sxs-lookup"><span data-stu-id="1f8f2-281">bx</span></span>    | <span data-ttu-id="1f8f2-282">endpt \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-282">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="1f8f2-283">by</span><span class="sxs-lookup"><span data-stu-id="1f8f2-283">by</span></span>    | <span data-ttu-id="1f8f2-284">endpt \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-284">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="1f8f2-285">Bz</span><span class="sxs-lookup"><span data-stu-id="1f8f2-285">bz</span></span>    | <span data-ttu-id="1f8f2-286">endpt \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="1f8f2-286">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="1f8f2-287">Endpt i , dove i è 0 o 1, fa riferimento rispettivamente al \[ \] 0° o 1° set di endpoint.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-287">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="1f8f2-288">Estensione della firma per i valori dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="1f8f2-288">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="1f8f2-289">Per i riquadri in due aree, sono disponibili quattro valori di endpoint che possono essere firmati estesi.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-289">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="1f8f2-290">Endpt \[ 0 \] . Un oggetto è firmato solo se il formato è un formato con segno; gli altri endpoint vengono firmati solo se l'endpoint è stato trasformato o se il formato è un formato con segno.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-290">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="1f8f2-291">Il codice seguente illustra l'algoritmo per l'estensione del segno dei valori dell'endpoint a due aree.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-291">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

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

<span data-ttu-id="1f8f2-292">Per i riquadri di un'area, il comportamento è lo stesso, solo con endpt \[ 1 \] rimosso.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-292">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

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

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="1f8f2-293">Inversione della trasformazione per i valori dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="1f8f2-293">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="1f8f2-294">Per i riquadri a due aree, la trasformazione applica l'inverso della codifica delle differenze, aggiungendo il valore di base a endpt \[ \] 0. Oggetto per le altre tre voci per un totale di 9 operazioni di aggiunta.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-294">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="1f8f2-295">Nell'immagine seguente il valore di base è rappresentato come "A0" e ha la precisione a virgola mobile più elevata.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-295">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="1f8f2-296">"A1", "B0" e "B1" sono tutti delta calcolati dal valore di ancoraggio e questi valori differenziali sono rappresentati con precisione inferiore.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-296">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="1f8f2-297">(A0 corrisponde a endpt \[ \] 0. A, B0 corrisponde a endpt \[ \] 0. B, A1 corrisponde a endpt \[ \] 1. A e B1 corrispondono a endpt \[ 1 \] .B.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-297">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![calcolo dei valori dell'endpoint di inversione della trasformazione](images/bc6h-transform-inverse.png)

<span data-ttu-id="1f8f2-299">Per i riquadri in un'area è presente una sola offset differenziale e quindi solo 3 operazioni di aggiunta.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-299">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="1f8f2-300">Il decompressore deve assicurarsi che i risultati della trasformazione inversa non esercitino la precisione di endpt \[ 0 \] .a.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-300">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="1f8f2-301">In caso di overflow, i valori risultanti dalla trasformazione inversa devono essere incapsulati nello stesso numero di bit.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-301">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="1f8f2-302">Se la precisione di A0 è "p", l'algoritmo di trasformazione è:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-302">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="1f8f2-303">Per i formati firmati, anche i risultati del calcolo differenziale devono essere estesi con segno.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-303">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="1f8f2-304">Se l'operazione di estensione del segno considera l'estensione di entrambi i segni, dove 0 è positivo e 1 è negativo, l'estensione del segno 0 si occupa della chiusura precedente.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-304">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="1f8f2-305">In modo equivalente, dopo la chiusura precedente, è necessario estendere solo il valore 1 (negativo).</span><span class="sxs-lookup"><span data-stu-id="1f8f2-305">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="1f8f2-306">Nonquantization of Color Endpoints (Nonquantization degli endpoint colore)</span><span class="sxs-lookup"><span data-stu-id="1f8f2-306">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="1f8f2-307">Dato gli endpoint non compressi, il passaggio successivo consiste nell'eseguire una nonquantizzazione iniziale degli endpoint di colore.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-307">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="1f8f2-308">Questa operazione comporta tre passaggi:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-308">This involves three steps:</span></span>

-   <span data-ttu-id="1f8f2-309">Nonquantizzazione delle tavolozze dei colori</span><span class="sxs-lookup"><span data-stu-id="1f8f2-309">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="1f8f2-310">Interpolazione delle tavolozze</span><span class="sxs-lookup"><span data-stu-id="1f8f2-310">Interpolation of the palettes</span></span>
-   <span data-ttu-id="1f8f2-311">Finalizzazione senzaquantization</span><span class="sxs-lookup"><span data-stu-id="1f8f2-311">Unquantization finalization</span></span>

<span data-ttu-id="1f8f2-312">La separazione del processo di nonquantizzazione in due parti (nonquantizzazione della tavolozza dei colori prima dell'interpolazione e nonquazione finale dopo l'interpolazione) riduce il numero di operazioni di moltiplicazione necessarie rispetto a un processo di nonquantizzazione completo prima dell'interpolazione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-312">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="1f8f2-313">Il codice seguente illustra il processo per recuperare le stime dei valori di colore originali a 16 bit e quindi usare i valori di spessore forniti per aggiungere altri 6 valori di colore alla tavolozza.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-313">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="1f8f2-314">La stessa operazione viene eseguita su ogni canale.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-314">The same operation is performed on each channel.</span></span>

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

<span data-ttu-id="1f8f2-315">L'esempio di codice seguente illustra il processo di interpolazione, con le osservazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f8f2-315">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="1f8f2-316">Poiché l'intera gamma di valori di colore per la funzione **unquantize** (di seguito) è compreso tra -32768 e 65535, l'interpolatore viene implementato usando l'aritmetica con segno a 17 bit.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-316">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="1f8f2-317">Dopo l'interpolazione, i valori vengono passati alla funzione **completa nonquantize \_** (descritta nel terzo esempio di questa sezione), che applica il ridimensionamento finale.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-317">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="1f8f2-318">Tutti i decompressori hardware sono necessari per restituire risultati accurati in bit con queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-318">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

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

<span data-ttu-id="1f8f2-319">**Il \_ metodo finish unquantize** viene chiamato dopo l'interpolazione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-319">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="1f8f2-320">La **funzione unquantize** posticipa il ridimensionamento di 31/32 per signed, 31/64 per unsigned.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-320">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="1f8f2-321">Questo comportamento è necessario per ottenere il valore finale nell'intervallo dimezzamento valido (-0x7BFF ~ 0x7BFF) dopo il completamento dell'interpolazione della tavolozza per ridurre il numero di moltiplicazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="1f8f2-321">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="1f8f2-322">**finish \_ unquantize applica** il ridimensionamento finale e restituisce un valore **short** senza segno che viene reinterpretato in **metà.**</span><span class="sxs-lookup"><span data-stu-id="1f8f2-322">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="1f8f2-323">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f8f2-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8f2-324">Compressione dei blocchi di trama in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1f8f2-324">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 