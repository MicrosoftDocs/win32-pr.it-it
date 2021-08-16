---
description: In questo argomento vengono presentati i formati pixel forniti da Windows Imaging Component (WIC).
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Panoramica dei formati di pixel nativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379e67d422ccbd05ef178e67eb25c973e6b5943ef85d22873097f245f8914a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206339"
---
# <a name="native-pixel-formats-overview"></a>Panoramica dei formati di pixel nativi

In questo argomento vengono presentati i formati pixel forniti da Windows Imaging Component (WIC).

Un formato pixel descrive il layout di memoria di ogni pixel in una bitmap. Questo layout di memoria descrive come vengono codificati i dati immagine di una bitmap specificando il formato numerico e l'organizzazione del canale colori. WIC supporta diversi formati numerici per più schemi organizzativi del canale colori, offrendo un'ampia gamma di formati di pixel.

-   [Profondità in bit](#bit-depth)
-   [Codifica numerica](#numerical-encoding)
-   [Canali colori](#color-channels)
    -   [Modello colori RGB/BGR](#rgbbgr-color-model)
    -   [Modello colori CMYK](#cmyk-color-model)
    -   [Modello colori a n canali](#n-channel-color-model)
    -   [Modelli a colori indicizzati e in scala di grigi](#indexed-and-grayscale-color-models)
    -   [Modello a colori Y'CbCr](#ycbcr-color-model)
-   [Formato pixel WIC](#wic-pixel-format)
    -   [Formati di pixel non definiti](#undefined-pixel-formats)
    -   [Formati di pixel indicizzati](#indexed-pixel-formats)
    -   [Formati di pixel di bit packed](#packed-bit-pixel-formats)
    -   [Formati pixel in scala di grigi](#grayscale-pixel-formats)
    -   [Formati RGB/BGR Pixel](#rgbbgr-pixel-formats)
    -   [Formati pixel CMYK](#cmyk-pixel-formats)
    -   [Formati pixel a n canali](#n-channel-pixel-formats)
    -   [Formati di pixel solo alfa](#alpha-only-pixel-formats)
    -   [Formati pixel Y'CbCr](#ycbcr-pixel-formats)
-   [Spazio colore](#color-space)
-   [Formati di immagine nativa](#native-image-formats)
    -   [Codec nativo BMP](#bmp-native-codec)
    -   [Codec nativo GIF](#gif-native-codec)
    -   [Codec ICO nativo](#ico-native-codec)
    -   [Codec nativo JPEG](#jpeg-native-codec)
    -   [Codec PNG nativo](#png-native-codec)
    -   [Codec NATIVO TIFF](#tiff-native-codec)
    -   [Codec nativo JPEG-XR](#jpeg-xr-native-codec)
-   [Codec nativo DDS](#dds-native-codec)
-   [Estendibilità del formato pixel](#pixel-format-extensibility)
-   [Argomenti correlati](#related-topics)

## <a name="bit-depth"></a>Profondità in bit

La *profondità in bit* è il numero di bit usati per codificare ogni canale di colore. Attualmente, la maggior parte delle immagini digitali usa una profondità in bit di 8, vale a dire che ogni canale di colore in un pixel è rappresentato da 8 bit, fornendo 2⁸ (256) valori univoci per canale. Un'immagine con una profondità in bit di 8 e tre canali di colori (ad esempio rosso, verde e blu) usa 24 bit per pixel (bpp), che fornisce 2⁴ (16.777.216) colori diversi per pixel.

Per una migliore risoluzione dei colori, è possibile usare una profondità in bit di 16 o 32. In questo modo, ogni canale di colore ha 2⁶ (65.536) o 2 i valori univoci, a un costo di più memoria per pixel.

In alcuni formati, la profondità in bit non è un multiplo di 8. Questi formati sono *detti formati packed,* perché i canali di colore in un pixel non sono allineati ai limiti dei byte. Ad esempio, se la profondità in bit di 5, tre canali di colore possono essere archiviati in 16 bit (incluso 1 bit di spaziatura interna, per rendere i pixel allineati ai byte). I formati pack sono utili quando la memoria o la potenza di elaborazione sono limitate.

## <a name="numerical-encoding"></a>Codifica numerica

Per la maggior parte delle immagini digitali attuali, i byte senza segno e i valori short integer senza segno vengono usati per descrivere l'intervallo numerico di ogni canale di colore. Il valore minimo (0) rappresenta l'intensità zero in un singolo canale di colore e il nero si ottiene quando tutti i canali di colore sono pari a zero. Analogamente, il valore massimo rappresenta l'intensità completa e il bianco si ottiene quando tutti i canali di colore sono a intensità completa. A una profondità di bit di 8, un UINT fornisce 256 valori univoci per canale di colore (da 0 a 255). Un UINT a 16 bit fornisce 65.536 valori univoci per canale di colore (da 0 a 65.535).

WiC supporta anche formati a virgola fissa e a virgola mobile. Questi formati supportano intervalli dinamici più grandi, perché l'intero intervallo numerico di ogni canale di colore è maggiore dell'intervallo visibile. Di conseguenza, i colori possono essere regolati sopra o sotto l'intervallo visibile, durante i passaggi intermedi dell'elaborazione delle immagini, senza perdita di informazioni sulle immagini.

### <a name="fixed-point-numerical-encoding"></a>Fixed-Point numerica

I valori a virgola fissa a 16 bit vengono interpretati come s2.13: bit di segno, due bit interi e 13 bit frazionari. Usando questa interpretazione, un intervallo numerico compreso tra [...]4,0 e +3,999... può essere rappresentato con il valore 1.0 rappresentato dal valore intero con segno 8192 (0x2000).

I valori a virgola fissa a 32 bit vengono interpretati come s7.24: bit di segno, sette bit interi e 24 bit frazionari. Usando questa interpretazione, un intervallo numerico compreso tra [...]128,0 e +127,999... può essere rappresentato con il valore 1.0 rappresentato dal valore intero con segno 16777216 (0x01000000).

## <a name="color-channels"></a>Canali colori

I canali di colore di un formato pixel definiscono il layout di memoria di ogni colore all'interno dei dati dell'immagine di una bitmap. Esistono un'ampia gamma di diverse strutture di canali di colori comuni nelle immagini digitali attuali e WIC fornisce il supporto per molte di queste.

### <a name="rgbbgr-color-model"></a>Modello colori RGB/BGR

I formati RGB e BGR descrivono i colori in un modello di colore additivo. Il metodo più comune per descrivere un'immagine è con tre canali di colore separati che rappresentano i colori rosso (R), verde (G) e blu (B). WIC fornisce il supporto per questi tre canali nell'ordine rosso-verde-blu (RGB) o blu-verde-rosso (BGR). Questo è l'ordine in cui ogni canale di colore viene visualizzato all'interno del flusso di bit sequenziale. Nel formato GUID \_ WICPixelFormat32bppRGB, ad esempio, ogni pixel ha una larghezza di 32 bit. Il canale rosso è il primo byte (meno significativo) in memoria, seguito dal verde e quindi dal blu. Al contrario, nel formato \_ GUID WICPixelFormat32bppBGR i canali di colore sono nell'ordine opposto. WIC supporta diversi formati RGB/BGR, inclusi speciali formati di bit di tipo pack, ad esempio \_ GUID WICPixelFormat16bppBGR555.

> [!Note]  
> I canali di colore dei formati di bit speciali con pacchetto BGR non sono in multipli di 8 come i canali di colore nei formati pixel tipici. Ciò significa che i valori del canale non sono allineati ai byte. È necessario fare attenzione durante la lettura di canali di colori bit imballati.

 

Oltre ai formati RGB e BGR, WIC fornisce anche formati di pixel RGB e BGR che supportano un canale alfa (A). Il canale alfa fornisce dati di opacità per il pixel. Per i formati con un canale alfa aggiunto, il canale alfa è in genere l'ultimo nell'ordine del canale colore. Ad esempio, nel formato pixel GUID \_ WICPixelFormat32bppBGRA, l'ordine dei byte è blu, verde e rosso, seguito dal canale alfa.

WIC supporta anche formati di pixel RGB alfa (P) pre-moltiplicati. In un tipico formato pixel RGBA, i valori dei colori rosso, verde e blu sono i valori di colore effettivi per l'immagine. Per creare un'immagine composita nel formato RGBA standard, il valore alfa dell'immagine in primo piano deve essere moltiplicato per ognuno dei canali rosso, verde e blu prima di aggiungerla al colore dell'immagine di sfondo. In un formato di pixel RGB alfa pre-moltiplicato, ogni canale di colore è già stato moltiplicato per il valore alfa. In questo modo viene fornito un metodo più efficiente di composizione delle immagini con dati del canale alfa. Per recuperare i valori di colore effettivi di ogni canale in un formato pixel PRGBA/PBGRA, la moltiplicazione del canale alfa deve essere inversa dividendo i valori di colore per il valore alfa.

### <a name="cmyk-color-model"></a>Modello colori CMYK

CMYK è un modello di colore sottrazione usato nella stampa. I colori prodotti da un modello CMYK vengono generati dalla luce che non è sorvolata, ma riflessa. CMYK è un modello a quattro canali di ciano (C), magenta (M), giallo (Y) e nero (K). Quando tutti e quattro i canali di colore hanno un valore massimo, il risultato è nero. Analogamente ai modelli di colore RGB/BGR, l'ordine dei byte all'interno del flusso di bit sequenziale è dato dal nome del formato pixel. Ad esempio, nel formato pixel GUID \_ WICPixelFormat32bppCMYK, ogni pixel è costituito da 32 bit. Il primo byte contiene il valore ciano, seguito a sua volta da magenta, giallo e nero. WIC fornisce formati pixel per CMYK a 32 e 64 bit per pixel (bpp).

Oltre al modello di colore CMYK standard, WIC fornisce anche CMYK con alfa. In questo modo le immagini CMYK possono avere dati di fusione alfa simili al modello di colore RGB/BGR. Il canale alfa si trova immediatamente dopo il nero nel flusso di bit sequenziale di una bitmap.

### <a name="n-channel-color-model"></a>Modello colori a n canali

Per una maggiore flessibilità, WIC fornisce anche formati pixel che non hanno un ordine predefinito per i canali. WIC offre formati pixel che supportano da tre a otto canali di dati di immagine continui a profondità di bit sia di 8 che di 16. A differenza dei formati pixel RGB/BGR e CMYK, i formati a n canali non specificano l'ordine dei canali, ma piuttosto il numero di canali di colore disponibili. Ad esempio, nel formato pixel GUID WICPixelFormat32bpp4Channels, ogni pixel è costituito da 32 bit con ognuno dei 4 canali che occupano \_ un singolo byte.

WIC fornisce anche formati pixel per n-channel con alfa. In questo modo le immagini a n canali possono avere dati di fusione alfa simili ai modelli di colore RGB/BGR e CMYK. Il canale alfa si trova immediatamente dopo l'ultimo canale di colore nel flusso di bit sequenziale di una bitmap.

### <a name="indexed-and-grayscale-color-models"></a>Modelli a colori indicizzati e in scala di grigi

*I formati indicizzati* usano una tabella di colori, denominata *tavolozza*. La tavolozza viene archiviata esternamente ai dati pixel oppure definita in modo implicito. Il valore di ogni pixel nell'immagine è un indice nella tavolozza. Con un formato indicizzato, il numero di bit per pixel è direttamente correlato al numero di voci nella tavolozza. Questo riduce significativamente la quantità di dati necessari per rappresentare l'immagine, ma limita anche il numero di colori disponibili per l'immagine. WIC supporta i formati indicizzati con 1, 2, 4 o 8 bpp.

Per i formati monocromatici (in scala di grigi), WIC supporta 1, 2, 4, 8, 16 e 32 bit per pixel. Per profondità in bit di 1, 8, 16 e 32, i dati dei colori vengono archiviati in un singolo canale. Per profondità in bit di 2 o 4, i pixel sono indici in una tavolozza in scala di grigi.

### <a name="ycbcr-color-model"></a>Modello a colori Y'CbCr

WIC aggiunge il supporto per il modello di colore JFIF Y'CbCr JPEG. Y'CbCr separa i colori in un componente luma (Y') e due componenti di chroma (Cb e Cr). Molti file JPEG archiviano in modo nativo i dati delle immagini usando il modello a colori Y'CbCr.

Il sistema visivo umano è meno sensibile alle modifiche nella croma rispetto a luma e i formati Y'CbCr possono sfruttare questa sensibilità ridotta riducendo la quantità di dati di chroma archiviati rispetto a luma. A tale scopo, archiviano chroma e luma in piani separati e ridimensionano ogni piano componente in una risoluzione diversa. Questa pratica è nota come sottocampionamento di chroma.

Poiché i dati di chroma e luma vengono archiviati separatamente e possono essere risoluzioni diverse, WIC definisce formati di pixel luma e chroma separati. WIC supporta dati a 8 bit per canale.

## <a name="wic-pixel-format"></a>Formato pixel WIC

I formati pixel in WIC vengono definiti usando GUID per evitare conflitti con gli IHV. WIC fornisce un nome descrittivo per fare riferimento al GUID di un formato pixel nativo. La convenzione di denominazione per i formati pixel WIC è la seguente:

**\[GUID \_ WICPixelFormat \] \[ Bits Per Pixel \] \[ Channel Order Archiviazione \] \[ Type\]**

| Componente Format         | Descrizione                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ WICPixelFormat** | Identificazione descrittiva per tutti i formati di pixel WIC. Il nome descrittivo per tutti i pixel wic inizia con questa stringa.                                                                                                                                                                                       |
| **Bit per pixel**       | Numero di bit per pixel (bpp) usati per il formato pixel.                                                                                                                                                                                                                                                |
| **Ordine dei canali**        | Modello del canale a colori e ordine di ogni canale per il formato.                                                                                                                                                                                                                                            |
| **Archiviazione digitare**         | Codifica numerica usata per il formato pixel. La codifica predefinita è un intero senza segno. Se non segue le informazioni sul modello a colori, viene implicito un intero senza segno (UINT). FixedPoint e Float vengono usati per identificare i formati pixel che usano rispettivamente la codifica a virgola fissa e a virgola mobile. |



 

> [!Note]  
> Per i formati a n canali, l'ordine dei canali non \[ \] specifica l'ordine dei colori, ma il numero di canali disponibili. Ad esempio, GUID \_ WICPixelFormat24bpp3Channels fornisce 3 canali a colori in cui "3Channels" è la voce Channel Order, ma indica solo il numero di canali e non \[ l'ordine. \]

 

Ad esempio, il nome descrittivo GUID \_ WICPixelFormat24bppRGB indica che il formato pixel usa 24 bit per pixel e il modello di colore RGB. Poiché il nome non identifica in modo esplicito un tipo di archiviazione, è implicito un intero senza segno.

WIC supporta diversi formati pixel. Le tabelle seguenti raggruppano formati di pixel simili in base alla struttura dei colori, fornendo allo stesso tempo informazioni aggiuntive, ad esempio profondità in bit, bit per pixel e codifica numerica. Ogni tabella contiene le informazioni seguenti:

-   **Nome descrittivo**. Nome descrittivo del formato pixel.
-   **Conteggio canali**. Numero di canali di colore.
-   **Bit per canale**. Numero di bit per canale (profondità in bit).
-   **Bit per pixel**. Numero di bit per pixel, inclusi i bit di riempimento.
-   **Archiviazione tipo**. Codifica numerica dei dati dell'immagine. Questo valore può essere un intero senza segno (UINT), un numero a virgola fissa (FixedPoint) o un numero a virgola mobile (Float).

> [!Note]  
> Per maggiore chiarezza, questo documento fa riferimento ai formati pixel solo in base ai relativi nomi descrittivi. Il valore esadecimale effettivo per i formati pixel è disponibile nei file wincodec.h/idl.

 

### <a name="undefined-pixel-formats"></a>Formati di pixel non definiti

L'elenco seguente mostra i formati pixel generici usati quando il formato pixel non è definito o non è importante per un'operazione di immagine.

-   GUID \_ WICPixelFormatUndefined
-   GUID \_ WICPixelFormatDontCare

### <a name="indexed-pixel-formats"></a>Formati di pixel indicizzati

Nella tabella seguente sono elencati i formati di pixel indicizzati forniti da WIC. In questi formati, il valore di ogni pixel è un indice in una tavolozza dei colori.



| Nome descrittivo                   | Conteggio canali | Bit per pixel | Tipo di archiviazione |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Formati di pixel di bit imballati

Nella tabella seguente sono elencati i formati di bit pack forniti da WIC. In questi formati, i dati del canale di colore non sono allineati a byte.



| Nome descrittivo                          | Conteggio canali | Bit per canale       | Bit per pixel | Tipo di archiviazione |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5(B)/6(G)/5(R)         | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5(B)/5(G)/5(R)/1(A)    | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10(R)/10(G)/10(B)/2(A) | 32             | UINT         |

Per i formati \_ GUID WICPixelFormat32bppBGR101010 e \_ GUID WICPixelFormat32bppRGBA101010102, il canale rosso viene archiviato nei bit meno significativi. Per i formati \_ GUID WICPixelFormat32bppR10G10B10A2 e GUID \_ WICPixelFormat32bppR10G10B10A2HDR10, il canale rosso viene definito [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)nei bit più significativi, lo stesso layout di DXGI_FORMAT_R10G10B10A2_UNORM .

Il formato \_ GUID WICPixelFormat32bppR10G10B10A2HDR10 è il formato pixel a 10 bit per HDR10 (spazio colori BT.2020 e SMPTE ST.2084 EOTF).

### <a name="grayscale-pixel-formats"></a>Formati pixel in scala di grigi

Nella tabella seguente sono elencati i formati in scala di grigi forniti da WIC. In questi formati, i dati sui colori rappresentano sfumature di grigio.



| Nome descrittivo                           | Conteggio canali | Bit per canale | Bit per pixel | Tipo di archiviazione |
|-----------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormatBlackWhite          | 1             | 1                | 1              | UINT         |
| GUID \_ WICPixelFormat2bppGray            | 1             | 2                | 2              | UINT         |
| GUID \_ WICPixelFormat4bppGray            | 1             | 4                | 4              | UINT         |
| GUID \_ WICPixelFormat8bppGray            | 1             | 8                | 8              | UINT         |
| GUID \_ WICPixelFormat16bppGray           | 1             | 16               | 16             | UINT         |
| GUID \_ WICPixelFormat16bppGrayFixedPoint | 1             | 16               | 16             | FixedPoint   |
| GUID \_ WICPixelFormat16bppGrayHalf       | 1             | 16               | 16             | Float        |
| GUID \_ WICPixelFormat32bppGrayFloat      | 1             | 32               | 32             | Float        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint | 1             | 32               | 32             | FixedPoint   |



 

### <a name="rgbbgr-pixel-formats"></a>Formati RGB/BGR Pixel

La tabella seguente elenca i formati RGB/BGR forniti da WIC. Questi formati separano i dati dei colori primari in canali rosso (R), verde (G) e blu (B). Viene fornito un canale alfa (A) aggiuntivo per le informazioni sull'opacità in alcuni formati.



| Nome descrittivo                            | Numero di canali | Bit per canale | Bit per pixel | Tipo di archiviazione |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bppRGB             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat24bppBGR             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat32bppBGR             | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppBGRA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBE\*          | 4             | 8                | 32             | Float        |
| GUID \_ WICPixelFormat32bppPRGBA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppPBGRA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat48bppRGB             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppBGR             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | 3             | 16               | 48             | Fisso        |
| GUID \_ WICPixelFormat48bppBGRFixedPoint   | 3             | 16               | 48             | Fisso        |
| GUID \_ WICPixelFormat48bppRGBHalf         | 3             | 16               | 48             | Float        |
| GUID \_ WICPixelFormat64bppRGBA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppBGRA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPRGBA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPBGRA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | 3             | 16               | 64             | Fisso        |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | 4             | 16               | 64             | Fisso        |
| GUID \_ WICPixelFormat64bppBGRAFixedPoint  | 4             | 16               | 64             | Fisso        |
| GUID \_ WICPixelFormat64bppRGBHalf         | 3             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat64bppRGBAHalf        | 4             | 16               | 64             | Float        |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | 3             | 32               | 96             | Fisso        |
| GUID \_ WICPixelFormat128bppRGBFloat       | 3             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBAFloat      | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppPRGBAFloat     | 4             | 32               | 128            | Float        |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | 3             | 32               | 128            | Fisso        |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | 4             | 32               | 128            | Fisso        |



 

> [!Note]  
> \*Il formato \_ GUID WICPixelFormat32bppRGBE codifica tre valori a virgola mobile a 16 bit in 4 byte, come indicato di seguito: tre mantissa a 8 bit senza segno per i canali R, G e B, oltre a un esponente condiviso a 8 bit. Questo formato fornisce la precisione a virgola mobile a 16 bit in una rappresentazione in pixel più piccola.

 

A partire Windows 8 e l'aggiornamento della piattaforma [per Windows 7,](/windows/desktop/direct3darticles/platform-update-for-windows-7)WIC fornisce formati aggiuntivi, illustrati nella tabella qui.



| Nome descrittivo                      | Numero di canali | Bit per canale | Bit per pixel | Tipo di archiviazione |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | FLOAT        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | FLOAT        |



 

### <a name="cmyk-pixel-formats"></a>Formati pixel CMYK

La tabella seguente elenca i formati CMYK forniti da WIC. Questi formati separano i dati dei colori primari in canali ciano (C), magenta (M), giallo (Y) e nero (K).



| Nome descrittivo                      | Numero di canali | Bit per canale | Bit per pixel | Tipo di archiviazione |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppCMYK      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppCMYK      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCMYKAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCMYKAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>Formati pixel a n canali

Nella tabella seguente sono elencati i formati a n canali forniti da WIC. Questi formati forniscono una serie di canali di colore non definiti per archiviare i dati delle immagini.



| Nome descrittivo                            | Conteggio canali | Bit per canale | Bit per pixel | Tipo di archiviazione |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bpp3Channels       | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat48bpp3Channels       | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat32bpp4Channels       | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp4Channels       | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bpp4ChannelsAlpha  | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat40bpp5Channels       | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp5Channels       | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat48bpp5ChannelsAlpha  | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat48bpp6Channels       | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp6Channels       | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat56bpp6ChannelsAlpha  | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat56bpp7Channels       | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp7Channels      | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat64bpp8Channels       | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp8Channels      | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | 9             | 8                | 72             | UINT         |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | 9             | 16               | 144            | UINT         |



 

### <a name="alpha-only-pixel-formats"></a>Formati pixel solo alfa

Nella tabella seguente sono elencati i formati solo alfa forniti da WIC. Questo formato contiene solo informazioni alfa.



| Nome descrittivo                 | Conteggio canali | Bit per canale | Bit per pixel | Tipo di archiviazione |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Formati pixel Y'CbCr

Nella tabella seguente sono elencati i formati Y'CbCr forniti da WIC. Questi formati separano i dati dei colori primari in luma (Y), differenza di chroma blu (Cb) e differenza choma rossa (Cr). Si noti che questi formati sono progettati per archiviare i dati pixel JFIF Y'CbCr JPEG.



| Nome descrittivo                 | Conteggio canali | Bit per pixel | Tipo di archiviazione |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Spazio colore

I formati pixel in se stessi non hanno uno spazio colore. In genere, lo spazio colore è un'interpretazione semantica dei valori dei pixel che dipende dal contesto della bitmap. Alcune immagini identificano un contesto di colore che definisce lo spazio colore dell'immagine. Lo spazio colore deve essere dedotto solo in assenza di un contesto di colore.

Le informazioni sul contesto del colore sono definite [**dall'interfaccia IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) per WIC. Per recuperare le informazioni sul contesto del colore per una cornice di immagine, usare il **metodo GetColorContext.**

In assenza di informazioni sullo spazio colore per un'immagine, la regola generale per l'inferenza dello spazio colore è che i formati UINT RGB e grayscale usano lo spazio colori RGB standard (sRGB), mentre i formati RGB a virgola fissa e a virgola mobile e scala di grigi usano lo spazio colori RGB esteso (scRGB). Il modello a colori CMYK usa uno spazio colore RWOP.

## <a name="native-image-formats"></a>Formati di immagini native

Ognuno dei Windows codec WIC forniti supporta un subset dei formati di pixel WIC. Per ogni codec, i formati di decodifica supportati possono essere diversi dai formati di codifica supportati.

Quando si decodifica un'immagine, se i dati vengono archiviati in modo nativo in un formato pixel non supportato dal decodificatore, verrà convertito un formato supportato. Per determinare il formato pixel di output, chiamare [**IWICBitmapFrameDecode::GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat).

Quando si codifica un'immagine, usare [**IWICBitmapFrameEncode::SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) per richiedere che il codificatore usi un formato pixel specifico. Il codificatore restituirà il formato pixel supportato più vicino, che potrebbe essere diverso da quello richiesto.

Le tabelle seguenti illustrano i formati pixel supportati da ognuno dei Windows codec WIC forniti.

### <a name="bmp-native-codec"></a>Codec nativo BMP



| Formati pixel del decodificatore                   | Formati pixel del codificatore                   |
|-----------------------------------------|-----------------------------------------|
| GUID \_ WICPixelFormat1bppIndexed         | GUID \_ WICPixelFormat1bppIndexed         |
| GUID \_ WICPixelFormat4bppIndexed         | GUID \_ WICPixelFormat4bppIndexed         |
| GUID \_ WICPixelFormat8bppIndexed         | GUID \_ WICPixelFormat8bppIndexed         |
| GUID \_ WICPixelFormat16bppBGR555         | GUID \_ WICPixelFormat16bppBGR555         |
| GUID \_ WICPixelFormat16bppBGR565         | GUID \_ WICPixelFormat16bppBGR565         |
| GUID \_ WICPixelFormat24bppBGR            | GUID \_ WICPixelFormat24bppBGR            |
| GUID \_ WICPixelFormat32bppBGR            | GUID \_ WICPixelFormat32bppBGR            |
| GUID \_ WICPixelFormat32bppBGRA\*         | GUID \_ WICPixelFormat32bppBGRA\*         |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint | GUID \_ WICPixelFormat32bppPBGRA          |
|                                         | GUID \_ WICPixelFormat64bppRGBAFixedPoint |
|                                         | GUID \_ WICPixelFormat64bppBGRAFixedPoint |



 

> [!Note]  
> IL \_ GUID WICPixelFormat32bppBGRA è supportato solo in Windows 8, l'aggiornamento della piattaforma [per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)e versioni successive.
>
> -   Per codificare in questo formato, usare **l'opzione del codificatore EnableV5Header32bppBGRA.** Il BMP verrà scritto con un'intestazione BITMAPV5HEADER.
> -   Se un file ha bitmapV5HEADER, viene decodificato come GUID \_ WICPixelFormat32bppBGRA.

 

### <a name="gif-native-codec"></a>Codec nativo GIF



| Formati di pixel del decodificatore           | Formati pixel del codificatore           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |



 

### <a name="ico-native-codec"></a>Codec ICO nativo



| Formati di pixel del decodificatore         | Formati pixel del codificatore |
|-------------------------------|-----------------------|
| GUID \_ WICPixelFormat32bppBGRA |                       |



 

### <a name="jpeg-native-codec"></a>Codec nativo JPEG



| Formati di pixel del decodificatore         | Formati pixel del codificatore         |
|-------------------------------|-------------------------------|
| GUID \_ WICPixelFormat8bppGray  | GUID \_ WICPixelFormat8bppGray  |
| GUID \_ WICPixelFormat24bppBGR  | GUID \_ WICPixelFormat24bppBGR  |
| GUID \_ WICPixelFormat32bppCMYK | GUID \_ WICPixelFormat32bppCMYK |



 

### <a name="png-native-codec"></a>Codec PNG nativo



| Formati di pixel del decodificatore           | Formati pixel del codificatore           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat2bppIndexed | GUID \_ WICPixelFormat2bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite  | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat2bppGray    | GUID \_ WICPixelFormat2bppGray    |
| GUID \_ WICPixelFormat4bppGray    | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray    | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray   | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat24bppBGR    | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat32bppBGRA   | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat48bppRGB    | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat64bppRGBA   | GUID \_ WICPixelFormat48bppBGR    |
|                                 | GUID \_ WICPixelFormat64bppRGBA   |
|                                 | GUID \_ WICPixelFormat64bppBGRA   |



 

### <a name="tiff-native-codec"></a>Codec NATIVO TIFF



| Formati di pixel del decodificatore                | Formati pixel del codificatore           |
|--------------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed      | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed      | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed      | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite       | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat4bppGray         | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray         | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray        | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat32bppGrayFloat   | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat24bppBGR         | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat32bppBGRA        | GUID \_ WICPixelFormat32bppCMYK   |
| GUID \_ WICPixelFormat32bppPBGRA       | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat48bppRGB         | GUID \_ WICPixelFormat64bppRGBA   |
| GUID \_ WICPixelFormat32bppCMYK        |                                 |
| GUID \_ WICPixelFormat40bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat64bppRGBA        |                                 |
| GUID \_ WICPixelFormat64bppPRGBA       |                                 |
| GUID \_ WICPixelFormat64bppCMYK        |                                 |
| GUID \_ WICPixelFormat80bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat96bppRGBFloat\*  |                                 |
| GUID \_ WICPixelFormat128bppRGBAFloat  |                                 |
| GUID \_ WICPixelFormat128bppPRGBAFloat |                                 |



 

> [!Note]  
> GUID \_ WICPixelFormat96bppRGBFloat è supportato solo in Windows 8, l'aggiornamento della piattaforma [per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)e versioni successive.

 

### <a name="jpeg-xr-native-codec"></a>Codec nativo JPEG-XR



| Formati di pixel del decodificatore                    | Formati pixel del codificatore                    |
|------------------------------------------|------------------------------------------|
| GUID \_ WICPixelFormatBlackWhite           | GUID \_ WICPixelFormatBlackWhite           |
| GUID \_ WICPixelFormat8bppGray             | GUID \_ WICPixelFormat8bppGray             |
| GUID \_ WICPixelFormat16bppBGR555          | GUID \_ WICPixelFormat16bppBGR555          |
| GUID \_ WICPixelFormat16bppGray            | GUID \_ WICPixelFormat16bppGray            |
| GUID \_ WICPixelFormat24bppBGR             | GUID \_ WICPixelFormat24bppBGR             |
| GUID \_ WICPixelFormat24bppRGB             | GUID \_ WICPixelFormat24bppRGB             |
| GUID \_ WICPixelFormat32bppBGR             | GUID \_ WICPixelFormat32bppBGR             |
| GUID \_ WICPixelFormat32bppBGRA            | GUID \_ WICPixelFormat32bppBGRA            |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | GUID \_ WICPixelFormat48bppRGBFixedPoint   |
| GUID \_ WICPixelFormat16bppGrayFixedPoint  | GUID \_ WICPixelFormat16bppGrayFixedPoint  |
| GUID \_ WICPixelFormat32bppBGR101010       | GUID \_ WICPixelFormat32bppBGR101010       |
| GUID \_ WICPixelFormat48bppRGB             | GUID \_ WICPixelFormat48bppRGB             |
| GUID \_ WICPixelFormat64bppRGBA            | GUID \_ WICPixelFormat64bppRGBA            |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat96bppRGBFixedPoint   |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat128bppRGBAFloat      |
| GUID \_ WICPixelFormat128bppRGBFloat       | GUID \_ WICPixelFormat128bppRGBFloat       |
| GUID \_ WICPixelFormat32bppCMYK            | GUID \_ WICPixelFormat32bppCMYK            |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | GUID \_ WICPixelFormat64bppRGBAFixedPoint  |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | GUID \_ WICPixelFormat128bppRGBAFixedPoint |
| GUID \_ WICPixelFormat64bppCMYK            | GUID \_ WICPixelFormat64bppCMYK            |
| GUID \_ WICPixelFormat24bpp3Channels       | GUID \_ WICPixelFormat24bpp3Channels       |
| GUID \_ WICPixelFormat32bpp4Channels       | GUID \_ WICPixelFormat32bpp4Channels       |
| GUID \_ WICPixelFormat40bpp5Channels       | GUID \_ WICPixelFormat40bpp5Channels       |
| GUID \_ WICPixelFormat48bpp6Channels       | GUID \_ WICPixelFormat48bpp6Channels       |
| GUID \_ WICPixelFormat56bpp7Channels       | GUID \_ WICPixelFormat56bpp7Channels       |
| GUID \_ WICPixelFormat64bpp8Channels       | GUID \_ WICPixelFormat64bpp8Channels       |
| GUID \_ WICPixelFormat48bpp3Channels       | GUID \_ WICPixelFormat48bpp3Channels       |
| GUID \_ WICPixelFormat64bpp4Channels       | GUID \_ WICPixelFormat64bpp4Channels       |
| GUID \_ WICPixelFormat80bpp5Channels       | GUID \_ WICPixelFormat80bpp5Channels       |
| GUID \_ WICPixelFormat96bpp6Channels       | GUID \_ WICPixelFormat96bpp6Channels       |
| GUID \_ WICPixelFormat112bpp7Channels      | GUID \_ WICPixelFormat112bpp7Channels      |
| GUID \_ WICPixelFormat128bpp8Channels      | GUID \_ WICPixelFormat128bpp8Channels      |
| GUID \_ WICPixelFormat40bppCMYKAlpha       | GUID \_ WICPixelFormat40bppCMYKAlpha       |
| GUID \_ WICPixelFormat80bppCMYKAlpha       | GUID \_ WICPixelFormat80bppCMYKAlpha       |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | GUID \_ WICPixelFormat32bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | GUID \_ WICPixelFormat40bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | GUID \_ WICPixelFormat48bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | GUID \_ WICPixelFormat56bpp6ChannelsAlpha  |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | GUID \_ WICPixelFormat64bpp7ChannelsAlpha  |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | GUID \_ WICPixelFormat72bpp8ChannelsAlpha  |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | GUID \_ WICPixelFormat64bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | GUID \_ WICPixelFormat80bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | GUID \_ WICPixelFormat96bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bppRGBAHalf        | GUID \_ WICPixelFormat112bpp6ChannelsAlpha |
| GUID \_ WICPixelFormat48bppRGBHalf         | GUID \_ WICPixelFormat128bpp7ChannelsAlpha |
| GUID \_ WICPixelFormat32bppRGBE            | GUID \_ WICPixelFormat144bpp8ChannelsAlpha |
| GUID \_ WICPixelFormat16bppGrayHalf        | GUID \_ WICPixelFormat64bppRGBAHalf        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint  | GUID \_ WICPixelFormat48bppRGBHalf         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | GUID \_ WICPixelFormat32bppRGBE            |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | GUID \_ WICPixelFormat16bppGrayHalf        |
| GUID \_ WICPixelFormat64bppRGBHalf         | GUID \_ WICPixelFormatBlackWhite           |



 

## <a name="dds-native-codec"></a>Codec nativo DDS



| Formati di pixel del decodificatore          | Formati pixel del codificatore          |
|--------------------------------|--------------------------------|
| GUID \_ WICPixelFormat32bppBGRA  | GUID \_ WICPixelFormat32bppBGRA  |
| GUID \_ WICPixelFormat32bppPBGRA | GUID \_ WICPixelFormat32bppPBGRA |



 

> [!Note]  
> Il codec DDS Windows supporta i file DDS codificati usando i valori DXGI \_ FORMAT seguenti:

 

-   FORMATO DXGI \_ \_ BC1 \_ UNORM
-   FORMATO DXGI \_ \_ BC2 \_ UNORM
-   FORMATO DXGI \_ \_ BC3 \_ UNORM

Vengono decodificati e codificati come GUID \_ WICPixelFormat32bppBGRA o GUID \_ WICPixelFormat32bppPBGRA. Per altre informazioni, vedere Panoramica [del formato DDS.](dds-format-overview.md)

## <a name="pixel-format-extensibility"></a>Estendibilità del formato pixel

I formati di immagine personalizzati possono usare formati pixel non forniti in modo nativo da WIC, ad esempio YCbCr (YUV) e YCCK (Y/Cb/Cr/K). WIC offre un modello di estendibilità che consente il funzionamento dei formati pixel predefiniti e dei componenti aggiuntivi all'interno della stessa pipeline di creazione dell'immagine. Per integrare questi formati pixel con la pipeline di creazione dell'immagine WIC, è necessario creare convertitori di formati pixel per convertire i formati di pixel dei componenti aggiuntivi in uno o più formati di pixel nativi. L'interfaccia principale per la compilazione di convertitori di formato [**è IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[GUID e CLSID WIC](-wic-guids-clsids.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Specifica foto HD 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 
