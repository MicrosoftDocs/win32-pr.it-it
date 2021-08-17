---
description: Definisce i vari tipi di formati di superficie.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFORMAT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ec3f934d9d94bfcc1129414b652de770d205b6e190b9f901c6e4f35768f59217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732403"
---
# <a name="d3dformat"></a>D3DFORMAT

Definisce i vari tipi di formati di superficie.

``` syntax
typedef enum _D3DFORMAT {
    D3DFMT_UNKNOWN              =  0,

    D3DFMT_R8G8B8               = 20,
    D3DFMT_A8R8G8B8             = 21,
    D3DFMT_X8R8G8B8             = 22,
    D3DFMT_R5G6B5               = 23,
    D3DFMT_X1R5G5B5             = 24,
    D3DFMT_A1R5G5B5             = 25,
    D3DFMT_A4R4G4B4             = 26,
    D3DFMT_R3G3B2               = 27,
    D3DFMT_A8                   = 28,
    D3DFMT_A8R3G3B2             = 29,
    D3DFMT_X4R4G4B4             = 30,
    D3DFMT_A2B10G10R10          = 31,
    D3DFMT_A8B8G8R8             = 32,
    D3DFMT_X8B8G8R8             = 33,
    D3DFMT_G16R16               = 34,
    D3DFMT_A2R10G10B10          = 35,
    D3DFMT_A16B16G16R16         = 36,

    D3DFMT_A8P8                 = 40,
    D3DFMT_P8                   = 41,

    D3DFMT_L8                   = 50,
    D3DFMT_A8L8                 = 51,
    D3DFMT_A4L4                 = 52,

    D3DFMT_V8U8                 = 60,
    D3DFMT_L6V5U5               = 61,
    D3DFMT_X8L8V8U8             = 62,
    D3DFMT_Q8W8V8U8             = 63,
    D3DFMT_V16U16               = 64,
    D3DFMT_A2W10V10U10          = 67,

    D3DFMT_UYVY                 = MAKEFOURCC('U', 'Y', 'V', 'Y'),
    D3DFMT_R8G8_B8G8            = MAKEFOURCC('R', 'G', 'B', 'G'),
    D3DFMT_YUY2                 = MAKEFOURCC('Y', 'U', 'Y', '2'),
    D3DFMT_G8R8_G8B8            = MAKEFOURCC('G', 'R', 'G', 'B'),
    D3DFMT_DXT1                 = MAKEFOURCC('D', 'X', 'T', '1'),
    D3DFMT_DXT2                 = MAKEFOURCC('D', 'X', 'T', '2'),
    D3DFMT_DXT3                 = MAKEFOURCC('D', 'X', 'T', '3'),
    D3DFMT_DXT4                 = MAKEFOURCC('D', 'X', 'T', '4'),
    D3DFMT_DXT5                 = MAKEFOURCC('D', 'X', 'T', '5'),

    D3DFMT_D16_LOCKABLE         = 70,
    D3DFMT_D32                  = 71,
    D3DFMT_D15S1                = 73,
    D3DFMT_D24S8                = 75,
    D3DFMT_D24X8                = 77,
    D3DFMT_D24X4S4              = 79,
    D3DFMT_D16                  = 80,

    D3DFMT_D32F_LOCKABLE        = 82,
    D3DFMT_D24FS8               = 83,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_D32_LOCKABLE         = 84,
    D3DFMT_S8_LOCKABLE          = 85,
#endif // !D3D_DISABLE_9EX

    D3DFMT_L16                  = 81,

    D3DFMT_VERTEXDATA           =100,
    D3DFMT_INDEX16              =101,
    D3DFMT_INDEX32              =102,

    D3DFMT_Q16W16V16U16         =110,

    D3DFMT_MULTI2_ARGB8         = MAKEFOURCC('M','E','T','1'),

    D3DFMT_R16F                 = 111,
    D3DFMT_G16R16F              = 112,
    D3DFMT_A16B16G16R16F        = 113,

    D3DFMT_R32F                 = 114,
    D3DFMT_G32R32F              = 115,
    D3DFMT_A32B32G32R32F        = 116,

    D3DFMT_CxV8U8               = 117,

#if !defined(D3D_DISABLE_9EX)
    D3DFMT_A1                   = 118,
    D3DFMT_A2B10G10R10_XR_BIAS  = 119,
    D3DFMT_BINARYBUFFER         = 199,
#endif // !D3D_DISABLE_9EX

    D3DFMT_FORCE_DWORD          =0x7fffffff
} D3DFORMAT;
```

