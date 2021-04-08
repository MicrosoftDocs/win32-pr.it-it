---
description: Definisce i vari tipi di formati di superficie.
ms.assetid: a222e3bb-310c-4019-93ee-6a2da2a46ded
title: D3DFORMAT (D3D9Types. h)
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
ms.openlocfilehash: 228884435322992b8c87d20a9f351161f945c43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762107"
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

-   [Formati di visualizzazione o backBuffer](#backbuffer-or-display-formats)
-   [Formati di buffer](#buffer-formats)
-   [Formati di trama compressi DXTn](#dxtn-compressed-texture-formats)
-   [Formati a virgola mobile](#floating-point-formats)
-   [Formati FOURCC](#fourcc-formats)
-   [Formati IEEE](#ieee-formats)
-   [Formati misti](#mixed-formats)
-   [Formati firmati](#signed-formats)
-   [Formati non firmati](#unsigned-formats)
-   [Altri](#other)

Tutti i formati sono elencati da sinistra a destra, da un bit più significativo a un bit meno significativo. Ad esempio, **D3DFORMAT \_ ARGB** viene ordinato dal canale di bit più significativo a (alfa) al canale di bit meno significativo B (blu). Quando si attraversano i dati della superficie, i dati vengono archiviati in memoria dal bit meno significativo al bit più significativo, il che significa che l'ordine dei canali in memoria è da un bit meno significativo (blu) a un bit più significativo (alfa).

Il valore predefinito per i formati che contengono canali non definiti (G16R16, A8 e così via) è 1. L'unica eccezione è il formato A8, che viene inizializzato a 000 per i tre canali dei colori.

L'ordine dei bit è primo dal byte più significativo, quindi D3DFMT \_ A8L8 indica che il byte elevato del formato a 2 byte è alfa. **D3DFMT \_ D16** indica un valore integer a 16 bit e una superficie bloccabile per l'applicazione.

Sono stati scelti formati pixel per abilitare l'espressione dei formati di estensione definiti dal fornitore di hardware, oltre a includere il metodo FOURCC ben definito. Il set di formati riconosciuto dal runtime Direct3D è definito da D3DFORMAT.

Si noti che i formati sono forniti da fornitori di hardware indipendenti (IHV) e molti codici FOURCC non sono elencati. I formati in questa enumerazione sono univoci in quanto sono approvati dal runtime, vale a dire che l'rasterizzazione dei riferimenti funzionerà su tutti questi tipi. I formati forniti da IHV saranno supportati dai singoli IHV in base a una scheda.

### <a name="backbuffer-or-display-formats"></a>Formati di visualizzazione o backBuffer

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

I buffer di profondità, stencil, vertex e index hanno formati univoci.



| Flag del buffer               | Valore | Formato                                                                                                                                        |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ D16 \_ lockable**  | 70    | profondità di bit del buffer z a 16 bit.                                                                                                                    |
| **\_D32 D3DFMT**            | 71    | profondità di bit del buffer z a 32 bit.                                                                                                                    |
| **\_D15S1 D3DFMT**          | 73    | profondità di bit del buffer z a 16 bit, dove 15 bit sono riservati per il canale di profondità e 1 bit è riservato per il canale dello stencil.                     |
| **\_D24S8 D3DFMT**          | 75    | profondità di bit del buffer z a 32 bit con 24 bit per il canale di profondità e 8 bit per il canale dello stencil.                                             |
| **\_D24X8 D3DFMT**          | 77    | profondità di bit del buffer z a 32 bit con 24 bit per il canale di profondità.                                                                                |
| **\_D24X4S4 D3DFMT**        | 79    | profondità di bit del buffer z a 32 bit con 24 bit per il canale di profondità e 4 bit per il canale dello stencil.                                             |
| **D3DFMT \_ D32F \_ lockable** | 82    | Formato bloccabile in cui il valore di profondità viene rappresentato come numero a virgola mobile IEEE standard.                                              |
| **\_D24FS8 D3DFMT**         | 83    | Formato non bloccabile che contiene 24 bit di profondità (in un formato a virgola mobile a 24 bit-20E4) e 8 bit di stencil.                        |
| **D3DFMT \_ D32 \_ lockable**  | 84    | Buffer di profondità a 32 bit bloccabile. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/>  |
| **D3DFMT \_ S8 \_ bloccabile**   | 85    | Buffer di stencil a 8 bit bloccabile. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/> |
| **\_D16 D3DFMT**            | 80    | profondità di bit del buffer z a 16 bit.                                                                                                                    |
| **\_VERTEXDATA D3DFMT**     | 100   | Descrive una superficie del buffer del vertice.                                                                                                            |
| **\_INDEX16 D3DFMT**        | 101   | profondità dei bit del buffer di indice a 16 bit.                                                                                                                |
| **\_INDEX32 D3DFMT**        | 102   | profondità di bit del buffer dell'indice a 32 bit.                                                                                                                |



 

Tutti i formati di stencil Depth, ad eccezione \_ di D3DFMT D16 \_ lockable, non indicano alcun ordine di bit specifico per pixel e il driver è autorizzato a utilizzare un numero di canali superiore al numero indicato di bit per profondità (ma non il canale dello stencil).

### <a name="dxtn-compressed-texture-formats"></a>Formati di trama compressi DXTn

Questi flag vengono usati per le trame compresse:



| Flag di trama compressi DXTn | Valore                          | Formato                          |
|-------------------------------|--------------------------------|---------------------------------|
| **\_DXT1 D3DFMT**              | MAKEFOURCC (' D',' X ',' T',' 1') | Formato trama compressione DXT1 |
| **\_DXT2 D3DFMT**              | MAKEFOURCC (' D',' X ',' T',' 2') | Formato trama compressione DXT2 |
| **\_DXT3 D3DFMT**              | MAKEFOURCC (' D',' X ',' T',' 3') | Formato trama compressione DXT3 |
| **\_DXT4 D3DFMT**              | MAKEFOURCC (' D',' X ',' T',' 4') | Formato trama compressione DXT4 |
| **\_DXT5 D3DFMT**              | MAKEFOURCC (' D',' X ',' T',' 5') | Formato trama compressione DXT5 |



 

Il runtime non consentirà a un'applicazione di creare una superficie utilizzando un formato DXTn, a meno che le dimensioni della superficie non siano multipli di 4. Questo vale per le superfici semplici Offscreen, le destinazioni di rendering, le trame 2D, le trame del cubo e le trame del volume.

### <a name="floating-point-formats"></a>Formati di Floating-Point

Questi flag vengono utilizzati per i formati di superficie a virgola mobile. Questi formati a 16 bit per canale sono noti anche come formati s10e5.



| Flag a virgola mobile      | Valore | Formato                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **\_R16F D3DFMT**          | 111   | formato float a 16 bit con 16 bit per il canale rosso.                                   |
| **\_G16R16F D3DFMT**       | 112   | formato float a 32 bit con 16 bit per il canale rosso e 16 bit per il canale verde. |
| **\_A16B16G16R16F D3DFMT** | 113   | formato float a 64 bit con 16 bit per ogni canale (alfa, blu, verde, rosso).        |



 

### <a name="fourcc-formats"></a>Formati FOURCC

I dati in un formato FOURCC sono dati compressi.

### <a name="makefourcc"></a>MAKEFOURCC

Di seguito è riportata una macro per la generazione di codici di quattro caratteri:

``` syntax
#define MAKEFOURCC(ch0, ch1, ch2, ch3)                              \
                ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |   \
                ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 ))
```

Di seguito sono riportati i formati FOURCC definiti:



| Flag FOURCC              | Valore                          | Formato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DFMT \_ MULTi2 \_ ARGB8** | MAKEFOURCC (' M',' È,' T',' 1')    | Trama a più elementi (non compresso)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **D3DFMT \_ G8R8 \_ G8B8**    | MAKEFOURCC (' G ',' R ',' G ',' B ') | Formato RGB compresso a 16 bit analogo a YUY2 (Y0U0, Y1V0, Y2U2 e così via). Richiede una coppia di pixel per rappresentare correttamente il valore del colore. Il primo pixel della coppia contiene 8 bit di verde (negli 8 bit alti) e 8 bit di rosso (negli 8 bit bassi). Il secondo pixel contiene 8 bit di verde (negli 8 bit alti) e 8 bit di blu (negli 8 bit bassi). Insieme, i due pixel condividono i componenti rosso e blu, mentre ognuno ha un componente verde univoco (G0R0, G1B0, G2R2 e così via). Il campionatore di trame non normalizza i colori durante la ricerca in un pixel shader; rimangono nell'intervallo da 0,0 f a 255.0 f. Questo vale per tutti i modelli di pixel shader programmabili. Per la funzione Fixed pixel shader, l'hardware deve normalizzarsi nell'intervallo da 0. f a 1. f e essenzialmente considerarlo come trama YUY2. Per l'hardware che espone questo formato il membro PixelShader1xMaxValue di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) deve essere impostato su un valore in grado di gestire tale intervallo. |
| **D3DFMT \_ R8G8 \_ B8G8**    | MAKEFOURCC (' R ',' G ',' B ',' G ') | Formato RGB compresso a 16 bit analogo a UYVY (U0Y0, V0Y1, U2Y2 e così via). Richiede una coppia di pixel per rappresentare correttamente il valore del colore. Il primo pixel della coppia contiene 8 bit di verde (negli 8 bit bassi) e 8 bit di rosso (negli 8 bit superiori). Il secondo pixel contiene 8 bit di verde (negli 8 bit bassi) e 8 bit di blu (negli 8 bit superiori). Insieme, i due pixel condividono i componenti rosso e blu, mentre ognuno ha un componente verde univoco (R0G0, B0G1, R2G2 e così via). Il campionatore di trame non normalizza i colori durante la ricerca in un pixel shader; rimangono nell'intervallo da 0,0 f a 255.0 f. Questo vale per tutti i modelli di pixel shader programmabili. Per la funzione Fixed pixel shader, l'hardware deve normalizzarsi nell'intervallo da 0. f a 1. f e essenzialmente considerarlo come trama YUY2. Per l'hardware che espone questo formato il membro PixelShader1xMaxValue di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) deve essere impostato su un valore in grado di gestire tale intervallo.     |
| **\_UYVY D3DFMT**          | MAKEFOURCC (' U ',' Y ',' V',' Y ') | Formato UYVY (conformità PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **\_YUY2 D3DFMT**          | MAKEFOURCC (' Y ',' U ',' Y ',' 2') | Formato YUY2 (conformità PC98)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="ieee-formats"></a>Formati IEEE

Questi flag vengono utilizzati per i formati di superficie a virgola mobile. Questi formati 32-bits per canale sono noti anche come formati s23e8.



| Flag a virgola mobile      | Valore | Formato                                                                                   |
|---------------------------|-------|------------------------------------------------------------------------------------------|
| **\_R32F D3DFMT**          | 114   | formato float a 32 bit con 32 bit per il canale rosso.                                   |
| **\_G32R32F D3DFMT**       | 115   | formato float a 64 bit con 32 bit per il canale rosso e 32 bit per il canale verde. |
| **\_A32B32G32R32F D3DFMT** | 116   | formato float a 128 bit con 32 bit per ogni canale (alfa, blu, verde, rosso).       |



 

### <a name="mixed-formats"></a>Formati misti

I dati in formati misti possono contenere una combinazione di dati non firmati e dati firmati.



| Flag di formato misto      | Valore | Formato                                                                                         |
|-------------------------|-------|------------------------------------------------------------------------------------------------|
| **\_L6V5U5 D3DFMT**      | 61    | formato di mappa Bump a 16 bit con luminanza usando 6 bit per la luminanza e 5 bit per v e l'utente. |
| **\_X8L8V8U8 D3DFMT**    | 62    | formato di mappa Bump a 32 bit con luminanza con 8 bit per ogni canale.                           |
| **\_A2W10V10U10 D3DFMT** | 67    | formato di mappa Bump a 32 bit che usa 2 bit per Alpha e 10 bit ciascuno per w, v e l'utente.                |



 

### <a name="signed-formats"></a>Formati firmati

I dati in un formato firmato possono essere sia positivi che negativi. I formati firmati usano combinazioni di dati (U), (V), (W) e (Q).



| Flag di formato firmato      | Valore | Formato                                                                                                    |
|--------------------------|-------|-----------------------------------------------------------------------------------------------------------|
| **\_V8U8 D3DFMT**         | 60    | formato della mappa Bump a 16 bit con 8 bit ciascuno per i dati utente e v.                                                |
| **\_Q8W8V8U8 D3DFMT**     | 63    | formato di mappa Bump a 32 bit con 8 bit per ogni canale.                                                     |
| **\_V16U16 D3DFMT**       | 64    | formato di mappa Bump a 32 bit con 16 bit per ogni canale.                                                    |
| **\_Q16W16V16U16 D3DFMT** | 110   | formato di mappa Bump a 64 bit con 16 bit per ogni componente.                                                  |
| **\_CXV8U8 D3DFMT**       | 117   | formato di compressione normale a 16 bit. Il campionatore di trame calcola il canale C da: C = sqrt (1-U ²-V ²). |



 

### <a name="unsigned-formats"></a>Formati non firmati

I dati in un formato senza segno devono essere positivi. I formati non firmati usano combinazioni di dati (R) ed, (G) reen, (B) lue, (A) lpha, (L) uminance e (P) alette dei colori. I dati della tavolozza sono anche denominati dati indicizzati a colori perché i dati vengono utilizzati per indicizzare una tavolozza dei colori.



| Flag di formato senza segno             | Valore | Formato                                                                                                                                                                    |
|-----------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_R8G8B8 D3DFMT**                | 20    | formato pixel RGB a 24 bit con 8 bit per canale.                                                                                                                          |
| **\_A8R8G8B8 D3DFMT**              | 21    | formato pixel ARGB a 32 bit con Alpha, con 8 bit per canale.                                                                                                            |
| **\_X8R8G8B8 D3DFMT**              | 22    | formato pixel RGB a 32 bit, dove 8 bit sono riservati per ogni colore.                                                                                                        |
| **\_R5G6B5 D3DFMT**                | 23    | formato pixel RGB a 16 bit con 5 bit per il rosso, 6 bit per il verde e 5 bit per il blu.                                                                                       |
| **\_X1R5G5B5 D3DFMT**              | 24    | formato pixel a 16 bit in cui 5 bit sono riservati per ogni colore.                                                                                                             |
| **\_A1R5G5B5 D3DFMT**              | 25    | formato pixel a 16 bit in cui 5 bit sono riservati per ogni colore e 1 bit è riservato per Alpha.                                                                             |
| **\_A4R4G4B4 D3DFMT**              | 26    | formato pixel ARGB a 16 bit con 4 bit per ogni canale.                                                                                                                    |
| **\_R3G3B2 D3DFMT**                | 27    | formato di trama RGB a 8 bit con 3 bit per il rosso, 3 bit per il verde e 2 bit per il blu.                                                                                     |
| **D3DFMT \_ a8**                    | 28    | solo Alpha a 8 bit.                                                                                                                                                         |
| **\_A8R3G3B2 D3DFMT**              | 29    | formato di trama ARGB a 16 bit con 8 bit per alfa, 3 bit per colore rosso e verde e 2 bit per il blu.                                                                    |
| **\_X4R4G4B4 D3DFMT**              | 30    | formato pixel RGB a 16 bit con 4 bit per ogni colore.                                                                                                                      |
| **\_A2B10G10R10 D3DFMT**           | 31    | formato pixel a 32 bit che usa 10 bit per ogni colore e 2 bit per alfa.                                                                                                    |
| **\_A8B8G8R8 D3DFMT**              | 32    | formato pixel ARGB a 32 bit con Alpha, con 8 bit per canale.                                                                                                            |
| **\_X8B8G8R8 D3DFMT**              | 33    | formato pixel RGB a 32 bit, dove 8 bit sono riservati per ogni colore.                                                                                                        |
| **\_G16R16 D3DFMT**                | 34    | formato pixel a 32 bit con 16 bit ciascuno per verde e rosso.                                                                                                                 |
| **\_A2R10G10B10 D3DFMT**           | 35    | formato pixel a 32 bit che usa 10 bit per ogni rosso, verde e blu e 2 bit per alfa.                                                                                    |
| **\_A16B16G16R16 D3DFMT**          | 36    | formato pixel a 64 bit con 16 bit per ogni componente.                                                                                                                     |
| **\_A8P8 D3DFMT**                  | 40    | colore a 8 bit indicizzato con 8 bit di alfa.                                                                                                                                 |
| **D3DFMT \_ P8**                    | 41    | colore a 8 bit indicizzato.                                                                                                                                                      |
| **\_L8 D3DFMT**                    | 50    | solo luminanza a 8 bit.                                                                                                                                                     |
| **\_L16 D3DFMT**                   | 81    | solo luminanza a 16 bit.                                                                                                                                                    |
| **\_A8L8 D3DFMT**                  | 51    | a 16 bit con 8 bit per alfa e luminanza.                                                                                                                         |
| **\_A4L4 D3DFMT**                  | 52    | a 8 bit con 4 bit per alfa e luminanza.                                                                                                                          |
| **D3DFMT \_ a1**                    | 118   | monocromatico a 1 bit. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/>                                            |
| **D3DFMT \_ A2B10G10R10 \_ XR \_ Bias** | 119   | 2,8-punto fisso distorta. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/>                                      |
| **\_BINARYBUFFER D3DFMT**          | 199   | Formato binario che indica che i dati non hanno un tipo intrinseco. **Differenze tra Direct3D 9 e Direct3D 9Ex:** Questo flag è disponibile solo in Direct3D 9Ex.<br/> |



 

### <a name="other"></a>Altro

Questo flag viene utilizzato per i formati non definiti.



| Altri flag         | Valore | Formato                    |
|---------------------|-------|---------------------------|
| **D3DFMT \_ sconosciuto** | 0     | Il formato della superficie è sconosciuto |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




