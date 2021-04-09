---
description: Questo argomento descrive i formati YUV a 10 e 16 bit consigliati per l'acquisizione, l'elaborazione e la visualizzazione di video nel sistema operativo Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formati video YUV a 10 bit e a 16 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129559"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a>Formati video YUV a 10 bit e a 16 bit

Questo argomento descrive i formati YUV a 10 e 16 bit consigliati per l'acquisizione, l'elaborazione e la visualizzazione di video nel sistema operativo Microsoft Windows.

In questo argomento sono incluse le sezioni seguenti:

-   [Overview](#overview)
-   [Codici FOURCC per YUV a 10 bit e a 16 bit](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [Definizioni di superficie](#surface-definitions)
    -   [formati 4:2:0](#420-formats)
    -   [formati 4:2:2](#422-formats)
    -   [formati 4:4:4](#444-formats)
-   [Formati YUV Preferiti](#preferred-yuv-formats)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Questi formati usano una rappresentazione a virgola fissa per i canali Luma Channel e Chroma (C'b e C'r). I valori di esempio vengono ridimensionati a 8 bit, usando un fattore di scala 2 ^ (n − 8), dove n è 10 o 16, come per le sezioni 7,7-7,8 e 7.11-7.12 di SMPTE 274M. Le conversioni di precisione possono essere eseguite utilizzando semplici turni di bit. Se, ad esempio, il punto bianco di un formato a 8 bit è 235, il formato a 10 bit corrispondente è costituito da un punto bianco a 940 (235 × 4).

Le rappresentazioni a 16 bit descritte di seguito usano valori di **parola** little-endian per ogni canale. I formati a 10 bit utilizzano anche 16 bit per ogni canale, con i 6 bit più bassi impostati su zero, come illustrato nella figura seguente.

![diagramma che mostra la rappresentazione a 10 bit](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

Poiché le rappresentazioni a 10 bit e a 16 bit dello stesso formato YUV hanno lo stesso layout di memoria, è possibile eseguire il cast di una rappresentazione a 10 bit a una rappresentazione a 16 senza perdita di precisione. È anche possibile eseguire il cast di una rappresentazione a 16 bit fino a una rappresentazione a 10 bit. I formati Y416 e Y410 rappresentano un'eccezione a questa regola generale, tuttavia, poiché non condividono lo stesso layout di memoria.

Quando l'hardware grafico legge una superficie che contiene una rappresentazione a 10 bit, deve ignorare i 6 bit di ordine inferiore di ogni canale. Se una superficie contiene dati a 16 bit validi, tuttavia, deve essere identificata come una superficie a 16 bit.

Nei formati che contengono Alpha, un pixel completamente trasparente ha un valore alfa pari a zero e un pixel completamente opaco ha un valore alfa pari a (2 ^ n)-1, dove n è il numero di bit alfa. Si presuppone che Alpha sia un valore lineare applicato a ogni componente dopo che il componente è stato convertito in un formato lineare normalizzato.

Per le immagini nella memoria video, il driver di grafica seleziona l'allineamento della memoria della superficie. L'area deve essere **DWORD** allineata. Ovvero le singole righe all'interno di una superficie vengono avviate a un limite di 32 bit, anche se l'allineamento può essere maggiore di 32 bit. L'origine (0, 0) è sempre l'angolo superiore sinistro della superficie.

Ai fini di questa documentazione, il termine *U* è equivalente a *CB* e il termine *V* è equivalente a *CR*.

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a>Codici FOURCC per YUV a 10 bit e a 16 bit

I codici FOURCC per i formati descritti in questa sezione usano la convenzione seguente:

-   Se il formato è planare, il primo carattere nel codice FOURCC è "P". Se il formato è compresso, il primo carattere è "Y".
-   Il secondo carattere nel codice FOURCC è determinato dal campionamento Chroma, come illustrato nella tabella seguente.

    

    | Campionamento Chroma | Lettera di codice FOURCC |
    |-----------------|--------------------|
    | 4:4:4           | 4                |
    | 4:2:2           | 2                |
    | 4:2:1           | '1'                |
    | 4:2:0           | '0'                |

    

     

-   I due caratteri finali in FOURCC indicano il numero di bit per canale, ovvero "16" per 16 bit o "10" per 10 bit.

Utilizzando questo schema, sono stati definiti i seguenti codici FOURCC. In questo momento non sono stati definiti formati 4:2:1 per YUV a 10 bit o a 16 bit.



| FOURCC | Descrizione            |
|--------|------------------------|
| P016   | Planar, 4:2:0, a 16 bit. |
| P010   | Planar, 4:2:0, a 10 bit. |
| P216   | Planar, 4:2:2, a 16 bit. |
| P210   | Planar, 4:2:2, a 10 bit. |
| Y216   | Compresso, 4:2:2, a 16 bit. |
| Y210   | Compresso, 4:2:2, a 10 bit. |
| Y416   | Compresso, 4:4:4, a 16 bit  |
| Y410   | Compresso, 4:4:4, a 10 bit. |



 

I GUID del sottotipo sono stati anche definiti da questi FourCC; vedere [GUID del sottotipo video](video-subtype-guids.md).

## <a name="surface-definitions"></a>Definizioni di superficie

In questa sezione viene descritto il layout della memoria di ogni formato. Nelle descrizioni che seguono il termine **Word** si riferisce a un valore a 16 bit Little-endian e il termine **DWORD** si riferisce a un valore little endian a 32 bit.

### <a name="420-formats"></a>formati 4:2:0

Sono definiti due formati 4:2:0, con i codici FOURCC P016 e P010. Condividono lo stesso layout di memoria, ma P016 USA 16 bit per canale e P010 USA 10 bit per canale.

### <a name="p016-and-p010"></a>P016 e P010

In questi due formati, tutti i campioni Y vengono visualizzati prima in memoria come una matrice di **Word** s con un numero pari di righe. Lo stride della superficie può essere maggiore della larghezza del piano Y. Questa matrice è seguita immediatamente da una matrice di **Word** che contiene esempi Interleaved e V, come illustrato nella figura seguente.

![diagramma che mostra il layout di P016 e P010 pixel](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

Se la matrice di U-V combinata viene considerata come una matrice di **DWORD**, la parola meno significativa (LSW) contiene il valore U e la parola più significativa (RSU) contiene il valore V. Lo stride del piano combinato U-V è uguale allo stride del piano Y. Il piano U-V ha un numero di righe pari a metà del piano Y.

Questi due formati sono i formati di pixel planari 4:2:0 preferiti per le rappresentazioni YUV con precisione più elevata. Si presuppone che si tratta di un requisito a breve termine per gli acceleratori DXVA (DirectX Video Acceleration) che supportano il video 4:2:0 a 10 bit o a 16 bit.

### <a name="422-formats"></a>formati 4:2:2

Sono definiti quattro formati 4:2:2, due planari e due compressi. Hanno i codici FOURCC seguenti:

-   P216
-   P210
-   Y216
-   Y210

### <a name="p216-and-p210"></a>P216 e P210

In questi due formati planari tutti i campioni Y vengono visualizzati prima in memoria come una matrice di **Word** s con un numero pari di righe. Lo stride della superficie può essere maggiore della larghezza del piano Y. Questa matrice è seguita immediatamente da una matrice di **Word** che contiene esempi Interleaved e V, come illustrato nella figura seguente.

![diagramma che mostra il layout di p216 e P210 pixel](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

Se l'array U-V combinato viene considerato come una matrice di **DWORD** s, LSW contiene il valore U e il RSU contiene il valore V. Lo stride del piano combinato U-V è uguale allo stride del piano Y. Il piano U-V ha lo stesso numero di righe del piano Y.

Questi due formati sono i formati di pixel planari 4:2:2 Preferiti per le rappresentazioni YUV con precisione più elevata. Si presuppone che si tratta di un requisito a breve termine per gli acceleratori DXVA (DirectX Video Acceleration) che supportano il video 4:2:2 a 10 bit o a 16 bit.

### <a name="y216-and-y210"></a>Y216 e Y210

In questi due formati compressi ogni coppia di pixel viene archiviata come matrice di quattro **Word** s, come illustrato nella figura seguente.

![diagramma che illustra il layout di y216 e Y210 pixel.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

La prima **parola** nella matrice contiene il primo campione y nella coppia, la seconda **parola** contiene l'esempio U, la terza **parola** contiene il secondo campione y e la quarta **parola** contiene l'esempio V.

Y210 è identico a y216 ad eccezione del fatto che ogni campione contiene solo 10 bit di dati significativi. I 6 bit meno significativi sono impostati su zero, come descritto in precedenza.

### <a name="444-formats"></a>formati 4:4:4

Sono definiti due formati 4:4:4, con i codici FOURCC Y410 e Y416. Entrambi i formati sono compressi.

### <a name="y410"></a>Y410

Questo formato è una rappresentazione a 10 bit compressa che include 2 bit di alfa. Ogni pixel è codificato come **valore DWORD** singolo con il layout di memoria illustrato nel diagramma seguente.

![diagramma che mostra il layout del pixel y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

BITS 0-9 contengono l'esempio U, bits 10-19 contengono l'esempio Y, BITS 20-29 contiene l'esempio V e BITS 30-31 contengono il valore alfa. Per indicare che un pixel è completamente opaco, un'applicazione deve impostare i due bit alfa uguali a 0x03.

### <a name="y416"></a>Y416

Questo formato è una rappresentazione a 16 bit compresso che include 16 bit di alfa. Ogni pixel è codificato come coppia di **DWORD**, come illustrato nella figura seguente.

![diagramma che mostra il layout del pixel Y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

BITS 0-15 contengono l'esempio U, BITS 16-31 contengono l'esempio Y, BITS 32-47 contiene l'esempio V e BITS 48-63 contengono il valore alfa.

Per indicare che un pixel è completamente opaco, un'applicazione deve impostare i due bit alfa uguali a 0xFFFF. Questo formato è destinato principalmente a un formato intermedio durante l'elaborazione di immagini per evitare l'accumulo di errori.

## <a name="preferred-yuv-formats"></a>Formati YUV Preferiti

La tabella seguente elenca i formati YUV preferiti, inclusi i formati a 8 bit.



| Formato | Campionamento Chroma | Compresso o planare | BITS per canale |
|--------|-----------------|------------------|------------------|
| AYUV   | 4:4:4           | Compressi           | 8                |
| Y410   | 4:4:4           | Compressi           | 10               |
| Y416   | 4:4:4           | Compressi           | 16               |
| AI44   | 4:4:4           | Compressi           | Pallettizzati       |
| YUY2   | 4:2:2           | Compressi           | 8                |
| Y210   | 4:2:2           | Compressi           | 10               |
| Y216   | 4:2:2           | Compressi           | 16               |
| P210   | 4:2:2           | Planare           | 10               |
| P216   | 4:2:2           | Planare           | 16               |
| NV12   | 4:2:0           | Planare           | 8                |
| P010   | 4:2:0           | Planare           | 10               |
| P016   | 4:2:0           | Planare           | 16               |
| NV11   | 4:1:1           | Planare           | 8                |



 

È consigliabile che se un oggetto supporta uno schema di campionamento di profondità di bit e Chroma, deve supportare i formati YUV corrispondenti elencati in questa tabella. Gli oggetti potrebbero supportare formati aggiuntivi non elencati qui.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati YUV a 8 bit consigliati per il rendering video](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[GUID del sottotipo video](video-subtype-guids.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 



