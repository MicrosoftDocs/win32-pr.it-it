---
title: Guida alla programmazione per DDS
description: Direct3D implementa il formato di file DDS per l'archiviazione di trame non compresse o compresse (DXTn).
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4940db5ec40e6ec0b907aa4ee7ce725cd585e961
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399938"
---
# <a name="programming-guide-for-dds"></a>Guida alla programmazione per DDS

Direct3D implementa il formato di file DDS per l'archiviazione di trame non compresse o compresse (DXTn). Il formato di file implementa diversi tipi leggermente diversi, progettati per l'archiviazione di diversi tipi di dati, e supporta trame a livello singolo, trame con mipmap, mappe di cubi, mappe del volume e matrici di trame (in Direct3D 10/11). In questa sezione viene descritto il layout di un file DDS.

Per informazioni sulla creazione di una trama in Direct3D 11, vedere [How to: Create a texture](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create). Per informazioni su Direct3D 9, vedere [supporto delle trame in D3DX (Direct3D 9)](/windows/desktop/direct3d9/texture-support-in-d3dx).

-   [Layout file DDS](#dds-file-layout)
-   [Varianti DDS](#dds-variants)
-   [Uso di matrici di trama in Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Formati di risorse file DDS comuni e contenuto di intestazione associato](#common-dds-file-resource-formats-and-associated-header-content)
-   [Argomenti correlati](#related-topics)

## <a name="dds-file-layout"></a>Layout file DDS

Un file DDS è un file binario contenente le informazioni seguenti:

-   Un valore DWORD (numero chiave) contenente il valore del codice di quattro caratteri 'DDS ' (0x20534444).

-   Una descrizione dei dati nel file.

    I dati vengono descritti con una descrizione dell'intestazione usando l' [**\_ intestazione DDS**](dds-header.md). il formato pixel viene definito usando [**DDS \_ PIXELFORMAT**](dds-pixelformat.md). Si noti che **l' \_ intestazione DDS** e le strutture **DDS \_ PIXELFORMAT** sostituiscono le strutture deprecate DDSURFACEDESC2, DDSCAPS2 e DDPIXELFORMAT di DirectDraw 7. **DDS \_ HEADER** è l'equivalente binario di DDSURFACEDESC2 e DDSCAPS2. **DDS \_ PIXELFORMAT** è l'equivalente binario di DDPIXELFORMAT.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Se l'oggetto \_ dwFlags PIXELFORMAT dwFlags è impostato su DDPF \_ fourcc e dwFourCC è impostato su "DX10", sarà presente un'intestazione DDS aggiuntiva struttura [**\_ \_ DXT10**](dds-header-dxt10.md) per contenere matrici di trama o formati DXGI che non possono essere espressi come formato pixel RGB, ad esempio formati a virgola mobile, formati sRGB e così via. Quando la struttura dell' **\_ intestazione DDS \_ DXT10** è presente, l'intera descrizione dei dati sarà simile alla seguente.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
    DDS_HEADER_DXT10    header10;
    ```

    

-   Un puntatore a una matrice di byte contenente i dati della superficie principale.
    ```
    BYTE bdata[]
    ```

    

-   Un puntatore a una matrice di byte contenente le superfici rimanenti, ad esempio i livelli mipmap, le facce in una mappa di cubo, le profondità in una trama di volume. Visita questi collegamenti per altre informazioni sul layout dei file DDS per una [texture](dds-file-layout-for-textures.md), una [mappa di cubo](dds-file-layout-for-cubic-environment-maps.md) o una [trama di volume](dds-file-layout-for-volume-textures.md).

    ```
    BYTE bdata2[]
    ```

    

Per un supporto hardware ampio, è consigliabile usare il [**formato DXGI \_ \_ R8G8B8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ Format \_ R8G8B8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R8G8B8A8 \_ russar**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), DXGI [**\_ Format \_ B8G8R8A8 \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)UNORM, [**DXGI Format R16G16 \_ \_ \_ russar**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI Format R8G8 \_ \_ \_ russar**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), DXGI [**\_ Format \_ BC1 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ BC1 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)BC2 UNORM, DXGI [**\_ Format BC2 UNORM \_ \_ \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ \_ \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)BC3 UNORM o DXGI Format BC3 [**UNORM in formato \_ \_ \_ \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

Per altre informazioni sui formati di trama compressi, vedere [compressione dei blocchi di trama in Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) e [compressione dei blocchi (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

La libreria D3DX (ad esempio, D3DX11. lib) e altre librerie simili forniscono in modo non affidabile o in modo incoerente il valore di pitch nel membro **dwPitchOrLinearSize** della struttura dell' [**\_ intestazione DDS**](dds-header.md) . Pertanto, durante la lettura e la scrittura nei file DDS, è consigliabile calcolare il pitch in uno dei modi seguenti per i formati indicati:

-   Per i formati compressi a blocchi, calcolare il pitch come:

    numero massimo di blocchi (1, (larghezza + 3)/4) \*

    Le dimensioni del blocco sono pari a 8 byte per i formati DXT1, BC1 e BC4 e 16 byte per altri formati compressi a blocchi.

-   Per R8G8 \_ B8G8, G8R8 \_ G8B8, Legacy UYVY e i formati legacy YUY2 compressi, calcolare il passo come:

    ((larghezza + 1)  >> 1) \* 4

-   Per altri formati, calcolare il pitch come:

    ( \* bit larghezza-per-pixel + 7)/8

    Dividere per 8 per l'allineamento dei byte.

> [!Note]  
> Il valore di pitch calcolato non è sempre uguale al passo fornito dal runtime, che è allineato a DWORD in alcune situazioni e allineato a byte in altre situazioni. È pertanto consigliabile copiare una riga di analisi alla volta anziché tentare di copiare l'intera immagine in una copia.

 

## <a name="dds-variants"></a>Varianti DDS

Sono disponibili molti strumenti per la creazione e l'utilizzo di file DDS, ma possono variare nei dettagli di ciò che richiedono nell'intestazione. I writer devono popolare le intestazioni nel modo più completo possibile e i lettori devono verificare i valori minimi per la massima compatibilità. Per convalidare un file DDS, un lettore deve verificare che il file sia di almeno 128 byte per contenere il valore di Magic e l'intestazione di base, il valore Magic è 0x20534444 ("DDS"), le \_ dimensioni dell'intestazione DDS sono 124 e le dimensioni dell' \_ intestazione dds è 32. Se DDS \_ PIXELFORMAT dwFlags è impostato su DDPF \_ fourcc e dwFourCC è impostato su "DX10", le dimensioni totali del file devono essere almeno di 148 byte.

Esistono alcune varianti comuni in uso, in cui il formato pixel è impostato su un \_ codice DDPF FourCC in cui dwFourCC è impostato su un valore di enumerazione di formato D3DFORMAT o DXGI \_ . Non esiste alcun modo per stabilire se un valore di enumerazione è un formato D3DFORMAT o DXGI \_ , quindi è consigliabile usare invece l'intestazione "DX10" e l' \_ intestazione DXT10 dell'intestazione DDS \_ per archiviare il dxgiFormat quando il formato DDS di base \_ non è in grado di esprimere il formato.

\_Per la massima compatibilità per archiviare i dati non compressi RGB e i dati DXT1-5 è consigliabile preferire la versione standard di DDS. non tutti gli strumenti DDS supportano l'estensione DX10.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Uso di matrici di trama in Direct3D 10/11

Le nuove strutture DDS ([**\_ intestazione DDS**](dds-header.md) e [**\_ intestazione dds \_ DXT10**](dds-header-dxt10.md)) in Direct3D 10/11 estendono il formato di file DDS per supportare una matrice di trame, che è un nuovo tipo di risorsa in Direct3D 10/11. Di seguito è riportato un codice di esempio che illustra come accedere ai diversi livelli di mipmap in una matrice di trame usando le nuove intestazioni.


```
DWORD               dwMagic;
DDS_HEADER          header;
DDS_HEADER_DXT10    header10;
   
for (int iArrayElement = 0; iArrayElement < header10.arraySize; iArrayElement++)
{
   for (int iMipLevel = 0; iMipLevel < header.dwMipMapCount; iMipLevel++)
   {
     ...
   }
}       
```



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Formati di risorse file DDS comuni e contenuto di intestazione associato



| Formato risorsa                                                                            | dwFlags        | dwRGBBitCount | dwRBitMask | dwGBitMask | dwBBitMask | dwABitMask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| \_Formato DXGI \_ R8G8B8A8 \_ UNORM<br/> \_A8B8G8R8 D3DFMT<br/>                       | \_RGBA DDS      | 32            | 0xFF       | 0xff00     | 0xFF0000   | 0xFF000000 |
| \_Formato DXGI \_ R16G16 \_ UNORM<br/> \_G16R16 D3DFMT<br/>                           | \_RGBA DDS      | 32            | 0xFFFF     | 0xffff0000 |            |            |
| \*\*<br/> \_Formato DXGI \_ R10G10B10A2 \_ UNORM<br/> \_A2B10G10R10 D3DFMT<br/> | \_RGBA DDS      | 32            | 0x3FF      | 0xffc00    | 0x3ff00000 |            |
| \_Formato DXGI \_ R16G16 \_ UNORM<br/> \_G16R16 D3DFMT<br/>                           | \_RGB DDS       | 32            | 0xFFFF     | 0xffff0000 |            |            |
| \_Formato DXGI \_ B5G5R5A1 \_ UNORM<br/> \_A1R5G5B5 D3DFMT<br/>                       | \_RGBA DDS      | 16            | 0x7c00     | 0x3e0      | 0x1F       | 0x8000     |
| \_Formato DXGI \_ B5G6R5 \_ UNORM<br/> \_R5G6B5 D3FMT<br/>                            | \_RGB DDS       | 16            | 0xf800     | 0x7e0      | 0x1F       |            |
| DXGI \_ a8 \_ UNORM<br/> D3DFMT \_ a8<br/>                                           | \_alfa DDS     | 8             |            |            |            | 0xFF       |
| \_A8R8G8B8 D3DFMT<br/>                                                                | \_RGBA DDS      | 32            | 0xFF0000   | 0xff00     | 0xFF       | 0xFF000000 |
| \_X8R8G8B8 D3DFMT<br/>                                                                | \_RGB DDS       | 32            | 0xFF0000   | 0xff00     | 0xFF       |            |
| \_X8B8G8R8 D3DFMT<br/>                                                                | \_RGB DDS       | 32            | 0xFF       | 0xff00     | 0xFF0000   |            |
| \*\*<br/> \_A2R10G10B10 D3DFMT<br/>                                             | \_RGBA DDS      | 32            | 0x3ff00000 | 0xffc00    | 0x3FF      | 0xC0000000 |
| \_R8G8B8 D3DFMT<br/>                                                                  | \_RGB DDS       | 24            | 0xFF0000   | 0xff00     | 0xFF       |            |
| \_X1R5G5B5 D3DFMT<br/>                                                                | \_RGB DDS       | 16            | 0x7c00     | 0x3e0      | 0x1F       |            |
| \_A4R4G4B4 D3DFMT<br/>                                                                | \_RGBA DDS      | 16            | 0xf00      | 0xf0       | 0xF        | 0xF000     |
| \_X4R4G4B4 D3DFMT<br/>                                                                | \_RGB DDS       | 16            | 0xf00      | 0xf0       | 0xF        |            |
| \_A8R3G3B2 D3DFMT<br/>                                                                | \_RGBA DDS      | 16            | 0XE0       | 0x1C       | 0x3        | 0xff00     |
| \_A8L8 D3DFMT<br/>                                                                    | \_luminanza DDS | 16            | 0xFF       |            |            | 0xff00     |
| \_L16 D3DFMT<br/>                                                                     | \_luminanza DDS | 16            | 0xFFFF     |            |            |            |
| \_L8 D3DFMT<br/>                                                                      | \_luminanza DDS | 8             | 0xFF       |            |            |            |
| \_A4L4 D3DFMT<br/>                                                                    | \_luminanza DDS | 8             | 0xF        |            |            | 0xf0       |



 



| Formato risorsa                                                                             | dwFlags     | dwFourCC |
|---------------------------------------------------------------------------------------------|-------------|----------|
| \_Formato DXGI \_ BC1 \_ UNORM<br/> \_DXT1 D3DFMT<br/>                                 | \_fourcc DDS | DXT1   |
| \_Formato DXGI \_ BC2 \_ UNORM<br/> \_DXT3 D3DFMT<br/>                                 | \_fourcc DDS | "DXT3"   |
| \_Formato DXGI \_ BC3 \_ UNORM<br/> \_DXT5 D3DFMT<br/>                                 | \_fourcc DDS | DXT5   |
| \*<br/> \_Formato DXGI \_ BC4 \_ UNORM<br/>                                           | \_fourcc DDS | "BC4U"   |
| \*<br/> DXGI \_ Format \_ BC4 \_ russar<br/>                                           | \_fourcc DDS | "BC4S"   |
| \*<br/> \_Formato DXGI \_ BC5 \_ UNORM<br/>                                           | \_fourcc DDS | "ATI2"   |
| \*<br/> DXGI \_ Format \_ BC5 \_ russar<br/>                                           | \_fourcc DDS | "BC5S"   |
| DXGI \_ Format \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | \_fourcc DDS | "RGBG"   |
| DXGI \_ Format \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | \_fourcc DDS | "GRGB"   |
| \*<br/> \_Formato DXGI \_ R16G16B16A16 \_ UNORM<br/> \_A16B16G16R16 D3DFMT<br/>  | \_fourcc DDS | 36       |
| \*<br/> DXGI \_ Format \_ R16G16B16A16 \_ russar<br/> \_Q16W16V16U16 D3DFMT<br/>  | \_fourcc DDS | 110      |
| \*<br/> \_Formato DXGI \_ R16 \_ float<br/> \_R16F D3DFMT<br/>                   | \_fourcc DDS | 111      |
| \*<br/> \_Formato DXGI \_ R16G16 \_ float<br/> \_G16R16F D3DFMT<br/>             | \_fourcc DDS | 112      |
| \*<br/> \_Formato DXGI \_ R16G16B16A16 \_ float<br/> \_A16B16G16R16F D3DFMT<br/> | \_fourcc DDS | 113      |
| \*<br/> \_Formato DXGI \_ R32 \_ float<br/> \_R32F D3DFMT<br/>                   | \_fourcc DDS | 114      |
| \*<br/> \_Formato DXGI \_ R32G32 \_ float<br/> \_G32R32F D3DFMT<br/>             | \_fourcc DDS | 115      |
| \*<br/> \_Formato DXGI \_ R32G32B32A32 \_ float<br/> \_A32B32G32R32F D3DFMT<br/> | \_fourcc DDS | 116      |
| \_DXT2 D3DFMT<br/>                                                                     | \_fourcc DDS | "DXT2"   |
| \_DXT4 D3DFMT<br/>                                                                     | \_fourcc DDS | "DXT4"   |
| \_UYVY D3DFMT<br/>                                                                     | \_fourcc DDS | UYVY   |
| \_YUY2 D3DFMT<br/>                                                                     | \_fourcc DDS | YUY2   |
| \_CXV8U8 D3DFMT<br/>                                                                   | \_fourcc DDS | 117      |
| Qualsiasi formato DXGI                                                                             | \_fourcc DDS | DX10   |



 

\* = Un lettore DDS affidabile deve essere in grado di gestire questi codici di formato legacy. Tuttavia, tale reader DDS dovrebbe preferire l'uso dell'estensione di intestazione "DX10" quando scrive questi codici di formato per evitare ambiguità.

\*\* = A causa di alcuni problemi di lunga durata nelle implementazioni comuni di Reader e writer DDS, il modo più efficace per scrivere dati di tipo 10:10:10:2 consiste nell'usare l'estensione di intestazione "DX10" con il codice di [**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) "24", ovvero il \_ formato DXGI \_ R10G10B10A2 \_ UNORM value. \_I dati di D3DFMT A2R10G10B10 devono essere convertiti in dati di tipo 10:10:10:2 prima di essere scritti come dxgi \_ Format \_ R10G10B10A2 \_ UNORM Format DDS file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DDS](dx-graphics-dds.md)
</dt> </dl>

 

