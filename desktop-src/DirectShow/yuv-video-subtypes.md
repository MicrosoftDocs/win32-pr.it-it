---
description: 'I formati YUV sono suddivisi in categorie in base alle informazioni seguenti:'
ms.assetid: 452f017c-81ce-4be4-9962-4b9c1a9ce849
title: Sottotipi video YUV (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312a3d9d8e12953353ed0f61fff67a05bf87426b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333168"
---
# <a name="yuv-video-subtypes"></a>Sottotipi video YUV

I formati YUV sono suddivisi in categorie in base alle informazioni seguenti:

**Formati compressi rispetto ai formati planari.** In un formato compresso, i componenti Y, U e V vengono archiviati in una sola matrice. I pixel sono organizzati in gruppi di macropixels, il cui layout dipende dal formato. In un formato planare, i componenti Y, U e V vengono archiviati separatamente, come tre piani.

**Campionamento Chroma.** Una notazione denominata A:B: C Notation viene usata per descrivere la frequenza con cui vengono campionati i e V rispetto a Y:

-   4:4:4 indica nessun sottocampionando dei canali Chroma.
-   4:2:2 indica 2:1 sottocampionando orizzontali, senza sottocampionando verticali. Ogni riga di analisi contiene quattro campioni Y per ogni due campioni U o V.
-   4:2:0 indica 2:1 sottocampionando orizzontali, con 2:1 sottocampionando verticali.
-   4:1:1 indica 4:1 sottocampionando orizzontali, senza sottocampionando verticali. Ogni riga di analisi contiene quattro esempi Y per ogni esempio U o V. 4:1:1 il campionamento è meno comune di altri formati e non viene descritto in dettaglio in questo articolo.

**BITS per canale.** Le dimensioni di esempio più comuni sono 8, 10 o 16 bit per campione. Alcuni formati YUV sono pallettizzati.

**Layout di memoria.** Due tipi di formato YUV possono essere identici, ma usare ordini diversi per gli esempi di Y, V e U in memoria.

**Formati YUV consigliati**



| GUID               | Formato | campionamento | Compresso o planare | BITS per canale |
|--------------------|--------|----------|------------------|------------------|
| \_AYUV MEDIASUBTYPE | AYUV   | 4:4:4    | Compressi           | 8                |
| \_YUY2 MEDIASUBTYPE | YUY2   | 4:2:2    | Compressi           | 8                |
| \_UYVY MEDIASUBTYPE | UYVY   | 4:2:2    | Compressi           | 8                |
| \_IMC1 MEDIASUBTYPE | IMC1   | 4:2:0    | Planare           | 8                |
| \_IMC3 MEDIASUBTYPE | IMC2   | 4:2:0    | Planare           | 8                |
| \_IMC2 MEDIASUBTYPE | IMC3   | 4:2:0    | Planare           | 8                |
| \_IMC4 MEDIASUBTYPE | IMC4   | 4:2:0    | Planare           | 8                |
| \_YV12 MEDIASUBTYPE | YV12   | 4:2:0    | Planare           | 8                |
| \_NV12 MEDIASUBTYPE | NV12   | 4:2:0    | Planare           | 8                |



 

Per una descrizione di questi formati YUV per il rendering video in Windows, vedere [formati YUV a 8 bit consigliati per il rendering video](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md) .

**Altri tipi di formato YUV**



| GUID               | Formato                                                | campionamento                                                | Compresso o planare                                  | BITS per canale                             |
|--------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------------------------------------|----------------------------------------------|
| \_I420 MEDIASUBTYPE | I420                                                  | 4:2:0                                                   | Planare                                            | 8                                            |
| \_If09 MEDIASUBTYPE | Non più supportata.<br/> Indeo YVU9<br/> | Non più supportata.<br/> Vedere la sezione Osservazioni.<br/> | Non più supportata.<br/> Planare<br/> | Non più supportata.<br/> 8<br/> |
| \_IYUV MEDIASUBTYPE | IYUV                                                  | 4:2:0                                                   | Planare                                            | 8                                            |
| \_Y211 MEDIASUBTYPE | Y211                                                  | Vedere la sezione Osservazioni.                                            | Compressi                                            | 8                                            |
| \_Y411 MEDIASUBTYPE | Y411                                                  | 4:1:1                                                   | Compressi                                            | 8                                            |
| \_Y41P MEDIASUBTYPE | Y41P                                                  | 4:1:1                                                   | Compressi                                            | 8                                            |
| \_YVU9 MEDIASUBTYPE | YVU9                                                  | Vedere la sezione Osservazioni.                                            | Planare                                            | 8                                            |
| \_YVYU MEDIASUBTYPE | YVYU                                                  | 4:2:2                                                   | Compressi                                            | 8                                            |



 

-   I420 è costituito da un piano Y, seguito da un piano U, seguito da un piano V.
-   IYUV è identico a I420.
-   Y211 è un formato compresso, in cui Y viene campionato ogni 2 pixel orizzontalmente e l'utente e la V vengono campionati ogni 4 pixel orizzontalmente. Ogni macropixel è di 4 byte e contiene 4 pixel. Usa l'ordine dei byte seguente:

    `Y0 U0 Y2 V0    Y4 U4 Y6 V4    Y8 U8 Y10 V8`

-   Y41P è un formato compresso 4:1:1. Usa l'ordine dei byte seguente:

    `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`

-   YVU9 è un formato planare, in cui l'utente e la V vengono campionati ogni 4 pixel orizzontalmente e verticalmente (a volte definito come 16:1:1). Il piano V viene visualizzato prima del piano U.
-   Il formato Indeo YVU9 (MEDIASUBTYPE \_ if09) è una variante di YVU9 con ulteriori informazioni sulla cornice Delta dopo il piano U. Il codec Indeo non è più supportato in Windows.
-   YVYU è simile a UYVY con un ordine dei byte diverso: `Y0 V0 Y1 U0`

-   Il codec Indeo non è più supportato in Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Formati YUV a 8 bit consigliati per il rendering video](../medfound/recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[Sottotipi video](video-subtypes.md)
</dt> <dt>

[Utilizzo di fotogrammi video](working-with-video-frames.md)
</dt> </dl>

 

 
