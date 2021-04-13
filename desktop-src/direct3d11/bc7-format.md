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
# <a name="bc7-format"></a>Formato BC7

Il formato BC7 è un formato di compressione di trama usato per la compressione di alta qualità dei dati RGB e RGBA.

-   [Informazioni sul formato BC7/DXGI \_ \_ BC7](/windows)
-   [Implementazione di BC7](#bc7-implementation)
-   [Decodifica del formato BC7](#decoding-the-bc7-format)
-   [Argomenti correlati](#related-topics)

Per informazioni sulle modalità di blocco del formato BC7, vedere [riferimento alla modalità di formattazione BC7](bc7-format-mode-reference.md).

## <a name="about-bc7dxgi_format_bc7"></a>Informazioni sul formato BC7/DXGI \_ \_ BC7

BC7 viene specificato dai valori di enumerazione del formato DXGI seguenti \_ :

-   **DXGI \_ FORMATTARE \_ BC7 con \_ tipo**.
-   **DXGI \_ FORMATTARE \_ BC7 \_ UNORM**.
-   **DXGI \_ FORMATTARE \_ BC7 \_ UNORM \_ sRGB**.

Il formato BC7 può essere usato per le risorse di trama [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (incluse le matrici), Texture3D o TextureCube (incluse le matrici). Analogamente, questo formato si applica a qualsiasi superficie mappa MIP associata a tali risorse.

BC7 usa una dimensione fissa a blocchi di 16 byte (128 bit) e una dimensione del riquadro fissa di Texel 4x4. Come per i formati BC precedenti, le immagini di trama più grandi delle dimensioni del riquadro supportate (4x4) vengono compresse usando più blocchi. Questa identità di indirizzamento si applica anche alle immagini tridimensionali e alle matrici MIP, CubeMaps e di trama. Tutti i riquadri immagine devono avere lo stesso formato.

BC7 comprime sia immagini di dati a virgola fissa a tre canali (RGB) che a quattro canali (RGBA). In genere, i dati di origine sono a 8 bit per componente colore (canale), sebbene il formato sia in grado di codificare i dati di origine con bit più alti per componente colore. Tutti i riquadri immagine devono avere lo stesso formato.

Il decodificatore BC7 esegue la decompressione prima dell'applicazione del filtro della trama.

L'hardware di decompressione di BC7 deve essere leggermente accurato; ovvero, l'hardware deve restituire risultati identici ai risultati restituiti dal decodificatore descritto in questo documento.

## <a name="bc7-implementation"></a>Implementazione di BC7

Un'implementazione di BC7 può specificare una delle 8 modalità, con la modalità specificata nel bit meno significativo del blocco a 16 byte (128 bit). La modalità è codificata da zero o più bit con un valore pari a 0 seguito da 1.

Un blocco BC7 può contenere più coppie di endpoint. Ai fini di questa documentazione, il set di indici che corrisponde a una coppia di endpoint può essere definito "subset". Inoltre, in alcune modalità di blocco, la rappresentazione dell'endpoint viene codificata in un form che, ai fini di questa documentazione, deve essere denominata "RBGP", dove il bit "P" rappresenta un bit meno significativo condiviso per i componenti di colore dell'endpoint. Se, ad esempio, la rappresentazione dell'endpoint per il formato è "RGB 5.5.5.1", l'endpoint viene interpretato come valore 6.6.6 RGB, dove lo stato del P-bit definisce il bit meno significativo di ogni componente. Analogamente, per i dati di origine con un canale alfa, se la rappresentazione per il formato è "RGBAP 5.5.5.5.1", l'endpoint è interepreted come RGBA 6.6.6.6. A seconda della modalità di blocco, è possibile specificare il bit meno significativo condiviso per entrambi gli endpoint di un subset singolarmente (2 P-bit per subset) o condivisi tra endpoint di un subset (1 P-bit per subset).

Per i blocchi BC7 che non codificano in modo esplicito il componente alfa, un blocco BC7 è costituito da bit in modalità, bit di partizione, endpoint compressi, indici compressi e un P-bit facoltativo. In questi blocchi gli endpoint hanno una rappresentazione solo RGB e il componente alfa viene decodificato come 1,0 per tutti i Texel nei dati di origine.

Per i blocchi BC7 con componenti combinati di colore e alfa, un blocco è costituito da bit in modalità, endpoint compressi, indici compressi e bit di partizione facoltativi e un P-bit. In questi blocchi, i colori dell'endpoint sono espressi in formato RGBA e i valori dei componenti alfa vengono interpolati insieme ai valori dei componenti dei colori.

Per i blocchi BC7 con componenti di colore e alfa distinti, un blocco è costituito da bit in modalità, bit di rotazione, endpoint compressi, indici compressi e un bit del selettore di indice facoltativo. Questi blocchi hanno un vettore RGB effettivo \[ R, G, B \] e un canale alfa scalare \[ a \] codificato separatamente.

Nella tabella seguente sono elencati i componenti di ogni tipo di blocco.



| Il blocco BC7 contiene...     | bit della modalità | bit di rotazione | bit selettore indice | bit partizione | endpoint compressi | P-bit    | indici compressi |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| solo componenti colori     | necessario  | N/D           | N/D                | necessario       | necessario             | facoltative | necessario           |
| colore + Alpha combinato    | necessario  | N/D           | N/D                | facoltative       | necessario             | facoltative | necessario           |
| colore e alfa separati | necessario  | necessario      | facoltative           | N/D            | necessario             | N/D      | necessario           |



 

BC7 definisce una tavolozza di colori su una linea approssimativa tra due endpoint. Il valore della modalità determina il numero di coppie di endpoint di interpolazione per blocco. BC7 archivia un indice tavolozza per Texel.

Per ogni subset di indici che corrisponde a una coppia di endpoint, il codificatore corregge lo stato di un bit dei dati dell'indice compresso per quel subset. Questa operazione viene eseguita scegliendo un ordine di endpoint che consente all'indice per l'indice "correzione" designato di impostare il bit più significativo su 0 e che può quindi essere ignorato, salvando un bit per ogni subset. Per le modalità di blocco con un solo subset, l'indice di correzione è sempre indice 0.

## <a name="decoding-the-bc7-format"></a>Decodifica del formato BC7

Lo pseudocodice seguente illustra i passaggi per decomprimere il pixel in corrispondenza di (x, y) in base al blocco BC7 a 16 byte.

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

Lo pseudocodice di seguente descrive i passaggi per decodificare completamente i componenti alfa e del colore dell'endpoint per ogni subset dato un blocco BC7 a 16 byte.

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

Per generare ogni componente interpolato per ogni subset, usare l'algoritmo seguente: lasciare che "c" sia il componente da generare. consentire a "E0" di essere il componente dell'endpoint 0 del sottoinsieme; e consentono a "E1" di essere il componente dell'endpoint 1 del sottoinsieme.

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

Nello pseudocodice seguente viene illustrato come estrarre gli indici e i conteggi dei bit per i componenti colore e alfa. I blocchi con colore separato e Alpha hanno anche due set di dati di indice: uno per il canale vettoriale e uno per il canale scalare. Per la modalità 4, questi indici hanno larghezze diverse (2 o 3 bit) ed esiste un selettore a un bit che specifica se i dati vettoriali o scalari usano gli indici a 3 bit. L'estrazione del conteggio dei bit alfa è simile all'estrazione del numero di bit di colore, ma con un comportamento inverso basato sul bit **idxMode** .

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

 

 