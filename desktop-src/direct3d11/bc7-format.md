---
title: Formato BC7
description: Il formato BC7 è un formato di compressione della trama usato per la compressione di alta qualità dei dati RGB e RGBA.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd48826cc0c02be6d15a837c272442c0931e9660f507a90cb491acf4d5820ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858221"
---
# <a name="bc7-format"></a>Formato BC7

Il formato BC7 è un formato di compressione della trama usato per la compressione di alta qualità dei dati RGB e RGBA.

-   [Informazioni su BC7/DXGI \_ FORMAT \_ BC7](/windows)
-   [Implementazione bc7](#bc7-implementation)
-   [Decodifica del formato BC7](#decoding-the-bc7-format)
-   [Argomenti correlati](#related-topics)

Per informazioni sulle modalità di blocco del formato BC7, vedere Bc7 Format Mode Reference (Informazioni [di riferimento sulla modalità di formato BC7).](bc7-format-mode-reference.md)

## <a name="about-bc7dxgi_format_bc7"></a>Informazioni su BC7/DXGI \_ FORMAT \_ BC7

BC7 viene specificato dai valori di enumerazione DXGI \_ FORMAT seguenti:

-   **DXGI \_ FORMAT \_ BC7 \_ TYPELESS**.
-   **DXGI \_ FORMAT \_ BC7 \_ UNORM**.
-   **DXGI \_ FORMAT \_ BC7 \_ UNORM \_ SRGB**.

Il formato BC7 può essere usato per le risorse [trama Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluse le matrici), Texture3D o TextureCube (incluse le matrici). Analogamente, questo formato si applica a qualsiasi superficie mappa MIP associata a queste risorse.

BC7 usa una dimensione di blocco fissa di 16 byte (128 bit) e una dimensione di riquadro fissa di 4x4 texel. Come per i formati BC precedenti, le immagini di trama di dimensioni superiori alle dimensioni del riquadro supportate (4x4) vengono compresse usando più blocchi. Questa identità di indirizzamento si applica anche a immagini tridimensionali e mappe MIP, mappe cubi e matrici di trame. Tutti i riquadri immagine devono avere lo stesso formato.

BC7 comprime sia immagini di dati a virgola fissa a tre canali (RGB) che a 4 canali (RGBA). In genere, i dati di origine sono a 8 bit per componente di colore (canale), anche se il formato è in grado di codificare i dati di origine con bit più elevati per componente colore. Tutti i riquadri immagine devono avere lo stesso formato.

Il decodificatore BC7 esegue la decompressione prima dell'applicazione del filtro della trama.

L'hardware di decompressione BC7 deve essere bit accurato; ciò significa che l'hardware deve restituire risultati identici ai risultati restituiti dal decodificatore descritto in questo documento.

## <a name="bc7-implementation"></a>Implementazione bc7

Un'implementazione BC7 può specificare una delle 8 modalità, con la modalità specificata nel bit meno significativo del blocco a 16 byte (128 bit). La modalità è codificata da zero o più bit con un valore pari a 0 seguito da 1.

Un blocco BC7 può contenere più coppie di endpoint. Ai fini di questa documentazione, il set di indici che corrispondono a una coppia di endpoint può essere definito "subset". Inoltre, in alcune modalità a blocchi, la rappresentazione dell'endpoint viene codificata in un formato che, anche in questo caso, ai fini di questa documentazione, deve essere definito "RBGP", dove il bit "P" rappresenta un bit condiviso meno significativo per i componenti di colore dell'endpoint. Ad esempio, se la rappresentazione dell'endpoint per il formato è "RGB 5.5.5.1", l'endpoint viene interpretato come un valore RGB 6.6.6, dove lo stato del bit P definisce il bit meno significativo di ogni componente. Analogamente, per i dati di origine con un canale alfa, se la rappresentazione per il formato è "RGBAP 5.5.5.5.1", l'endpoint viene interpretato come RGBA 6.6.6.6. A seconda della modalità di blocco, è possibile specificare il bit meno significativo condiviso per entrambi gli endpoint di un subset singolarmente (2 bit P per subset) o condivisi tra gli endpoint di un subset (1 P-bit per subset).

Per i blocchi BC7 che non codificano in modo esplicito il componente alfa, un blocco BC7 è costituito da bit di modalità, bit di partizione, endpoint compressi, indici compressi e un P-bit facoltativo. In questi blocchi gli endpoint hanno una rappresentazione solo RGB e il componente alfa viene decodificato come 1.0 per tutti i texel nei dati di origine.

Per i blocchi BC7 che hanno componenti colore e alfa combinati, un blocco è costituito da bit di modalità, endpoint compressi, indici compressi e bit di partizione facoltativi e P-bit. In questi blocchi, i colori dell'endpoint sono espressi in formato RGBA e i valori dei componenti alfa vengono interpolati insieme ai valori del componente colore.

Per i blocchi BC7 con componenti di colore e alfa separati, un blocco è costituito da bit di modalità, bit di rotazione, endpoint compressi, indici compressi e un bit del selettore di indice facoltativo. Questi blocchi hanno un vettore RGB R, G, B e un canale \[ \] alfa scalare A \[ \] codificati separatamente.

Nella tabella seguente sono elencati i componenti di ogni tipo di blocco.



| Il blocco BC7 contiene...     | bit della modalità | bit di rotazione | bit del selettore di indice | bit di partizione | endpoint compressi | P-bit    | indici compressi |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| Solo componenti a colori     | necessario  | N/D           | N/D                | necessario       | necessario             | facoltative | necessario           |
| combinazione di colore e alfa    | necessario  | N/D           | N/D                | facoltative       | necessario             | facoltative | necessario           |
| colore e valori alfa separati | necessario  | necessario      | facoltative           | N/A            | necessario             | N/A      | necessario           |



 

BC7 definisce una tavolozza di colori su una linea approssimativa tra due endpoint. Il valore mode determina il numero di coppie di endpoint di interpolazione per blocco. BC7 archivia un indice della tavolozza per ogni texel.

Per ogni subset di indici che corrisponde a una coppia di endpoint, il codificatore corregge lo stato di un bit dei dati dell'indice compresso per tale subset. A tale scopo, sceglie un ordine dell'endpoint che consente all'indice per l'indice di "correzione" designato di impostare il bit più significativo su 0 e che può quindi essere eliminato, salvando un bit per subset. Per le modalità a blocchi con un solo subset, l'indice di correzione è sempre l'indice 0.

## <a name="decoding-the-bc7-format"></a>Decodifica del formato BC7

Lo pseudocodice seguente illustra i passaggi per decomprimere il pixel in corrispondenza di (x,y) in base al blocco BC7 a 16 byte.

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

Lo pseudocodice seguente descrive i passaggi per decodificare completamente il colore dell'endpoint e i componenti alfa per ogni subset in base a un blocco BC7 a 16 byte.

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

Per generare ogni componente interpolato per ogni subset, usare l'algoritmo seguente: lasciare che "c" sia il componente da generare; lasciare che "e0" sia il componente dell'endpoint 0 del subset; e lasciare che "e1" sia il componente dell'endpoint 1 del subset.

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

Lo pseudocodice seguente illustra come estrarre indici e conteggi di bit per i componenti di colore e alfa. I blocchi con colore e alfa separati hanno anche due set di dati di indice: uno per il canale vettoriale e uno per il canale scalare. Per la modalità 4, questi indici hanno larghezze diverse (2 o 3 bit) ed è presente un selettore a 1 bit che specifica se il vettore o i dati scalari utilizzano gli indici a 3 bit. L'estrazione del conteggio dei bit alfa è simile all'estrazione del numero di bit dei colori, ma con un comportamento inverso basato sul bit **idxMode.**

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compressione dei blocchi di trama in Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 