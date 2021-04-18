---
description: In questo argomento vengono introdotti i formati pixel forniti da Windows Imaging Component (WIC).
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: Cenni preliminari sui formati pixel nativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df37481399ac8193effc5d8f93aa49050460ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314477"
---
# <a name="native-pixel-formats-overview"></a>Cenni preliminari sui formati pixel nativi

In questo argomento vengono introdotti i formati pixel forniti da Windows Imaging Component (WIC).

Un formato pixel descrive il layout di memoria di ogni pixel in una bitmap. Questo layout di memoria descrive il modo in cui i dati immagine di una bitmap vengono codificati specificando il formato numerico e l'organizzazione del canale colori. WIC supporta diversi formati numerici per più schemi di organizzazione del canale colore, offrendo un'ampia gamma di formati pixel.

-   [Profondità bit](#bit-depth)
-   [Codifica numerica](#numerical-encoding)
-   [Canali colori](#color-channels)
    -   [Modello colori RGB/BGR](#rgbbgr-color-model)
    -   [Modello colore CMYK](#cmyk-color-model)
    -   [Modello colori n-Channel](#n-channel-color-model)
    -   [Modelli di colori indicizzati e in scala di grigi](#indexed-and-grayscale-color-models)
    -   [Modello colori CbCr](#ycbcr-color-model)
-   [Formato pixel WIC](#wic-pixel-format)
    -   [Formati pixel non definiti](#undefined-pixel-formats)
    -   [Formati pixel indicizzati](#indexed-pixel-formats)
    -   [Formati pixel di bit compressi](#packed-bit-pixel-formats)
    -   [Formati pixel di scala di grigi](#grayscale-pixel-formats)
    -   [Formati pixel RGB/BGR](#rgbbgr-pixel-formats)
    -   [Formati pixel CMYK](#cmyk-pixel-formats)
    -   [Formati pixel n-Channel](#n-channel-pixel-formats)
    -   [Formati pixel solo Alpha](#alpha-only-pixel-formats)
    -   [Formati pixel CbCr](#ycbcr-pixel-formats)
-   [Spazio colore](#color-space)
-   [Formati di immagini native](#native-image-formats)
    -   [Codec nativo BMP](#bmp-native-codec)
    -   [Codec GIF nativo](#gif-native-codec)
    -   [Codec nativo ICO](#ico-native-codec)
    -   [Codec nativo JPEG](#jpeg-native-codec)
    -   [Codec nativo PNG](#png-native-codec)
    -   [Codec nativo TIFF](#tiff-native-codec)
    -   [Codec nativo JPEG-XR](#jpeg-xr-native-codec)
-   [Codec nativo DDS](#dds-native-codec)
-   [Estendibilità del formato pixel](#pixel-format-extensibility)
-   [Argomenti correlati](#related-topics)

## <a name="bit-depth"></a>Profondità bit

La *profondità del bit* è il numero di bit utilizzati per codificare ciascun canale di colore. Attualmente, la maggior parte delle immagini digitali usa una profondità di bit di 8, ovvero ogni canale di colore in un pixel è rappresentato da 8 bit, fornendo 2 valori univoci ⁸ (256) per canale. Un'immagine con una profondità di bit di 8 e tre canali di colore, ad esempio rosso, verde e blu, USA 24 bit per pixel (BPP), che fornisce 2 ² ⁴ (16.777.216) colori diversi per pixel.

Per una migliore risoluzione dei colori, è possibile usare una profondità di bit di 16 o 32. In questo modo viene fornito ogni canale di colore con 2 ¹ ⁶ (65.536) o 2 ³ ² di valori univoci, con un costo maggiore di memoria per pixel.

In alcuni formati, la profondità del bit non è un multiplo di 8. Questi formati sono denominati formati *compressi* , perché i canali dei colori in un pixel non sono allineati ai limiti di byte. Se, ad esempio, le profondità di bit di 5, tre canali di colore possono essere archiviati in 16 bit, incluso 1 bit di riempimento, per rendere allineato i pixel ai pixel. I formati compressi sono utili in caso di limitazione della memoria o della potenza di elaborazione.

## <a name="numerical-encoding"></a>Codifica numerica

Per la maggior parte delle immagini digitali odierne, vengono utilizzati byte senza segno e interi short senza segno per descrivere l'intervallo numerico di ogni canale di colore. Il valore minimo (0) rappresenta l'intensità zero in un canale a colore singolo e il nero viene eseguito quando tutti i canali dei colori sono pari a zero. Analogamente, il valore massimo rappresenta l'intensità completa e il bianco viene eseguito quando tutti i canali dei colori hanno una piena intensità. Con una profondità di bit di 8, un UINT fornisce 256 valori univoci per canale di colore (0-255). Un UINT a 16 bit fornisce 65.536 di valori univoci per canale di colore (0-65.535).

WIC supporta inoltre formati a virgola mobile e a virgola fissa. Questi formati supportano intervalli dinamici più grandi, perché l'intero intervallo numerico di ogni canale di colore è maggiore dell'intervallo visibile. Di conseguenza, i colori possono essere regolati al di sopra o al di sotto dell'intervallo visibile, durante i passaggi intermedi dell'elaborazione di immagini, senza perdita di informazioni sull'immagine.

### <a name="fixed-point-numerical-encoding"></a>Codifica Fixed-Point numerica

i valori a virgola fissa a 16 bit sono interpretati come s 2.13: bit di segno, due bit integer e tredici bit frazionari. Utilizzando questa interpretazione, un intervallo numerico compreso tra − 4,0 e + 3,999... può essere rappresentato, con il valore 1,0 rappresentato dal valore intero con segno 8192 (0x2000).

i valori a virgola fissa a 32 bit sono interpretati come 7.24: bit di segno, sette bit integer e ventiquattro bit frazionari. Utilizzando questa interpretazione, un intervallo numerico compreso tra − 128,0 e + 127,999... può essere rappresentato, con il valore 1,0 rappresentato dal valore intero con segno 16777216 (0x01000000).

## <a name="color-channels"></a>Canali colori

I canali dei colori di un formato pixel definiscono il layout di memoria di ogni colore nei dati dell'immagine di una bitmap. Nelle immagini digitali odierne sono disponibili diverse strutture di canali di colori diversi e WIC fornisce supporto per molti di questi tipi.

### <a name="rgbbgr-color-model"></a>Modello colori RGB/BGR

I formati RGB e BGR descrivono i colori in un modello a colori additivi. Il metodo più comune per descrivere un'immagine è costituito da tre canali di colore distinti che rappresentano i colori rosso (R), verde (G) e blu (B). WIC fornisce il supporto per questi tre canali nell'ordine Red-Green-Blue (RGB) o Blue-Green-Red (BGR). Si tratta dell'ordine in cui ogni canale di colore viene visualizzato all'interno del flusso di bit sequenziale. Ad esempio, nel formato GUID \_ WICPixelFormat32bppRGB ogni pixel è a 32 bit. Il canale rosso è il primo byte (meno significativo) in memoria, seguito da verde e quindi da blu. Viceversa, nel \_ formato GUID WICPixelFormat32bppBGR, i canali dei colori si trovano nell'ordine opposto. WIC supporta diversi formati RGB/BGR, inclusi formati di bit compressi speciali, ad esempio GUID \_ WICPixelFormat16bppBGR555.

> [!Note]  
> I canali dei colori dei formati di bit BGR compressi speciali non sono in multipli di 8 come i canali dei colori nei formati pixel tipici. Ciò significa che i valori del canale non sono allineati a byte. È necessario prestare attenzione durante la lettura di canali di colore di bit compressi.

 

Oltre ai formati RGB e BGR, WIC fornisce anche formati pixel RGB e BGR che supportano un canale alfa (A). Il canale alfa fornisce dati di opacità per il pixel. Per i formati con un canale alfa aggiunto, il canale alfa viene in genere visualizzato per ultimo nell'ordine del canale colore. Ad esempio, nel formato pixel GUID \_ WICPixelFormat32bppBGRA, l'ordine dei byte è blu, verde e rosso, seguito dal canale alfa.

WIC supporta inoltre formati di pixel RGB alfa pre-moltiplicati (P). In un tipico formato pixel RGBA, i valori di colore rosso, verde e blu sono i valori effettivi dei colori per l'immagine. Per creare un'immagine composita nel formato RGBA standard, il valore alfa dell'immagine in primo piano deve essere moltiplicato per ogni canale rosso, verde e blu prima di aggiungerlo al colore dell'immagine di sfondo. In un formato pixel RGB alfa pre-moltiplicato, ogni canale di colore è già stato moltiplicato per il valore alfa. Questo fornisce un metodo più efficiente per la composizione di immagini con i dati del canale alfa. Per recuperare i valori di colore true di ogni canale in un formato pixel PRGBA/PBGRA, è necessario invertire la moltiplicazione del canale alfa dividendo i valori dei colori in base al valore alfa.

### <a name="cmyk-color-model"></a>Modello colore CMYK

CMYK è un modello di colore sottrattivo utilizzato per la stampa. I colori prodotti da un modello CMYK vengono generati dalla luce che non viene assorbita, ma riflessa. CMYK è un modello a quattro canali di Cyan (C), magenta (M), giallo (Y) e nero (K). Quando tutti e quattro i canali dei colori sono al valore massimo, il risultato è nero. Analogamente ai modelli di colore RGB/BGR, l'ordine dei byte all'interno del flusso di bit sequenziale viene fornito dal nome del formato pixel. Ad esempio, nel formato pixel GUID \_ WICPixelFormat32bppCMYK ogni pixel è costituito da 32 bit. Il primo byte contiene il valore ciano, seguito a sua volta da Magenta, giallo e nero. WIC fornisce formati pixel per CMYK a 32 e 64 bit per pixel (BPP).

Oltre al modello di colore CMYK standard, WIC fornisce anche CMYK con Alpha. Questo consente alle immagini CMYK di avere dati di fusione alfa simili al modello di colore RGB/BGR. Il canale alfa si trova immediatamente dopo il nero nel flusso di bit sequenziale di una bitmap.

### <a name="n-channel-color-model"></a>Modello colori n-Channel

Per flessibilità, WIC fornisce anche formati pixel che non hanno un ordine di canale predefinito. WIC fornisce formati pixel che supportano da tre a otto canali di dati di immagini continui a profondità di bit di 8 e 16. Diversamente dai formati RGB/BGR e CMYK pixel, i formati n-Channel non specificano l'ordine del canale, bensì il numero di canali di colori disponibili. Ad esempio, nel formato pixel GUID \_ WICPixelFormat32bpp4Channels ogni pixel è costituito da 32 bit con ognuno dei 4 canali che occupano un solo byte.

WIC fornisce inoltre formati pixel per n-Channel con alfa. Ciò consente alle immagini a n canali di avere dati di fusione alfa simili ai modelli di colore RGB/BGR e CMYK. Il canale alfa si trova immediatamente dopo l'ultimo canale colori nel flusso di bit sequenziale di una bitmap.

### <a name="indexed-and-grayscale-color-models"></a>Modelli di colori indicizzati e in scala di grigi

I formati *indicizzati* utilizzano una tabella di colori, denominata *tavolozza*. La tavolozza viene archiviata esternamente nei dati pixel o altrimenti definiti in modo implicito. Il valore di ogni pixel nell'immagine è un indice nella tavolozza. Con un formato indicizzato, il numero di bit per pixel è direttamente correlato al numero di voci nella tavolozza. Questo riduce significativamente la quantità di dati necessari per rappresentare l'immagine, ma limita anche il numero di colori disponibili per l'immagine. WIC supporta formati indicizzati con 1, 2, 4 o 8 BPP.

Per i formati monocromi (scala di grigi), WIC supporta 1, 2, 4, 8, 16 e 32 bit per pixel. Per le profondità di bit di 1, 8, 16 e 32, i dati relativi ai colori vengono archiviati in un singolo canale. Per le profondità di bit di 2 o 4, i pixel sono indici in una tavolozza in scala di grigi.

### <a name="ycbcr-color-model"></a>Modello colori CbCr

WIC aggiunge il supporto per il modello di colore JFIF CbCr JPEG. CbCr separa i colori in un componente luma (Y) e due componenti Chroma (CB e CR). Molti file JPEG archiviano in modo nativo i dati dell'immagine usando il modello di colore CbCr.

Il sistema visivo umano è meno sensibile alle modifiche in Chroma rispetto a luma e i formati CbCr possono trarre vantaggio da questa sensibilità ridotta riducendo la quantità di dati Chroma archiviati rispetto a Luma. Questa operazione viene eseguita archiviando Chroma e luma in piani separati e scalando ogni piano di componente a una risoluzione diversa. Questa pratica è nota come sottocampionamento Chroma.

Poiché i dati Chroma e Luma vengono archiviati separatamente e possono essere risoluzioni diverse, WIC definisce formati di luma e cromatici separati. WIC supporta dati di 8 bit per canale.

## <a name="wic-pixel-format"></a>Formato pixel WIC

I formati pixel in WIC vengono definiti tramite GUID per evitare conflitti con IHV. WIC fornisce un nome descrittivo per fare riferimento al GUID di un formato pixel nativo. La convenzione di denominazione per i formati di pixel WIC è la seguente:

**\[\_Tipo di \] \[ \] \[ \] \[ archiviazione dell'ordine di bit WICPixelFormat GUID per pixel\]**

| Formatta componente         | Descrizione                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ WICPixelFormat** | Identificazione descrittiva per tutti i formati di pixel WIC. Il nome descrittivo per tutti i pixel WIC inizia con questa stringa.                                                                                                                                                                                       |
| **Bit per pixel**       | Numero di bit per pixel (BPP) utilizzato per il formato pixel.                                                                                                                                                                                                                                                |
| **Ordine del canale**        | Modello di canale del colore e ordine di ogni canale per il formato.                                                                                                                                                                                                                                            |
| **Tipo di archiviazione**         | Codifica numerica utilizzata per il formato pixel. La codifica predefinita è un Unsigned Integer. Se non segue le informazioni sul modello di colore, viene implicito un Unsigned Integer (UINT). FixedPoint e float vengono usati per identificare i formati pixel che usano rispettivamente la codifica a virgola mobile e a virgola mobile. |



 

> [!Note]  
> Per i formati n-Channel, \[ \] l'ordine dei canali non specifica l'ordine dei colori, bensì il numero di canali disponibili. Il GUID WICPixelFormat24bpp3Channels, ad esempio, \_ fornisce 3 canali di colore dove "3Channels" è la \[ voce dell'ordine del canale \] , ma indica solo il numero di canali e non l'ordine.

 

Il nome descrittivo GUID \_ WICPixelFormat24bppRGB indica ad esempio che il formato pixel utilizza 24 bit per pixel e il modello di colore RGB. Poiché il nome non identifica in modo esplicito un tipo di archiviazione, un Unsigned Integer è implicito.

WIC supporta diversi formati pixel. Le tabelle seguenti raggruppano formati pixel simili in base alla struttura dei colori, fornendo informazioni aggiuntive, ad esempio la profondità dei bit, i bit per pixel e la codifica numerica. Ogni tabella contiene le informazioni seguenti:

-   **Nome descrittivo**. Nome descrittivo del formato pixel.
-   **Numero di canali**. Numero di canali dei colori.
-   **Bits per canale**. Numero di bit per canale (profondità in bit).
-   **Bit per pixel**. Numero di bit per pixel, inclusi tutti i bit di riempimento.
-   **Tipo di archiviazione**. Codifica numerica dei dati dell'immagine. Questo valore può essere un Unsigned Integer (UINT), un numero a virgola fissa (FixedPoint) o un numero a virgola mobile (float).

> [!Note]  
> Per maggiore chiarezza, questo documento si riferisce ai formati pixel solo in base ai nomi descrittivi. Il valore esadecimale effettivo per i formati pixel si trova nei file wincodec. h/IDL.

 

### <a name="undefined-pixel-formats"></a>Formati pixel non definiti

L'elenco seguente mostra i formati pixel generici usati quando il formato pixel non è definito o non è importante per un'operazione di immagine.

-   GUID \_ WICPixelFormatUndefined
-   GUID \_ WICPixelFormatDontCare

### <a name="indexed-pixel-formats"></a>Formati pixel indicizzati

Nella tabella seguente sono elencati i formati di pixel indicizzati forniti da WIC. In questi formati, il valore per ogni pixel è un indice in una tavolozza dei colori.



| Nome descrittivo                   | Numero di canali | Bit per pixel | Tipo di archiviazione |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>Formati pixel di bit compressi

Nella tabella seguente sono elencati i formati di bit compressi forniti da WIC. In questi formati i dati del canale colore non sono allineati a byte.



| Nome descrittivo                          | Numero di canali | BITS per canale       | Bit per pixel | Tipo di archiviazione |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5 (B)/6 (G)/5 (R)         | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5 (B)/5 (G)/5 (R)/1 (A)    | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10 (R)/10 (G)/10 (B)/2 (A) | 32             | UINT         |

Per i \_ formati GUID WICPixelFormat32bppBGR101010 e GUID \_ WICPixelFormat32bppRGBA1010102, il canale rosso viene archiviato nei bit meno significativi. Per i \_ formati GUID WICPixelFormat32bppR10G10B10A2 e GUID \_ WICPixelFormat32bppR10G10B10A2HDR10, il canale rosso viene definito nei bit più significativi, lo stesso layout [DXGI_FORMAT_R10G10B10A2_UNORM](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

Il \_ formato GUID WICPixelFormat32bppR10G10B10A2HDR10 è il formato pixel a 10 bit per HDR10 (spazio colore BT. 2020 e SMPTE St. 2084 EOTF).

### <a name="grayscale-pixel-formats"></a>Formati pixel di scala di grigi

Nella tabella seguente sono elencati i formati di scala di grigi forniti da WIC. In questi formati, i dati relativi ai colori rappresentano le sfumature di grigio.



| Nome descrittivo                           | Numero di canali | BITS per canale | Bit per pixel | Tipo di archiviazione |
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



 

### <a name="rgbbgr-pixel-formats"></a>Formati pixel RGB/BGR

Nella tabella seguente sono elencati i formati RGB/BGR forniti da WIC. Questi formati separano i dati dei colori primari nei canali rosso (R), verde (G) e blu (B). In alcuni formati viene fornito un canale alfa (A) aggiuntivo per le informazioni di opacità.



| Nome descrittivo                            | Numero di canali | BITS per canale | Bit per pixel | Tipo di archiviazione |
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
> \*Il \_ formato GUID WICPixelFormat32bppRGBE codifica i valori a virgola mobile a 3 16 bit in 4 byte, come segue: tre mantisse senza segno a 8 bit per i canali R, G e B, più un esponente a 8 bit condiviso. Questo formato offre la precisione a virgola mobile a 16 bit in una rappresentazione in pixel più piccola.

 

A partire da Windows 8 e dall' [aggiornamento della piattaforma per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), WIC fornisce formati aggiuntivi, illustrati nella tabella qui.



| Nome descrittivo                      | Numero di canali | BITS per canale | Bit per pixel | Tipo di archiviazione |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | FLOAT        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | FLOAT        |



 

### <a name="cmyk-pixel-formats"></a>Formati pixel CMYK

Nella tabella seguente sono elencati i formati CMYK forniti da WIC. Questi formati separano i dati dei colori primari nei canali cyan (C), magenta (M), Yellow (Y) e Black (K).



| Nome descrittivo                      | Numero di canali | BITS per canale | Bit per pixel | Tipo di archiviazione |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppCMYK      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppCMYK      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCMYKAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCMYKAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>Formati pixel n-Channel

Nella tabella seguente sono elencati i formati n-Channel forniti da WIC. Questi formati forniscono una serie di canali di colori non definiti per archiviare i dati delle immagini.



| Nome descrittivo                            | Numero di canali | BITS per canale | Bit per pixel | Tipo di archiviazione |
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



 

### <a name="alpha-only-pixel-formats"></a>Formati pixel solo Alpha

Nella tabella seguente sono elencati i formati Alpha only forniti da WIC. Questo formato contiene solo informazioni Alpha.



| Nome descrittivo                 | Numero di canali | BITS per canale | Bit per pixel | Tipo di archiviazione |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Formati pixel CbCr

Nella tabella seguente sono elencati i formati CbCr forniti da WIC. Questi formati separano i dati del colore primario in luminanza (Y), la differenza di crominanza blu (CB) e la differenza del Choma rosso (CR). Si noti che questi formati sono progettati per archiviare i dati JPEG JFIF CbCr pixel.



| Nome descrittivo                 | Numero di canali | Bit per pixel | Tipo di archiviazione |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>Spazio colore

I formati pixel in sé non hanno uno spazio colore. In genere, lo spazio colore è un'interpretazione semantica dei valori pixel che dipendono dal contesto della bitmap. Alcune immagini identificano un contesto di colore che definisce lo spazio colore dell'immagine. Solo in assenza di un contesto di colore deve essere dedotto lo spazio colore.

Le informazioni sul contesto dei colori sono definite dall'interfaccia [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) per WIC. Per recuperare le informazioni sul contesto del colore per un frame immagine, usare il metodo **GetColorContext** .

In assenza di informazioni sullo spazio di colore per un'immagine, la regola generale per l'inferenza dello spazio colore è che i formati RGB e di scala di grigi di UINT utilizzano lo spazio dei colori RGB standard, mentre i formati RGB e in scala a virgola mobile e a virgola mobile utilizzano lo spazio dei colori RGB esteso. Il modello di colore CMYK usa uno spazio colore RWOP.

## <a name="native-image-formats"></a>Formati di immagini native

Ognuno dei codec WIC forniti da Windows supporta un subset dei formati pixel WIC. Per ogni codec, i formati di decodifica supportati potrebbero essere diversi dai formati di codifica supportati.

Quando si decodifica un'immagine, se i dati vengono archiviati in modo nativo in un formato pixel non supportato dal decodificatore, verranno convertiti in un formato supportato. Per determinare il formato dei pixel di output, chiamare [**IWICBitmapFrameDecode:: GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat).

Quando si codifica un'immagine, usare [**IWICBitmapFrameEncode:: SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) per richiedere che il codificatore usi un formato pixel specifico. Il codificatore restituirà il formato pixel più vicino supportato, che può essere diverso da quello richiesto.

Le tabelle seguenti illustrano i formati pixel supportati da ognuno dei codec WIC forniti da Windows.

### <a name="bmp-native-codec"></a>Codec nativo BMP



| Formati pixel decodificatore                   | Formati pixel del codificatore                   |
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
> GUID \_ WICPixelFormat32bppBGRA è supportato solo in Windows 8, l' [aggiornamento della piattaforma per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)e versioni successive.
>
> -   Per eseguire la codifica in questo formato, usare l'opzione **EnableV5Header32bppBGRA** Encoder. Il formato BMP verrà scritto con un'intestazione BITMAPV5HEADER.
> -   Se un file dispone di un BITMAPV5HEADER, decodifica come GUID \_ WICPixelFormat32bppBGRA.

 

### <a name="gif-native-codec"></a>Codec GIF nativo



| Formati pixel decodificatore           | Formati pixel del codificatore           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |



 

### <a name="ico-native-codec"></a>Codec nativo ICO



| Formati pixel decodificatore         | Formati pixel del codificatore |
|-------------------------------|-----------------------|
| GUID \_ WICPixelFormat32bppBGRA |                       |



 

### <a name="jpeg-native-codec"></a>Codec nativo JPEG



| Formati pixel decodificatore         | Formati pixel del codificatore         |
|-------------------------------|-------------------------------|
| GUID \_ WICPixelFormat8bppGray  | GUID \_ WICPixelFormat8bppGray  |
| GUID \_ WICPixelFormat24bppBGR  | GUID \_ WICPixelFormat24bppBGR  |
| GUID \_ WICPixelFormat32bppCMYK | GUID \_ WICPixelFormat32bppCMYK |



 

### <a name="png-native-codec"></a>Codec nativo PNG



| Formati pixel decodificatore           | Formati pixel del codificatore           |
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



 

### <a name="tiff-native-codec"></a>Codec nativo TIFF



| Formati pixel decodificatore                | Formati pixel del codificatore           |
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
> GUID \_ WICPixelFormat96bppRGBFloat è supportato solo in Windows 8, l' [aggiornamento della piattaforma per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)e versioni successive.

 

### <a name="jpeg-xr-native-codec"></a>Codec nativo JPEG-XR



| Formati pixel decodificatore                    | Formati pixel del codificatore                    |
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



| Formati pixel decodificatore          | Formati pixel del codificatore          |
|--------------------------------|--------------------------------|
| GUID \_ WICPixelFormat32bppBGRA  | GUID \_ WICPixelFormat32bppBGRA  |
| GUID \_ WICPixelFormat32bppPBGRA | GUID \_ WICPixelFormat32bppPBGRA |



 

> [!Note]  
> Il codec DDS fornito da Windows supporta i file DDS codificati con i valori di formato DXGI seguenti \_ :

 

-   \_Formato DXGI \_ BC1 \_ UNORM
-   \_Formato DXGI \_ BC2 \_ UNORM
-   \_Formato DXGI \_ BC3 \_ UNORM

Questi vengono decodificati e codificati come GUID \_ WICPixelFormat32bppBGRA o GUID \_ WICPixelFormat32bppPBGRA. Per ulteriori informazioni, vedere la [Panoramica del formato DDS](dds-format-overview.md).

## <a name="pixel-format-extensibility"></a>Estendibilità del formato pixel

I formati di immagine personalizzati possono usare formati pixel che non sono forniti in modo nativo da WIC, ad esempio YCbCr (YUV) e YCCK (Y/CB/CR/K). WIC fornisce un modello di estendibilità che consente il funzionamento dei formati pixel predefiniti e dei componenti aggiuntivi nella stessa pipeline di imaging. Per integrare questi formati pixel con la pipeline di imaging WIC, è necessario creare convertitori di formato pixel per convertire i formati di pixel dei componenti aggiuntivi in uno o più formati pixel nativi. L'interfaccia principale per la compilazione dei convertitori di formato è [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[GUID e CLSID WIC](-wic-guids-clsids.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Specifica foto HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 
