---
title: Guida per programmatori per DDS
description: Direct3D implementa il formato di file DDS per l'archiviazione di trame non compresse o compresse (DXTn).
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc1f8b9b84c2dc1f9236c79c320ae75848834ef2183db55b189f6b9d340d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796721"
---
# <a name="programming-guide-for-dds"></a>Guida per programmatori per DDS

Direct3D implementa il formato di file DDS per l'archiviazione di trame non compresse o compresse (DXTn). Il formato di file implementa diversi tipi leggermente diversi progettati per l'archiviazione di tipi diversi di dati e supporta trame a livello singolo, trame con mipmap, mappe cubo, mappe di volume e matrici di trame (in Direct3D 10/11). Questa sezione descrive il layout di un file DDS.

Per informazioni sulla creazione di una trama in Direct3D 11, vedere [Procedura: Creare una trama.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) Per informazioni su Direct3D 9, vedere [Supporto delle trame in D3DX (Direct3D 9).](/windows/desktop/direct3d9/texture-support-in-d3dx)

-   [DDS File Layout](#dds-file-layout)
-   [Varianti DDS](#dds-variants)
-   [Uso di matrici di trame in Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Formati di risorse file DDS comuni e contenuto dell'intestazione associato](#common-dds-file-resource-formats-and-associated-header-content)
-   [Argomenti correlati](#related-topics)

## <a name="dds-file-layout"></a>DDS File Layout

Un file DDS è un file binario contenente le informazioni seguenti:

-   Un valore DWORD (numero chiave) contenente il valore del codice di quattro caratteri 'DDS ' (0x20534444).

-   Una descrizione dei dati nel file.

    I dati vengono descritti con una descrizione dell'intestazione [**tramite DDS \_ HEADER.**](dds-header.md)Il formato pixel viene definito usando [**\_ PIXELFORMAT DDS.**](dds-pixelformat.md) Si noti che le **strutture DDS \_ HEADER** e **DDS \_ PIXELFORMAT** sostituiscono le strutture DDSURFACEDESC2, DDSCAPS2 e DDPIXELFORMAT DirectDraw 7 deprecate. **DDS \_ HEADER** è l'equivalente binario di DDSURFACEDESC2 e DDSCAPS2. **DDS \_ PIXELFORMAT è** l'equivalente binario di DDPIXELFORMAT.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Se DDS PIXELFORMAT dwFlags è impostato su DDPF FOURCC e dwFourCC è impostato su "DX10", sarà presente una struttura \_ \_ [**\_ \_ DXT10 DDS HEADER**](dds-header-dxt10.md) aggiuntiva per supportare matrici di trame o formati DXGI che non possono essere espressi come formato pixel RGB, ad esempio formati a virgola mobile, formati sRGB e così via. Quando è **presente la struttura \_ DDS HEADER \_ DXT10,** l'intera descrizione dei dati sarà simile alla seguente.

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

    

Per un ampio supporto hardware, è consigliabile usare [**DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R16G16 \_ SNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ FORMAT \_ R8G8 \_ SNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R8 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ BC1 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ BC2 \_ UNORM,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ BC3 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)o [**DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format.

Per altre informazioni sui formati di trama compressi, vedere Compressione dei blocchi di trama [in Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) e [Compressione a blocchi (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)

La libreria D3DX (ad esempio D3DX11.lib) e altre librerie simili forniscono in modo inaffidabile o incoerente il valore dell'altezza nel membro **dwPitchOrLinearSize** della struttura [**HEADER DDS. \_**](dds-header.md) Pertanto, quando si legge e si scrive nei file DDS, è consigliabile calcolare l'altezza in uno dei modi seguenti per i formati indicati:

-   Per i formati compressi a blocchi, calcolare l'altezza come:

    max( 1, ((width+3)/4) ) \* block-size

    Le dimensioni del blocco sono 8 byte per i formati DXT1, BC1 e BC4 e 16 byte per altri formati compressi a blocchi.

-   Per I formati R8G8 \_ B8G8, G8R8 G8B8, legacy con pacchetto \_ UYVY e legacy con pacchetto YUY2, calcolare il passo come:

    ((larghezza+1) >> 1) \* 4

-   Per altri formati, calcolare l'altezza come:

    ( width \* bits-per-pixel + 7 ) / 8

    Si divide per 8 per l'allineamento dei byte.

> [!Note]  
> Il valore di passo calcolato non è sempre uguale all'altezza fornita dal runtime, che è allineato a DWORD in alcune situazioni e allineato ai byte in altre situazioni. È pertanto consigliabile copiare una riga di analisi alla volta anziché provare a copiare l'intera immagine in un'unica copia.

 

## <a name="dds-variants"></a>Varianti DDS

Esistono molti strumenti che creano e utilizzano file DDS, ma possono variare nei dettagli di ciò che richiedono nell'intestazione. I writer devono popolare le intestazioni nel modo più completo possibile e i lettori devono controllare i valori minimi per la massima compatibilità. Per convalidare un file DDS, un lettore deve assicurarsi che il file sia lungo almeno 128 byte per contenere il valore magico e l'intestazione di base, il valore magico è 0x20534444 ("DDS"), le dimensioni dell'intestazione DDS sono 124 e DDS PIXELFORMAT nelle dimensioni dell'intestazione \_ \_ è 32. Se DDS PIXELFORMAT dwFlags è impostato su DDPF FOURCC e dwFourCC è impostato su \_ "DX10", le dimensioni totali del file devono essere di \_ almeno 148 byte.

Esistono alcune varianti comuni in uso in cui il formato pixel è impostato su un codice FOURCC DDPF in cui dwFourCC è impostato su un valore di enumerazione \_ D3DFORMAT o DXGI \_ FORMAT. Non è possibile determinare se un valore di enumerazione è D3DFORMAT o DXGI FORMAT, pertanto è consigliabile usare l'estensione "DX10" e l'intestazione \_ \_ DDS HEADER DXT10 per archiviare dxgiFormat quando l'estensione \_ DDS PIXELFORMAT di base non è in grado di esprimere \_ il formato.

Per garantire la massima compatibilità, è consigliabile utilizzare lo standard DDS PIXELFORMAT per archiviare dati RGB non compressi e dati DXT1-5 perché non tutti gli strumenti DDS supportano \_ l'estensione DX10.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Uso di matrici di trame in Direct3D 10/11

Le nuove strutture DDS ([**DDS \_ HEADER**](dds-header.md) e [**\_ DDS HEADER \_ DXT10**](dds-header-dxt10.md)) in Direct3D 10/11 estendono il formato di file DDS per supportare una matrice di trame, ovvero un nuovo tipo di risorsa in Direct3D 10/11. Ecco un esempio di codice che illustra come accedere ai diversi livelli mipmap in una matrice di trame usando le nuove intestazioni.


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



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Formati di risorse file DDS comuni e contenuto dell'intestazione associato



| Formato risorsa                                                                            | dwFlags        | dwRGBBitCount | dwRBitMask | dwGBitMask | dwBBitMask | dwABitMask |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM<br/> D3DFMT \_ A8B8G8R8<br/>                       | DDS \_ RGBA      | 32            | 0xff       | 0xff00     | 0xff0000   | 0xff000000 |
| DXGI \_ FORMAT \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGBA      | 32            | 0xffff     | 0xffff0000 |            |            |
| \*\*<br/> FORMATO DXGI \_ \_ R10G10B10A2 \_ UNORM<br/> D3DFMT \_ A2B10G10R10<br/> | DDS \_ RGBA      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| DXGI \_ FORMAT \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | DDS \_ RGB       | 32            | 0xffff     | 0xffff0000 |            |            |
| FORMATO DXGI \_ \_ B5G5R5A1 \_ UNORM<br/> D3DFMT \_ A1R5G5B5<br/>                       | DDS \_ RGBA      | 16            | 0x7c00     | 0x3e0      | 0x1f       | 0x8000     |
| FORMATO DXGI \_ \_ B5G6R5 \_ UNORM<br/> D3FMT \_ R5G6B5<br/>                            | DDS \_ RGB       | 16            | 0xf800     | 0x7e0      | 0x1f       |            |
| DXGI \_ A8 \_ UNORM<br/> D3DFMT \_ A8<br/>                                           | DDS \_ ALPHA     | 8             |            |            |            | 0xff       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | DDS \_ RGBA      | 32            | 0xff0000   | 0xff00     | 0xff       | 0xff000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | DDS \_ RGB       | 32            | 0xff0000   | 0xff00     | 0xff       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | DDS \_ RGB       | 32            | 0xff       | 0xff00     | 0xff0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | DDS \_ RGBA      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xc0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | DDS \_ RGB       | 24            | 0xff0000   | 0xff00     | 0xff       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | DDS \_ RGB       | 16            | 0x7c00     | 0x3e0      | 0x1f       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | DDS \_ RGBA      | 16            | 0xf00      | 0xf0       | 0xf        | 0xf000     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | DDS \_ RGB       | 16            | 0xf00      | 0xf0       | 0xf        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | DDS \_ RGBA      | 16            | 0xe0       | 0x1c       | 0x3        | 0xff00     |
| D3DFMT \_ A8L8<br/>                                                                    | DDS \_ LUMINANCE | 16            | 0xff       |            |            | 0xff00     |
| D3DFMT \_ L16<br/>                                                                     | DDS \_ LUMINANCE | 16            | 0xffff     |            |            |            |
| D3DFMT \_ L8<br/>                                                                      | DDS \_ LUMINANCE | 8             | 0xff       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | DDS \_ LUMINANCE | 8             | 0xf        |            |            | 0xf0       |



 



| Formato risorsa                                                                             | dwFlags     | dwFourCC |
|---------------------------------------------------------------------------------------------|-------------|----------|
| FORMATO DXGI \_ \_ BC1 \_ UNORM<br/> D3DFMT \_ DXT1<br/>                                 | DDS \_ FOURCC | "DXT1"   |
| FORMATO DXGI \_ \_ BC2 \_ UNORM<br/> D3DFMT \_ DXT3<br/>                                 | DDS \_ FOURCC | "DXT3"   |
| FORMATO DXGI \_ \_ BC3 \_ UNORM<br/> D3DFMT \_ DXT5<br/>                                 | DDS \_ FOURCC | "DXT5"   |
| \*<br/> FORMATO DXGI \_ \_ BC4 \_ UNORM<br/>                                           | DDS \_ FOURCC | "BC4U"   |
| \*<br/> DXGI \_ FORMAT \_ BC4 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC4S"   |
| \*<br/> DXGI \_ FORMAT \_ BC5 \_ UNORM<br/>                                           | DDS \_ FOURCC | "ATI2"   |
| \*<br/> DXGI \_ FORMAT \_ BC5 \_ SNORM<br/>                                           | DDS \_ FOURCC | "BC5S"   |
| FORMATO DXGI \_ \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | DDS \_ FOURCC | "RGBG"   |
| DXGI \_ FORMAT \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | DDS \_ FOURCC | "GRGB"   |
| \*<br/> FORMATO DXGI \_ \_ R16G16B16A16 \_ UNORM<br/> D3DFMT \_ A16B16G16R16<br/>  | DDS \_ FOURCC | 36       |
| \*<br/> DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM<br/> D3DFMT \_ Q16W16V16U16<br/>  | DDS \_ FOURCC | 110      |
| \*<br/> FORMATO DXGI \_ \_ R16 \_ FLOAT<br/> D3DFMT \_ R16F<br/>                   | DDS \_ FOURCC | 111      |
| \*<br/> FORMATO DXGI \_ \_ R16G16 \_ FLOAT<br/> D3DFMT \_ G16R16F<br/>             | DDS \_ FOURCC | 112      |
| \*<br/> FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT<br/> D3DFMT \_ A16B16G16R16F<br/> | DDS \_ FOURCC | 113      |
| \*<br/> FORMATO DXGI \_ \_ R32 \_ FLOAT<br/> D3DFMT \_ R32F<br/>                   | DDS \_ FOURCC | 114      |
| \*<br/> FORMATO DXGI \_ \_ R32G32 \_ FLOAT<br/> D3DFMT \_ G32R32F<br/>             | DDS \_ FOURCC | 115      |
| \*<br/> FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT<br/> D3DFMT \_ A32B32G32R32F<br/> | DDS \_ FOURCC | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | DDS \_ FOURCC | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | DDS \_ FOURCC | "DXT4"   |
| D3DFMT \_ UYVY<br/>                                                                     | DDS \_ FOURCC | "UYVY"   |
| D3DFMT \_ YUY2<br/>                                                                     | DDS \_ FOURCC | "YUY2"   |
| D3DFMT \_ CxV8U8<br/>                                                                   | DDS \_ FOURCC | 117      |
| Qualsiasi formato DXGI                                                                             | DDS \_ FOURCC | "DX10"   |



 

\* = Un lettore DDS affidabile deve essere in grado di gestire questi codici di formato legacy. Tuttavia, un lettore DDS di questo tipo deve preferire l'uso dell'estensione di intestazione "DX10" quando scrive questi codici di formato per evitare ambiguità.

\*\* = A causa di alcuni problemi di lunga data nelle implementazioni comuni di lettori e writer DDS, il modo più affidabile per scrivere dati di tipo 10:10:10:2 è usare l'estensione di intestazione "DX10" con il codice [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) "24", ovvero il valore \_ DXGI FORMAT \_ R10G10B10A2 \_ UNORM. I dati D3DFMT A2R10G10B10 devono essere convertiti in dati di tipo \_ 10:10:10:2 prima di essere scritti come file DDS in formato DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dds](dx-graphics-dds.md)
</dt> </dl>

 

