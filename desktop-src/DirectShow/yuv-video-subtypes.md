---
description: 'I formati YUV sono classificati in base alle informazioni seguenti:'
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: Sottotipi di video YUV (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d31afa11c855b865c7e524d393d1f86ae836e00119a3171b35a3c0c2549d184b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632691"
---
# <a name="yuv-video-subtypes"></a>Sottotipi di video YUV

I formati YUV sono classificati in base alle informazioni seguenti:

**Formati di tipo pack e formati planari.** In un formato di tipo pack, i componenti Y, U e V vengono archiviati in un'unica matrice. I pixel sono organizzati in gruppi di macropixel, il cui layout dipende dal formato. In un formato planare, i componenti Y, U e V vengono archiviati separatamente, come tre piani.

**Campionamento di chroma.** Una notazione denominata notazione A:B:C viene usata per descrivere la frequenza con cui si e V vengono campionati rispetto a Y:

-   4:4:4 indica l'assenza di sottocampionamento dei canali chroma.
-   4:2:2 significa sottocampionamento orizzontale 2:1, senza sottocampionamento verticale. Ogni linea di analisi contiene quattro campioni Y per ogni due campioni U o V.
-   4:2:0 significa sottocampionamento orizzontale 2:1, con sottocampionamento verticale 2:1.
-   4:1:1 significa sottocampionamento orizzontale 4:1, senza sottocampionamento verticale. Ogni linea di analisi contiene quattro campioni Y per ogni campione U o V. Il campionamento 4:1:1 è meno comune rispetto ad altri formati e non viene illustrato in dettaglio in questo articolo.

**Bit per canale.** Le dimensioni di esempio più comuni sono 8, 10 o 16 bit per campione. Alcuni formati YUV sono saturati.

**Layout di memoria.** Due tipi di formato YUV possono essere altrimenti identici, ma usano ordinamenti diversi per gli esempi Y, V e U in memoria.

**Formati YUV consigliati**



| GUID               | Formato | campionamento | Imballato o planare | Bit per canale |
|--------------------|--------|----------|------------------|------------------|
| MEDIASUBTYPE \_ AYUV | AYUV   | 4:4:4    | Pranzo           | 8                |
| MEDIASUBTYPE \_ YUY2 | YUY2   | 4:2:2    | Pranzo           | 8                |
| MEDIASUBTYPE \_ UYVY | UYVY   | 4:2:2    | Pranzo           | 8                |
| MEDIASUBTYPE \_ IMC1 | IMC1   | 4:2:0    | Planare           | 8                |
| MEDIASUBTYPE \_ IMC3 | IMC2   | 4:2:0    | Planare           | 8                |
| MEDIASUBTYPE \_ IMC2 | IMC3   | 4:2:0    | Planare           | 8                |
| MEDIASUBTYPE \_ IMC4 | IMC4   | 4:2:0    | Planare           | 8                |
| MEDIASUBTYPE \_ YV12 | YV12   | 4:2:0    | Planare           | 8                |
| MEDIASUBTYPE \_ NV12 | NV12   | 4:2:0    | Planare           | 8                |



 

Per una descrizione di questi formati YUV per il rendering video in Windows, vedere Formati YUV a [8 bit consigliati per il rendering video.](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)

**Altri tipi di formato YUV**



| GUID               | Formato                                                | campionamento                                                | Imballato o planare                                  | Bit per canale                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| MEDIASUBTYPE \_ I420 | I420                                                  | 4:2:0                                                   | Planare                                            | 8                                            |
| MEDIASUBTYPE \_ IF09 | Non più supportata.<br/> Indeo YVU9<br/> | Non più supportata.<br/> Vedere la sezione Osservazioni.<br/> | Non più supportata.<br/> Planare<br/> | Non più supportata.<br/> 8<br/> |
| MEDIASUBTYPE \_ IYUV | IYUV                                                  | 4:2:0                                                   | Planare                                            | 8                                            |
| MEDIASUBTYPE \_ Y211 | Y211                                                  | Vedere la sezione Osservazioni.                                            | Pranzo                                            | 8                                            |
| MEDIASUBTYPE \_ Y411 | Y411                                                  | 4:1:1                                                   | Pranzo                                            | 8                                            |
| MEDIASUBTYPE \_ Y41P | Y41P                                                  | 4:1:1                                                   | Pranzo                                            | 8                                            |
| MEDIASUBTYPE \_ YVU9 | YVU9                                                  | Vedere la sezione Osservazioni.                                            | Planare                                            | 8                                            |
| MEDIASUBTYPE \_ YVYU | YVYU                                                  | 4:2:2                                                   | Pranzo                                            | 8                                            |



 

-   I420 è costituito da un piano Y, seguito da un piano U, seguito da un piano V.
-   IYUV è identico a I420.
-   Y211 è un formato di tipo packed, in cui Y viene campionato orizzontalmente ogni 2 pixel e l'utente e V vengono campionati ogni 4 pixel in orizzontale. Ogni macropixel è di 4 byte e contiene 4 pixel. Usa l'ordine dei byte seguente:

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Y41P è un formato pack 4:1:1. Usa l'ordine dei byte seguente:

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YVU9 è un formato planare, in cui l'utente e V vengono campionati ogni 4 pixel orizzontalmente e verticalmente (a volte indicato come 16:1:1). Il piano V viene visualizzato prima del piano U.
-   Il formato Indeo YVU9 (MEDIASUBTYPE IF09) è una variante di YVU9 con informazioni \_ aggiuntive sui fotogrammi differenziali dopo il piano U. Il codec Indeo non è più supportato in Windows.
-   YVYU è simile a UYVY con un ordine di byte diverso: `Y0 V0 Y1 U0`

-   Il codec Indeo non è più supportato in Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Formati YUV a 8 bit consigliati per il rendering video](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Sottotipi video](video-subtypes.md)
</dt> <dt>

[Uso dei fotogrammi video](working-with-video-frames.md)
</dt> </dl>

 

 