## <a name="remarks"></a>Commenti

Esistono diversi tipi di formati:

-   [BackBuffer o formati di visualizzazione](#backbuffer-or-display-formats)
-   [Formati di buffer](#buffer-formats)
-   [Formati di trama compressa DXTn](#dxtn-compressed-texture-formats)
-   [Formati a virgola mobile](#floating-point-formats)
-   [Formati FOURCC](#fourcc-formats)
-   [Formati IEEE](#ieee-formats)
-   [Formati misti](#mixed-formats)
-   [Formati con segno](#signed-formats)
-   [Formati senza segno](#unsigned-formats)
-   [Altri](#other)

Tutti i formati sono elencati da sinistra a destra, dal bit più significativo al bit meno significativo. Ad esempio, **D3DFORMAT \_ ARGB** viene ordinato dal canale di bit A (alfa) più significativo al canale di bit meno significativo B (blu). Quando si attraversano i dati di superficie, i dati vengono archiviati in memoria dal bit meno significativo al bit più significativo, il che significa che l'ordine dei canali in memoria è dal bit meno significativo (blu) al bit più significativo (alfa).

Il valore predefinito per i formati che contengono canali non definiti (G16R16, A8 e così via) è 1. L'unica eccezione è il formato A8, che viene inizializzato su 000 per i tre canali di colore.

L'ordine dei bit deriva dal byte più significativo per primo, quindi D3DFMT A8L8 indica che il byte più alto di questo formato a \_ 2 byte è alfa. **D3DFMT \_ D16** indica un valore intero a 16 bit e una superficie bloccabile dall'applicazione.

I formati pixel sono stati scelti per consentire l'espressione dei formati di estensione definiti dal fornitore dell'hardware e per includere il metodo FOURCC ben definito. Il set di formati riconosciuto dal runtime Direct3D è definito da D3DFORMAT.

Si noti che i formati vengono forniti da fornitori di hardware indipendenti (IHV) e molti codici FOURCC non sono elencati. I formati di questa enumerazione sono univoci in quanto sono stati sanzionati dal runtime, vale a dire che l'rasterizzazione dei riferimenti funzionerà su tutti questi tipi. I formati forniti da IHV saranno supportati dai singoli IHV scheda per scheda.

### <a name="backbuffer-or-display-formats"></a>BackBuffer o formati di visualizzazione

Questi formati sono gli unici formati validi per un buffer nascosto o una visualizzazione.



| Formato      | Buffer nascosto | Visualizza                   |
|-------------|-------------|---------------------------|
| A2R10G10B10 | x           | x (solo modalità schermo intero) |
| A8R8G8B8    | x           |                           |
| X8R8G8B8    | x           | x                         |
| A1R5G5B5    | x           |                           |
| X1R5G5B5    | x           | x                         |
| R5G6B5      | x           | x                         |



 

### <a name="buffer-formats"></a>Formati di buffer

I buffer di profondità, stencil, vertice e indice hanno formati univoci.



| Flag di buffer               | Valore | Formato                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ D16 \_ BLOCCABILE**  | 70    | Profondità in bit z-buffer a 16 bit.                                                                                                                    |
| **D3DFMT \_ D32**            | 71    | Profondità in bit z-buffer a 32 bit.                                                                                                                    |
| **D3DFMT \_ D15S1**          | 73    | Profondità in bit z-buffer a 16 bit dove 15 bit sono riservati per il canale di profondità e 1 bit è riservato per il canale stencil.                     |
| **D3DFMT \_ D24S8**          | 75    | Profondità in bit z-buffer a 32 bit con 24 bit per il canale di profondità e 8 bit per il canale stencil.                                             |
| **D3DFMT \_ D24X8**          | 77    | Profondità in bit z-buffer a 32 bit usando 24 bit per il canale di profondità.                                                                                |
| **D3DFMT \_ D24X4S4**        | 79    | Profondità in bit z-buffer a 32 bit usando 24 bit per il canale di profondità e 4 bit per il canale stencil.                                             |
| **D3DFMT \_ D32F \_ LOCKABLE** | 82    | Formato bloccabile in cui il valore di profondità è rappresentato come numero a virgola mobile IEEE standard.                                              |
| **D3DFMT \_ D24FS8**         | 83    | Formato non bloccabile che contiene 24 bit di profondità (in un formato a virgola mobile a 24 bit - 20e4) e 8 bit di stencil.                        |
| **D3DFMT \_ D32 \_ LOCKABLE**  | 84    | Buffer di profondità a 32 bit bloccabile. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/>  |
| **D3DFMT \_ S8 \_ BLOCCABILE**   | 85    | Buffer degli stencil a 8 bit bloccabile. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/> |
| **D3DFMT \_ D16**            | 80    | Profondità in bit z-buffer a 16 bit.                                                                                                                    |
| **D3DFMT \_ VERTEXDATA**     | 100   | Descrive la superficie del buffer dei vertici.                                                                                                            |
| **D3DFMT \_ INDEX16**        | 101   | Profondità index buffer bit a 16 bit.                                                                                                                |
| **D3DFMT \_ INDEX32**        | 102   | Profondità index buffer bit a 32 bit.                                                                                                                |



 

Tutti i formati depth-stencil, ad eccezione di D3DFMT \_ D16 LOCKABLE, non indicano un particolare ordinamento dei bit per pixel e il driver può utilizzare più del numero indicato di canali bit per profondità (ma non del canale \_ stencil).

### <a name="dxtn-compressed-texture-formats"></a>Formati di trama compressa DXTn

Questi flag vengono usati per le trame compresse:



| Flag di trama compressa DXTn | Valore                          | Formato                          |
|-------------------------------|--------------------------------|---------------------------------|
| **D3DFMT \_ DXT1**              | MAKEFOURCC('D', 'X', 'T', '1') | Formato della trama di compressione DXT1 |
| **D3DFMT \_ DXT2**              | MAKEFOURCC('D', 'X', 'T', '2') | Formato della trama di compressione DXT2 |
| **D3DFMT \_ DXT3**              | MAKEFOURCC('D', 'X', 'T', '3') | Formato della trama di compressione DXT3 |
| **D3DFMT \_ DXT4**              | MAKEFOURCC('D', 'X', 'T', '4') | Formato della trama di compressione DXT4 |
| **D3DFMT \_ DXT5**              | MAKEFOURCC('D', 'X', 'T', '5') | Formato della trama di compressione DXT5 |



 

Il runtime non consentirà a un'applicazione di creare una superficie usando un formato DXTn a meno che le dimensioni della superficie non siano multipli di 4. Questo vale per le superfici non schermate, le destinazioni di rendering, le trame 2D, le trame dei cubi e le trame di volume.

### <a name="floating-point-formats"></a>Floating-Point formati

Questi flag vengono usati per i formati di superficie a virgola mobile. Questi formati a 16 bit per canale sono noti anche come formati s10e5.



| Flag a virgola mobile      | Valore | Formato                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R16F**          | 111   | Formato float a 16 bit con 16 bit per il canale rosso.                                   |
| **D3DFMT \_ G16R16F**       | 112   | Formato float a 32 bit con 16 bit per il canale rosso e 16 bit per il canale verde. |
| **D3DFMT \_ A16B16G16R16F** | 113   | Formato float a 64 bit con 16 bit per ogni canale (alfa, blu, verde, rosso).        |



 

### <a name="fourcc-formats"></a>Formati FOURCC

I dati in formato FOURCC sono dati compressi.

### <a name="makefourcc"></a>MAKEFOURCC

Una macro per la generazione di codici di quattro caratteri è la seguente:

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

Ecco i formati FOURCC definiti:



| Flag FOURCC              | Valore                          | Formato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ MULTI2 \_ ARGB8** | MAKEFOURCC('M','E','T','1')    | Trama MultiElement (non compressa)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **D3DFMT \_ G8R8 \_ G8B8**    | MAKEFOURCC('G', 'R', 'G', 'B') | Un formato RGB con pacchetto a 16 bit analogo a YUY2 (Y0U0, Y1V0, Y2U2 e così via). Richiede una coppia di pixel per rappresentare correttamente il valore del colore. Il primo pixel della coppia contiene 8 bit di verde (negli 8 bit alti) e 8 bit di rosso (negli 8 bit bassi). Il secondo pixel contiene 8 bit di verde (negli 8 bit alti) e 8 bit di blu (negli 8 bit bassi). Insieme, i due pixel condividono i componenti rosso e blu, mentre ognuno ha un componente verde univoco (G0R0, G1B0, G2R2 e così via). Il campionatore di trama non normalizza i colori quando si cerca in un pixel shader; rimangono nell'intervallo da 0,0f a 255,0f. Questo vale per tutti i modelli pixel shader programmabili. Per la funzione fissa pixel shader, l'hardware deve normalizzare l'intervallo da 0.f a 1.f e trattarlo essenzialmente come trama YUY2. L'hardware che espone questo formato deve avere il membro PixelShader1xMaxValue di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) impostato su un valore in grado di gestire tale intervallo. |
| **D3DFMT \_ R8G8 \_ B8G8**    | MAKEFOURCC('R', 'G', 'B', 'G') | Un formato RGB con pacchetto a 16 bit analogo a UYVY (U0Y0, V0Y1, U2Y2 e così via). Richiede una coppia di pixel per rappresentare correttamente il valore del colore. Il primo pixel della coppia contiene 8 bit di verde (negli 8 bit bassi) e 8 bit di rosso (negli 8 bit alti). Il secondo pixel contiene 8 bit di verde (negli 8 bit bassi) e 8 bit di blu (negli 8 bit alti). Insieme, i due pixel condividono i componenti rosso e blu, mentre ognuno ha un componente verde univoco (R0G0, B0G1, R2G2 e così via). Il campionatore di trama non normalizza i colori quando si cerca in un pixel shader; rimangono nell'intervallo da 0,0f a 255,0f. Questo vale per tutti i modelli pixel shader programmabili. Per la funzione fissa pixel shader, l'hardware deve normalizzare l'intervallo da 0.f a 1.f e trattarlo essenzialmente come trama YUY2. L'hardware che espone questo formato deve avere il membro PixelShader1xMaxValue di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) impostato su un valore in grado di gestire tale intervallo.     |
| **D3DFMT \_ UYVY**          | MAKEFOURCC('U', 'Y', 'V', 'Y') | Formato UYVY (conformità PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **D3DFMT \_ YUY2**          | MAKEFOURCC('Y', 'U', 'Y', '2') | Formato YUY2 (conformità PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a>Formati IEEE

Questi flag vengono usati per i formati di superficie a virgola mobile. Questi formati a 32 bit per canale sono noti anche come formati s23e8.



| Flag a virgola mobile      | Valore | Formato                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **D3DFMT \_ R32F**          | 114   | Formato float a 32 bit con 32 bit per il canale rosso.                                   |
| **D3DFMT \_ G32R32F**       | 115   | Formato float a 64 bit con 32 bit per il canale rosso e 32 bit per il canale verde. |
| **D3DFMT \_ A32B32G32R32F** | 116   | Formato float a 128 bit con 32 bit per ogni canale (alfa, blu, verde, rosso).       |



 

### <a name="mixed-formats"></a>Formati misti

I dati in formati misti possono contenere una combinazione di dati senza segno e dati firmati.



| Flag di formato misto      | Valore | Formato                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| **D3DFMT \_ L6V5U5**      | 61    | Formato bump-map a 16 bit con luminance con 6 bit per la luminance e 5 bit per v e you. |
| **D3DFMT \_ X8L8V8U8**    | 62    | Formato mappa a rilievo a 32 bit con luminanza che usa 8 bit per ogni canale.                           |
| **D3DFMT \_ A2W10V10U10** | 67    | Formato bump-map a 32 bit con 2 bit per alfa e 10 bit ciascuno per w, v e per l'utente.                |



 

### <a name="signed-formats"></a>Formati firmati

I dati in un formato con segno possono essere sia positivi che negativi. I formati con segno usano combinazioni di dati (U), (V), (W) e (Q).



| Flag di formato con segno      | Valore | Formato                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ V8U8**         | 60    | Formato bump-map a 16 bit con 8 bit ognuno per i dati e v.                                                |
| **D3DFMT \_ Q8W8V8U8**     | 63    | Formato bump-map a 32 bit con 8 bit per ogni canale.                                                     |
| **D3DFMT \_ V16U16**       | 64    | Formato bump-map a 32 bit con 16 bit per ogni canale.                                                    |
| **D3DFMT \_ Q16W16V16U16** | 110   | Formato bump-map a 64 bit con 16 bit per ogni componente.                                                  |
| **D3DFMT \_ CxV8U8**       | 117   | Formato di compressione normale a 16 bit. Il campionatore di trama calcola il canale C da: C = sqrt(1 - U² - V²). |



 

### <a name="unsigned-formats"></a>Formati senza segno

I dati in un formato senza segno devono essere positivi. I formati senza segno usano combinazioni di dati (R)ed, (G)reen, (B)lue, (A)lpha, (L)uminance e (P)alette. I dati della tavolozza vengono definiti anche dati indicizzati a colori perché vengono usati per indicizzare una tavolozza dei colori.



| Flag di formato senza segno             | Valore | Formato                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ R8G8B8**                | 20    | Formato di pixel RGB a 24 bit con 8 bit per canale.                                                                                                                          |
| **D3DFMT \_ A8R8G8B8**              | 21    | Formato pixel ARGB a 32 bit con alfa, usando 8 bit per canale.                                                                                                            |
| **D3DFMT \_ X8R8G8B8**              | 22    | Formato pixel RGB a 32 bit, dove 8 bit sono riservati per ogni colore.                                                                                                        |
| **D3DFMT \_ R5G6B5**                | 23    | Formato pixel RGB a 16 bit con 5 bit per il rosso, 6 bit per il verde e 5 bit per il blu.                                                                                       |
| **D3DFMT \_ X1R5G5B5**              | 24    | Formato pixel a 16 bit in cui i 5 bit sono riservati per ogni colore.                                                                                                             |
| **D3DFMT \_ A1R5G5B5**              | 25    | Formato pixel a 16 bit in cui i 5 bit sono riservati per ogni colore e 1 bit è riservato per alfa.                                                                             |
| **D3DFMT \_ A4R4G4B4**              | 26    | Formato pixel ARGB a 16 bit con 4 bit per ogni canale.                                                                                                                    |
| **D3DFMT \_ R3G3B2**                | 27    | Formato di trama RGB a 8 bit che usa 3 bit per il rosso, 3 bit per il verde e 2 bit per il blu.                                                                                     |
| **D3DFMT \_ A8**                    | 28    | Solo alfa a 8 bit.                                                                                                                                                         |
| **D3DFMT \_ A8R3G3B2**              | 29    | Formato di trama ARGB a 16 bit con 8 bit per alfa, 3 bit ciascuno per rosso e verde e 2 bit per il blu.                                                                    |
| **D3DFMT \_ X4R4G4B4**              | 30    | Formato pixel RGB a 16 bit con 4 bit per ogni colore.                                                                                                                      |
| **D3DFMT \_ A2B10G10R10**           | 31    | Formato pixel a 32 bit con 10 bit per ogni colore e 2 bit per alfa.                                                                                                    |
| **D3DFMT \_ A8B8G8R8**              | 32    | Formato pixel ARGB a 32 bit con alfa, usando 8 bit per canale.                                                                                                            |
| **D3DFMT \_ X8B8G8R8**              | 33    | Formato pixel RGB a 32 bit, dove 8 bit sono riservati per ogni colore.                                                                                                        |
| **D3DFMT \_ G16R16**                | 34    | Formato pixel a 32 bit con 16 bit ciascuno per verde e rosso.                                                                                                                 |
| **D3DFMT \_ A2R10G10B10**           | 35    | Formato pixel a 32 bit con 10 bit ciascuno per rosso, verde e blu e 2 bit per alfa.                                                                                    |
| **D3DFMT \_ A16B16G16R16**          | 36    | Formato pixel a 64 bit con 16 bit per ogni componente.                                                                                                                     |
| **D3DFMT \_ A8P8**                  | 40    | Colore a 8 bit indicizzato con 8 bit di alfa.                                                                                                                                 |
| **D3DFMT \_ P8**                    | 41    | Colore a 8 bit indicizzato.                                                                                                                                                      |
| **D3DFMT \_ L8**                    | 50    | Solo luminanza a 8 bit.                                                                                                                                                     |
| **D3DFMT \_ L16**                   | 81    | Solo luminanza a 16 bit.                                                                                                                                                    |
| **D3DFMT \_ A8L8**                  | 51    | 16 bit con 8 bit ciascuno per alfa e luminanza.                                                                                                                         |
| **D3DFMT \_ A4L4**                  | 52    | 8 bit con 4 bit ciascuno per alfa e luminanza.                                                                                                                          |
| **D3DFMT \_ A1**                    | 118   | Monocromatico a 1 bit. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/>                                            |
| **D3DFMT \_ A2B10G10R10 \_ XR \_ BIAS** | 119   | Punto fisso con distorsione 2.8. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/>                                      |
| **D3DFMT \_ BINARYBUFFER**          | 199   | Formato binario che indica che i dati non hanno un tipo intrinseco. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/> |



 

### <a name="other"></a>Altro

Questo flag viene usato per i formati non definiti.



| Altri flag         | Valore | Formato                    |
|---------------------|-------|---------------------------|
| **D3DFMT \_ UNKNOWN** | 0     | Il formato della superficie è sconosciuto |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




