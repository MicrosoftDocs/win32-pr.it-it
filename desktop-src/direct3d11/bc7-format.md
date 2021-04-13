---
title: Formato BC7
description: Il formato BC7 è un formato di compressione di trama usato per la compressione di alta qualità dei dati RGB e RGBA.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b64c3d4a8b5e960077a9f33de82ff08cd4bbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399522"
---
# <a name="bc7-format"></a><span data-ttu-id="24962-103">Formato BC7</span><span class="sxs-lookup"><span data-stu-id="24962-103">BC7 Format</span></span>

<span data-ttu-id="24962-104">Il formato BC7 è un formato di compressione di trama usato per la compressione di alta qualità dei dati RGB e RGBA.</span><span class="sxs-lookup"><span data-stu-id="24962-104">The BC7 format is a texture compression format used for high-quality compression of RGB and RGBA data.</span></span>

-   [<span data-ttu-id="24962-105">Informazioni sul formato BC7/DXGI \_ \_ BC7</span><span class="sxs-lookup"><span data-stu-id="24962-105">About BC7/DXGI\_FORMAT\_BC7</span></span>](/windows)
-   [<span data-ttu-id="24962-106">Implementazione di BC7</span><span class="sxs-lookup"><span data-stu-id="24962-106">BC7 Implementation</span></span>](#bc7-implementation)
-   [<span data-ttu-id="24962-107">Decodifica del formato BC7</span><span class="sxs-lookup"><span data-stu-id="24962-107">Decoding the BC7 Format</span></span>](#decoding-the-bc7-format)
-   [<span data-ttu-id="24962-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24962-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="24962-109">Per informazioni sulle modalità di blocco del formato BC7, vedere [riferimento alla modalità di formattazione BC7](bc7-format-mode-reference.md).</span><span class="sxs-lookup"><span data-stu-id="24962-109">For info about the block modes of the BC7 format, see [BC7 Format Mode Reference](bc7-format-mode-reference.md).</span></span>

## <a name="about-bc7dxgi_format_bc7"></a><span data-ttu-id="24962-110">Informazioni sul formato BC7/DXGI \_ \_ BC7</span><span class="sxs-lookup"><span data-stu-id="24962-110">About BC7/DXGI\_FORMAT\_BC7</span></span>

<span data-ttu-id="24962-111">BC7 viene specificato dai valori di enumerazione del formato DXGI seguenti \_ :</span><span class="sxs-lookup"><span data-stu-id="24962-111">BC7 is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="24962-112">**DXGI \_ FORMATTARE \_ BC7 con \_ tipo**.</span><span class="sxs-lookup"><span data-stu-id="24962-112">**DXGI\_FORMAT\_BC7\_TYPELESS**.</span></span>
-   <span data-ttu-id="24962-113">**DXGI \_ FORMATTARE \_ BC7 \_ UNORM**.</span><span class="sxs-lookup"><span data-stu-id="24962-113">**DXGI\_FORMAT\_BC7\_UNORM**.</span></span>
-   <span data-ttu-id="24962-114">**DXGI \_ FORMATTARE \_ BC7 \_ UNORM \_ sRGB**.</span><span class="sxs-lookup"><span data-stu-id="24962-114">**DXGI\_FORMAT\_BC7\_UNORM\_SRGB**.</span></span>

<span data-ttu-id="24962-115">Il formato BC7 può essere usato per le risorse di trama [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluse le matrici), Texture3D o TextureCube (incluse le matrici).</span><span class="sxs-lookup"><span data-stu-id="24962-115">The BC7 format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="24962-116">Analogamente, questo formato si applica a qualsiasi superficie mappa MIP associata a tali risorse.</span><span class="sxs-lookup"><span data-stu-id="24962-116">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="24962-117">BC7 usa una dimensione fissa a blocchi di 16 byte (128 bit) e una dimensione del riquadro fissa di Texel 4x4.</span><span class="sxs-lookup"><span data-stu-id="24962-117">BC7 uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="24962-118">Come per i formati BC precedenti, le immagini di trama più grandi delle dimensioni del riquadro supportate (4x4) vengono compresse usando più blocchi.</span><span class="sxs-lookup"><span data-stu-id="24962-118">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="24962-119">Questa identità di indirizzamento si applica anche alle immagini tridimensionali e alle matrici MIP, CubeMaps e di trama.</span><span class="sxs-lookup"><span data-stu-id="24962-119">This addressing identity also applies to three-dimensional images and MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="24962-120">Tutti i riquadri immagine devono avere lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="24962-120">All image tiles must be of the same format.</span></span>

<span data-ttu-id="24962-121">BC7 comprime sia immagini di dati a virgola fissa a tre canali (RGB) che a quattro canali (RGBA).</span><span class="sxs-lookup"><span data-stu-id="24962-121">BC7 compresses both three-channel (RGB) and four-channel (RGBA) fixed-point data images.</span></span> <span data-ttu-id="24962-122">In genere, i dati di origine sono a 8 bit per componente colore (canale), sebbene il formato sia in grado di codificare i dati di origine con bit più alti per componente colore.</span><span class="sxs-lookup"><span data-stu-id="24962-122">Typically, source data is 8 bits per color component (channel), although the format is capable of encoding source data with higher bits per color component.</span></span> <span data-ttu-id="24962-123">Tutti i riquadri immagine devono avere lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="24962-123">All image tiles must be of the same format.</span></span>

<span data-ttu-id="24962-124">Il decodificatore BC7 esegue la decompressione prima dell'applicazione del filtro della trama.</span><span class="sxs-lookup"><span data-stu-id="24962-124">The BC7 decoder performs decompression before texture filtering is applied.</span></span>

<span data-ttu-id="24962-125">L'hardware di decompressione di BC7 deve essere leggermente accurato; ovvero, l'hardware deve restituire risultati identici ai risultati restituiti dal decodificatore descritto in questo documento.</span><span class="sxs-lookup"><span data-stu-id="24962-125">BC7 decompression hardware must be bit accurate; that is, the hardware must return results that are identical to the results returned by the decoder described in this document.</span></span>

## <a name="bc7-implementation"></a><span data-ttu-id="24962-126">Implementazione di BC7</span><span class="sxs-lookup"><span data-stu-id="24962-126">BC7 Implementation</span></span>

<span data-ttu-id="24962-127">Un'implementazione di BC7 può specificare una delle 8 modalità, con la modalità specificata nel bit meno significativo del blocco a 16 byte (128 bit).</span><span class="sxs-lookup"><span data-stu-id="24962-127">A BC7 implementation can specify one of 8 modes, with the mode specified in the least significant bit of the 16 byte (128 bit) block.</span></span> <span data-ttu-id="24962-128">La modalità è codificata da zero o più bit con un valore pari a 0 seguito da 1.</span><span class="sxs-lookup"><span data-stu-id="24962-128">The mode is encoded by zero or more bits with a value of 0 followed by a 1.</span></span>

<span data-ttu-id="24962-129">Un blocco BC7 può contenere più coppie di endpoint.</span><span class="sxs-lookup"><span data-stu-id="24962-129">A BC7 block can contain multiple endpoint pairs.</span></span> <span data-ttu-id="24962-130">Ai fini di questa documentazione, il set di indici che corrisponde a una coppia di endpoint può essere definito "subset".</span><span class="sxs-lookup"><span data-stu-id="24962-130">For the purposes of this documentation, the set of indices that correspond to an endpoint pair may be referred to as a "subset."</span></span> <span data-ttu-id="24962-131">Inoltre, in alcune modalità di blocco, la rappresentazione dell'endpoint viene codificata in un form che, ai fini di questa documentazione, deve essere denominata "RBGP", dove il bit "P" rappresenta un bit meno significativo condiviso per i componenti di colore dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="24962-131">Also, in some block modes, the endpoint representation is encoded in a form that -- again, for the purposes of this documentation -- shall be referred to as "RBGP," where the "P" bit represents a shared least significant bit for the color components of the endpoint.</span></span> <span data-ttu-id="24962-132">Se, ad esempio, la rappresentazione dell'endpoint per il formato è "RGB 5.5.5.1", l'endpoint viene interpretato come valore 6.6.6 RGB, dove lo stato del P-bit definisce il bit meno significativo di ogni componente.</span><span class="sxs-lookup"><span data-stu-id="24962-132">For example, if the endpoint representation for the format is "RGB 5.5.5.1," then the endpoint is interpreted as an RGB 6.6.6 value, where the state of the P-bit defines the least significant bit of each component.</span></span> <span data-ttu-id="24962-133">Analogamente, per i dati di origine con un canale alfa, se la rappresentazione per il formato è "RGBAP 5.5.5.5.1", l'endpoint è interepreted come RGBA 6.6.6.6.</span><span class="sxs-lookup"><span data-stu-id="24962-133">Similarly, for source data with an alpha channel, if the representation for the format is "RGBAP 5.5.5.5.1," then the endpoint is interepreted as RGBA 6.6.6.6.</span></span> <span data-ttu-id="24962-134">A seconda della modalità di blocco, è possibile specificare il bit meno significativo condiviso per entrambi gli endpoint di un subset singolarmente (2 P-bit per subset) o condivisi tra endpoint di un subset (1 P-bit per subset).</span><span class="sxs-lookup"><span data-stu-id="24962-134">Depending on the block mode, you can specify the shared least significant bit for either both endpoints of a subset individually (2 P-bits per subset), or shared between endpoints of a subset (1 P-bit per subset).</span></span>

<span data-ttu-id="24962-135">Per i blocchi BC7 che non codificano in modo esplicito il componente alfa, un blocco BC7 è costituito da bit in modalità, bit di partizione, endpoint compressi, indici compressi e un P-bit facoltativo.</span><span class="sxs-lookup"><span data-stu-id="24962-135">For BC7 blocks that don't explicitly encode the alpha component, a BC7 block consists of mode bits, partition bits, compressed endpoints, compressed indices, and an optional P-bit.</span></span> <span data-ttu-id="24962-136">In questi blocchi gli endpoint hanno una rappresentazione solo RGB e il componente alfa viene decodificato come 1,0 per tutti i Texel nei dati di origine.</span><span class="sxs-lookup"><span data-stu-id="24962-136">In these blocks the endpoints have an RGB-only representation and the alpha component is decoded as 1.0 for all texels in the source data.</span></span>

<span data-ttu-id="24962-137">Per i blocchi BC7 con componenti combinati di colore e alfa, un blocco è costituito da bit in modalità, endpoint compressi, indici compressi e bit di partizione facoltativi e un P-bit.</span><span class="sxs-lookup"><span data-stu-id="24962-137">For BC7 blocks that have combined color and alpha components, a block consists of mode bits, compressed endpoints, compressed indices, and optional partition bits and a P-bit.</span></span> <span data-ttu-id="24962-138">In questi blocchi, i colori dell'endpoint sono espressi in formato RGBA e i valori dei componenti alfa vengono interpolati insieme ai valori dei componenti dei colori.</span><span class="sxs-lookup"><span data-stu-id="24962-138">In these blocks, the endpoint colors are expressed in RGBA format, and alpha component values are interpolated alongside the color component values.</span></span>

<span data-ttu-id="24962-139">Per i blocchi BC7 con componenti di colore e alfa distinti, un blocco è costituito da bit in modalità, bit di rotazione, endpoint compressi, indici compressi e un bit del selettore di indice facoltativo.</span><span class="sxs-lookup"><span data-stu-id="24962-139">For BC7 blocks that have separate color and alpha components, a block consists of mode bits, rotation bits, compressed endpoints, compressed indices, and an optional index selector bit.</span></span> <span data-ttu-id="24962-140">Questi blocchi hanno un vettore RGB effettivo \[ R, G, B \] e un canale alfa scalare \[ a \] codificato separatamente.</span><span class="sxs-lookup"><span data-stu-id="24962-140">These blocks have an effective RGB vector \[R, G, B\] and a scalar alpha channel \[A\] separately encoded.</span></span>

<span data-ttu-id="24962-141">Nella tabella seguente sono elencati i componenti di ogni tipo di blocco.</span><span class="sxs-lookup"><span data-stu-id="24962-141">The following table lists the components of each block type.</span></span>



| <span data-ttu-id="24962-142">Il blocco BC7 contiene...</span><span class="sxs-lookup"><span data-stu-id="24962-142">BC7 block contains...</span></span>     | <span data-ttu-id="24962-143">bit della modalità</span><span class="sxs-lookup"><span data-stu-id="24962-143">mode bits</span></span> | <span data-ttu-id="24962-144">bit di rotazione</span><span class="sxs-lookup"><span data-stu-id="24962-144">rotation bits</span></span> | <span data-ttu-id="24962-145">bit selettore indice</span><span class="sxs-lookup"><span data-stu-id="24962-145">index selector bit</span></span> | <span data-ttu-id="24962-146">bit partizione</span><span class="sxs-lookup"><span data-stu-id="24962-146">partition bits</span></span> | <span data-ttu-id="24962-147">endpoint compressi</span><span class="sxs-lookup"><span data-stu-id="24962-147">compressed endpoints</span></span> | <span data-ttu-id="24962-148">P-bit</span><span class="sxs-lookup"><span data-stu-id="24962-148">P-bit</span></span>    | <span data-ttu-id="24962-149">indici compressi</span><span class="sxs-lookup"><span data-stu-id="24962-149">compressed indices</span></span> |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| <span data-ttu-id="24962-150">solo componenti colori</span><span class="sxs-lookup"><span data-stu-id="24962-150">color components only</span></span>     | <span data-ttu-id="24962-151">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-151">required</span></span>  | <span data-ttu-id="24962-152">N/D</span><span class="sxs-lookup"><span data-stu-id="24962-152">N/A</span></span>           | <span data-ttu-id="24962-153">N/D</span><span class="sxs-lookup"><span data-stu-id="24962-153">N/A</span></span>                | <span data-ttu-id="24962-154">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-154">required</span></span>       | <span data-ttu-id="24962-155">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-155">required</span></span>             | <span data-ttu-id="24962-156">facoltative</span><span class="sxs-lookup"><span data-stu-id="24962-156">optional</span></span> | <span data-ttu-id="24962-157">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-157">required</span></span>           |
| <span data-ttu-id="24962-158">colore + Alpha combinato</span><span class="sxs-lookup"><span data-stu-id="24962-158">color + alpha combined</span></span>    | <span data-ttu-id="24962-159">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-159">required</span></span>  | <span data-ttu-id="24962-160">N/D</span><span class="sxs-lookup"><span data-stu-id="24962-160">N/A</span></span>           | <span data-ttu-id="24962-161">N/D</span><span class="sxs-lookup"><span data-stu-id="24962-161">N/A</span></span>                | <span data-ttu-id="24962-162">facoltative</span><span class="sxs-lookup"><span data-stu-id="24962-162">optional</span></span>       | <span data-ttu-id="24962-163">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-163">required</span></span>             | <span data-ttu-id="24962-164">facoltative</span><span class="sxs-lookup"><span data-stu-id="24962-164">optional</span></span> | <span data-ttu-id="24962-165">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-165">required</span></span>           |
| <span data-ttu-id="24962-166">colore e alfa separati</span><span class="sxs-lookup"><span data-stu-id="24962-166">color and alpha separated</span></span> | <span data-ttu-id="24962-167">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-167">required</span></span>  | <span data-ttu-id="24962-168">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-168">required</span></span>      | <span data-ttu-id="24962-169">facoltative</span><span class="sxs-lookup"><span data-stu-id="24962-169">optional</span></span>           | <span data-ttu-id="24962-170">N/D</span><span class="sxs-lookup"><span data-stu-id="24962-170">N/A</span></span>            | <span data-ttu-id="24962-171">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-171">required</span></span>             | <span data-ttu-id="24962-172">N/D</span><span class="sxs-lookup"><span data-stu-id="24962-172">N/A</span></span>      | <span data-ttu-id="24962-173">necessario</span><span class="sxs-lookup"><span data-stu-id="24962-173">required</span></span>           |



 

<span data-ttu-id="24962-174">BC7 definisce una tavolozza di colori su una linea approssimativa tra due endpoint.</span><span class="sxs-lookup"><span data-stu-id="24962-174">BC7 defines a palette of colors on an approximate line between two endpoints.</span></span> <span data-ttu-id="24962-175">Il valore della modalità determina il numero di coppie di endpoint di interpolazione per blocco.</span><span class="sxs-lookup"><span data-stu-id="24962-175">The mode value determines the number of interpolating endpoint pairs per block.</span></span> <span data-ttu-id="24962-176">BC7 archivia un indice tavolozza per Texel.</span><span class="sxs-lookup"><span data-stu-id="24962-176">BC7 stores one palette index per texel.</span></span>

<span data-ttu-id="24962-177">Per ogni subset di indici che corrisponde a una coppia di endpoint, il codificatore corregge lo stato di un bit dei dati dell'indice compresso per quel subset.</span><span class="sxs-lookup"><span data-stu-id="24962-177">For each subset of indices that corresponds to a pair of endpoints, the encoder fixes the state of one bit of the compressed index data for that subset.</span></span> <span data-ttu-id="24962-178">Questa operazione viene eseguita scegliendo un ordine di endpoint che consente all'indice per l'indice "correzione" designato di impostare il bit più significativo su 0 e che può quindi essere ignorato, salvando un bit per ogni subset.</span><span class="sxs-lookup"><span data-stu-id="24962-178">It does so by choosing an endpoint order that allows the index for the designated "fix-up" index to set its most significant bit to 0, and which can then be discarded, saving one bit per subset.</span></span> <span data-ttu-id="24962-179">Per le modalità di blocco con un solo subset, l'indice di correzione è sempre indice 0.</span><span class="sxs-lookup"><span data-stu-id="24962-179">For block modes with only a single subset, the fix-up index is always index 0.</span></span>

## <a name="decoding-the-bc7-format"></a><span data-ttu-id="24962-180">Decodifica del formato BC7</span><span class="sxs-lookup"><span data-stu-id="24962-180">Decoding the BC7 Format</span></span>

<span data-ttu-id="24962-181">Lo pseudocodice seguente illustra i passaggi per decomprimere il pixel in corrispondenza di (x, y) in base al blocco BC7 a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="24962-181">The following pseudocode outlines the steps to decompress the pixel at (x,y) given the 16 byte BC7 block.</span></span>

``` syntax
decompress_bc7(x, y, block)
{
    mode = extract_mode(block);
    
    //decode partition data from explicit partition bits
    subset_index = 0;
    num_subsets = 1;
    
    if (mode.type == 0 OR == 1 OR == 2 OR == 3 OR == 7)
    {
        num_subsets = get_num_subsets(mode.type);
        partition_set_id = extract_partition_set_id(mode, block);
        subset_index = get_partition_index(num_subsets, partition_set_id, x, y);
    }
    
    //extract raw, compressed endpoint bits
    UINT8 endpoint_array[num_subsets][4] = extract_endpoints(mode, block);
    
    //decode endpoint color and alpha for each subset
    fully_decode_endpoints(endpoint_array, mode, block);
    
    //endpoints are now complete.
    UINT8 endpoint_start[4] = endpoint_array[2 * subset_index];
    UINT8 endpoint_end[4]   = endpoint_array[2 * subset_index + 1];
        
    //Determine the palette index for this pixel
    alpha_index     = get_alpha_index(block, mode, x, y);
    alpha_bitcount  = get_alpha_bitcount(block, mode);
    color_index     = get_color_index(block, mode, x, y);
    color_bitcount  = get_color_bitcount(block, mode);

    //determine output
    UINT8 output[4];
    output.rgb = interpolate(endpoint_start.rgb, endpoint_end.rgb, color_index, color_bitcount);
    output.a   = interpolate(endpoint_start.a,   endpoint_end.a,   alpha_index, alpha_bitcount);
    
    if (mode.type == 4 OR == 5)
    {
        //Decode the 2 color rotation bits as follows:
        // 00 – Block format is Scalar(A) Vector(RGB) - no swapping
        // 01 – Block format is Scalar(R) Vector(AGB) - swap A and R
        // 10 – Block format is Scalar(G) Vector(RAB) - swap A and G
        // 11 - Block format is Scalar(B) Vector(RGA) - swap A and B
        rotation = extract_rot_bits(mode, block);
        output = swap_channels(output, rotation);
    }
    
}
```

<span data-ttu-id="24962-182">Lo pseudocodice di seguente descrive i passaggi per decodificare completamente i componenti alfa e del colore dell'endpoint per ogni subset dato un blocco BC7 a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="24962-182">The followoing pseudocode outlines the steps to fully decode endpoint color and alpha components for each subset given a 16-byte BC7 block.</span></span>

``` syntax
fully_decode_endpoints(endpoint_array, mode, block)
{
    //first handle modes that have P-bits
    if (mode.type == 0 OR == 1 OR == 3 OR == 6 OR == 7)
    {
        for each endpoint i
        {
            //component-wise left-shift
            endpoint_array[i].rgba = endpoint_array[i].rgba << 1;
        }
        
        //if P-bit is shared
        if (mode.type == 1) 
        {
            pbit_zero = extract_pbit_zero(mode, block);
            pbit_one = extract_pbit_one(mode, block);
            
            //rgb component-wise insert pbits
            endpoint_array[0].rgb |= pbit_zero;
            endpoint_array[1].rgb |= pbit_zero;
            endpoint_array[2].rgb |= pbit_one;
            endpoint_array[3].rgb |= pbit_one;  
        }
        else //unique P-bit per endpoint
        {  
            pbit_array = extract_pbit_array(mode, block);
            for each endpoint i
            {
                endpoint_array[i].rgba |= pbit_array[i];
            }
        }
    }

    for each endpoint i
    {
        // Color_component_precision & alpha_component_precision includes pbit
        // left shift endpoint components so that their MSB lies in bit 7
        endpoint_array[i].rgb = endpoint_array[i].rgb << (8 - color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a << (8 - alpha_component_precision(mode));

        // Replicate each component's MSB into the LSBs revealed by the left-shift operation above
        endpoint_array[i].rgb = endpoint_array[i].rgb | (endpoint_array[i].rgb >> color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a | (endpoint_array[i].a >> alpha_component_precision(mode));
    }
        
    //If this mode does not explicitly define the alpha component
    //set alpha equal to 1.0
    if (mode.type == 0 OR == 1 OR == 2 OR == 3)
    {
        for each endpoint i
        {
            endpoint_array[i].a = 255; //i.e. alpha = 1.0f
        }
    }
}
```

<span data-ttu-id="24962-183">Per generare ogni componente interpolato per ogni subset, usare l'algoritmo seguente: lasciare che "c" sia il componente da generare. consentire a "E0" di essere il componente dell'endpoint 0 del sottoinsieme; e consentono a "E1" di essere il componente dell'endpoint 1 del sottoinsieme.</span><span class="sxs-lookup"><span data-stu-id="24962-183">To generate each interpolated component for each subset, use the following algorithm: let "c" be the component to generate; let "e0" be that component of endpoint 0 of the subset; and let "e1" be that component of endpoint 1 of the subset.</span></span>

``` syntax
UINT16 aWeight2[] = {0, 21, 43, 64};
UINT16 aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
UINT16 aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

UINT8 interpolate(UINT8 e0, UINT8 e1, UINT8 index, UINT8 indexprecision)
{
    if(indexprecision == 2)
        return (UINT8) (((64 - aWeights2[index])*UINT16(e0) + aWeights2[index]*UINT16(e1) + 32) >> 6);
    else if(indexprecision == 3)
        return (UINT8) (((64 - aWeights3[index])*UINT16(e0) + aWeights3[index]*UINT16(e1) + 32) >> 6);
    else // indexprecision == 4
        return (UINT8) (((64 - aWeights4[index])*UINT16(e0) + aWeights4[index]*UINT16(e1) + 32) >> 6);
}
```

<span data-ttu-id="24962-184">Nello pseudocodice seguente viene illustrato come estrarre gli indici e i conteggi dei bit per i componenti colore e alfa.</span><span class="sxs-lookup"><span data-stu-id="24962-184">The following pseudocode illustrates how to extract indices and bit counts for color and alpha components.</span></span> <span data-ttu-id="24962-185">I blocchi con colore separato e Alpha hanno anche due set di dati di indice: uno per il canale vettoriale e uno per il canale scalare.</span><span class="sxs-lookup"><span data-stu-id="24962-185">Blocks with separate color and alpha also have two sets of index data: one for the vector channel, and one for the scalar channel.</span></span> <span data-ttu-id="24962-186">Per la modalità 4, questi indici hanno larghezze diverse (2 o 3 bit) ed esiste un selettore a un bit che specifica se i dati vettoriali o scalari usano gli indici a 3 bit.</span><span class="sxs-lookup"><span data-stu-id="24962-186">For Mode 4, these indices are of differing widths (2 or 3 bits), and there is a one-bit selector which specifies whether the vector or scalar data uses the 3-bit indices.</span></span> <span data-ttu-id="24962-187">L'estrazione del conteggio dei bit alfa è simile all'estrazione del numero di bit di colore, ma con un comportamento inverso basato sul bit **idxMode** .</span><span class="sxs-lookup"><span data-stu-id="24962-187">(Extracting the alpha bit count is similar to extracting color bit count but with inverse behavior based on the **idxMode** bit.)</span></span>

``` syntax
bitcount get_color_bitcount(block, mode)
{
    if (mode.type == 0 OR == 1)
        return 3;
    
    if (mode.type == 2 OR == 3 OR == 5 OR == 7)
        return 2;
    
    if (mode.type == 6)
        return 4;
        
    //The only remaining case is Mode 4 with 1-bit index selector
    idxMode = extract_idxMode(block);
    if (idxMode == 0)
        return 2;
    else
        return 3;
}
```

## <a name="related-topics"></a><span data-ttu-id="24962-188">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24962-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24962-189">Compressione dei blocchi di trama in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="24962-189">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 