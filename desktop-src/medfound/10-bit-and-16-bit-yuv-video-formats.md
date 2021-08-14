---
description: Questo argomento descrive i formati YUV a 10 e 16 bit consigliati per l'acquisizione, l'elaborazione e la visualizzazione di video nel sistema operativo Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formati video YUV a 10 e 16 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652929257c071bd735e1d6c7ec36e1767d904da7d2364ac3e30c61c81f342f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065731"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a>Formati video YUV a 10 e 16 bit

Questo argomento descrive i formati YUV a 10 e 16 bit consigliati per l'acquisizione, l'elaborazione e la visualizzazione di video nel sistema operativo Microsoft Windows.

In questo argomento sono incluse le sezioni seguenti:

-   [Overview](#overview)
-   [Codici FOURCC per YUV a 10 e 16 bit](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [Definizioni di superficie](#surface-definitions)
    -   [Formati 4:2:0](#420-formats)
    -   [Formati 4:2:2](#422-formats)
    -   [Formati 4:4:4](#444-formats)
-   [Formati YUV preferiti](#preferred-yuv-formats)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Questi formati usano una rappresentazione a virgola fissa sia per il canale luma che per i canali chroma (C'b e C'r). I valori di esempio vengono ridimensionati a 8 bit, usando un fattore di scala di 2^(n - 8), dove n è 10 o 16, in base alle sezioni 7.7-7.8 e 7.11-7.12 di SMPTE 274M. Le conversioni di precisione possono essere eseguite usando semplici turni di bit. Ad esempio, se il punto bianco di un formato a 8 bit è 235, il formato a 10 bit corrispondente ha un punto bianco a 940 (235 × 4).

Le rappresentazioni a 16 bit descritte in questo articolo usano valori **WORD** little-endian per ogni canale. I formati a 10 bit usano anche 16 bit per ogni canale, con i 6 bit più bassi impostati su zero, come illustrato nel diagramma seguente.

![Diagramma che mostra la rappresentazione a 10 bit](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

Poiché le rappresentazioni a 10 e 16 bit dello stesso formato YUV hanno lo stesso layout di memoria, è possibile eseguire il cast di una rappresentazione a 10 bit a una rappresentazione a 16 bit senza perdita di precisione. È anche possibile eseguire il cast di una rappresentazione a 16 bit verso il basso in una rappresentazione a 10 bit. I formati Y416 e Y410 sono un'eccezione a questa regola generale, tuttavia, perché non condividono lo stesso layout di memoria.

Quando l'hardware grafico legge una superficie che contiene una rappresentazione a 10 bit, deve ignorare i 6 bit di ordine inferiore di ogni canale. Se una superficie contiene dati a 16 bit validi, tuttavia, deve essere identificata come una superficie a 16 bit.

Nei formati che contengono alfa, un pixel completamente trasparente ha un valore alfa pari a zero e un pixel completamente opaco ha un valore alfa pari a (2^n) – 1, dove n è il numero di bit alfa. Si presuppone che Alpha sia un valore lineare applicato a ogni componente dopo che il componente è stato convertito nella forma lineare normalizzata.

Per le immagini nella memoria video, il driver di grafica seleziona l'allineamento della memoria della superficie. La superficie deve essere **allineata con DWORD.** In altri casi, è garantito che le singole linee all'interno di una superficie inizino da un limite a 32 bit, anche se l'allineamento può essere maggiore di 32 bit. L'origine (0,0) è sempre l'angolo superiore sinistro della superficie.

Ai fini di questa documentazione, il termine *U* equivale a *Cb* e il termine *V* è equivalente a *Cr*.

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a>Codici FOURCC per YUV a 10 e 16 bit

I codici FOURCC per i formati descritti di seguito usano la convenzione seguente:

-   Se il formato è planare, il primo carattere nel codice FOURCC è "P". Se il formato è imballato, il primo carattere è "Y".
-   Il secondo carattere nel codice FOURCC è determinato dal campionamento di chroma, come illustrato nella tabella seguente.

    

    | Campionamento di chroma | Lettera di codice FOURCC |
    |-----------------|--------------------|
    | 4:4:4           | '4'                |
    | 4:2:2           | '2'                |
    | 4:2:1           | '1'                |
    | 4:2:0           | '0'                |

    

     

-   Gli ultimi due caratteri in FOURCC indicano il numero di bit per canale, "16" per 16 bit o "10" per 10 bit.

Usando questo schema, sono stati definiti i codici FOURCC seguenti. Al momento non sono stati definiti formati 4:2:1 per YUV a 10 o 16 bit.



| FOURCC | Descrizione            |
|--------|------------------------|
| P016   | Planare, 4:2:0, 16 bit. |
| P010   | Planare, 4:2:0, 10 bit. |
| P216   | Planare, 4:2:2, 16 bit. |
| P210   | Planare, 4:2:2, 10 bit. |
| Y216   | Packed, 4:2:2, 16 bit. |
| Y210   | Packed, 4:2:2, 10 bit. |
| Y416   | Packed, 4:4:4, 16 bit  |
| Y410   | Packed, 4:4:4, 10 bit. |



 

Anche i GUID dei sottotipi sono stati definiti da questi QUATTROCC. vedere [GUID sottotipo video](video-subtype-guids.md).

## <a name="surface-definitions"></a>Definizioni di superficie

Questa sezione descrive il layout della memoria di ogni formato. Nelle descrizioni seguenti, il termine **WORD** si riferisce a un valore little-endian a 16 bit e il termine **DWORD** fa riferimento a un valore little-endian a 32 bit.

### <a name="420-formats"></a>Formati 4:2:0

Sono definiti due formati 4:2:0, con i codici FOURCC P016 e P010. Condividono lo stesso layout di memoria, ma P016 usa 16 bit per canale e P010 usa 10 bit per canale.

### <a name="p016-and-p010"></a>P016 e P010

In questi due formati, tutti gli esempi Y vengono visualizzati per primi in memoria come matrice di **WORD** s con un numero pari di righe. Lo stride della superficie può essere maggiore della larghezza del piano Y. Questa matrice è seguita immediatamente da una matrice di **WORD** s che contiene gli esempi interleaved you e V, come illustrato nel diagramma seguente.

![Diagramma che mostra il layout in pixel p016 e p010](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

Se la matrice U-V combinata viene indirizzata come matrice **di DWORD,** la parola meno significativa (LSW) contiene il valore U e la parola più significativa (MSW) contiene il valore V. Lo stride del piano U-V combinato è uguale al passo del piano Y. Il piano U-V ha metà delle linee del piano Y.

Questi due formati sono i formati di pixel planari 4:2:0 preferiti per le rappresentazioni YUV con precisione più elevata. Si prevede che siano un requisito a termine intermedio per gli acceleratori DirectX Video Acceleration (DXVA) che supportano video a 10 o 16 bit 4:2:0.

### <a name="422-formats"></a>Formati 4:2:2

Sono definiti quattro formati 4:2:2, due planari e due imballati. Hanno i codici FOURCC seguenti:

-   P216
-   P210
-   Y216
-   Y210

### <a name="p216-and-p210"></a>P216 e P210

In questi due formati planari, tutti gli esempi Y vengono visualizzati per primi in memoria come matrice di **WORD** s con un numero pari di righe. Lo stride della superficie può essere maggiore della larghezza del piano Y. Questa matrice è seguita immediatamente da una matrice di **WORD** s che contiene gli esempi interleaved you e V, come illustrato nel diagramma seguente.

![Diagramma che mostra il layout in pixel p216 e p210](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

Se la matrice U-V combinata viene indirizzata come matrice **di DWORD,** LSW contiene il valore U e MSW contiene il valore V. Lo stride del piano U-V combinato è uguale al passo del piano Y. Il piano U-V ha lo stesso numero di linee del piano Y.

Questi due formati sono i formati di pixel planari 4:2:2 preferiti per le rappresentazioni YUV con precisione più elevata. Si prevede che siano un requisito a termine intermedio per gli acceleratori DirectX Video Acceleration (DXVA) che supportano video a 10 o 16 bit 4:2:2.

### <a name="y216-and-y210"></a>Y216 e Y210

In questi due formati imballati, ogni coppia di pixel viene archiviata come matrice di **quattro WORD,** come illustrato nella figura seguente.

![diagramma che mostra il layout in pixel y216 e y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

La prima **PAROLA** nella matrice contiene il primo esempio Y nella coppia, la seconda **PAROLA** contiene l'esempio U, la terza **PAROLA** contiene il secondo esempio Y e la quarta **parola** contiene l'esempio V.

Y210 è identico a Y216, ad eccezione del fatto che ogni campione contiene solo 10 bit di dati significativi. I 6 bit meno significativi sono impostati su zero, come descritto in precedenza.

### <a name="444-formats"></a>Formati 4:4:4

Sono definiti due formati 4:4:4, con i codici FOURCC Y410 e Y416. Entrambi i formati sono di tipo pack.

### <a name="y410"></a>Y410

Questo formato è una rappresentazione a 10 bit imballata che include 2 bit di alfa. Ogni pixel viene codificato come una **singola DWORD** con il layout di memoria illustrato nel diagramma seguente.

![diagramma che mostra il layout in pixel y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

I bit 0-9 contengono l'esempio U, i bit da 10 a 19 contengono l'esempio Y, i bit da 20 a 29 contengono l'esempio V e i bit da 30 a 31 contengono il valore alfa. Per indicare che un pixel è completamente opaco, un'applicazione deve impostare i due bit alfa uguali a 0x03.

### <a name="y416"></a>Y416

Questo formato è una rappresentazione a 16 bit imballata che include 16 bit di alfa. Ogni pixel viene codificato come coppia **di DWORD,** come illustrato nella figura seguente.

![diagramma che mostra il layout in pixel y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

I bit 0-15 contengono l'esempio U, i bit 16-31 contengono l'esempio Y, i bit 32-47 contengono l'esempio V e i bit 48-63 contengono il valore alfa.

Per indicare che un pixel è completamente opaco, un'applicazione deve impostare i due bit alfa uguali a 0xFFFF. Questo formato è inteso principalmente come formato intermedio durante l'elaborazione dell'immagine per evitare l'accumulo di errori.

## <a name="preferred-yuv-formats"></a>Formati YUV preferiti

Nella tabella seguente sono elencati i formati YUV preferiti, inclusi i formati a 8 bit.



| Formato | Campionamento di chroma | Imballato o planare | Bit per canale |
|--------|-----------------|------------------|------------------|
| AYUV   | 4:4:4           | Pranzo           | 8                |
| Y410   | 4:4:4           | Pranzo           | 10               |
| Y416   | 4:4:4           | Pranzo           | 16               |
| INTELLIGENZA ARTIFICIALE44   | 4:4:4           | Pranzo           | Palettizzato       |
| YUY2   | 4:2:2           | Pranzo           | 8                |
| Y210   | 4:2:2           | Pranzo           | 10               |
| Y216   | 4:2:2           | Pranzo           | 16               |
| P210   | 4:2:2           | Planare           | 10               |
| P216   | 4:2:2           | Planare           | 16               |
| NV12   | 4:2:0           | Planare           | 8                |
| P010   | 4:2:0           | Planare           | 10               |
| P016   | 4:2:0           | Planare           | 16               |
| NV11   | 4:1:1           | Planare           | 8                |



 

È consigliabile che se un oggetto supporta una determinata profondità di bit e uno schema di campionamento chroma, deve supportare i formati YUV corrispondenti elencati in questa tabella. Gli oggetti potrebbero supportare formati aggiuntivi non elencati qui.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati YUV a 8 bit consigliati per il rendering video](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[GUID del sottotipo video](video-subtype-guids.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 



