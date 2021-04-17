---
title: Compressione Image-Data
description: Compressione Image-Data
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- Video Compression Manager (VCM), compressione dati immagine
- VCM (Video Compression Manager), compressione dati immagine
- ICCompress (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8f59a163a9b5a74d2d2fe984417069985fa86a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398907"
---
# <a name="image-data-compression"></a>Compressione Image-Data

L'applicazione può usare una serie di funzioni e macro [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) per comprimere i dati. Le funzioni e le macro consentono di eseguire le attività seguenti:

-   Determinare il formato di compressione da usare per un formato di input specificato.
-   Preparare il compressore.
-   Comprimere i dati.
-   Fine della compressione.

L'applicazione può aumentare il controllo sul processo di compressione usando le funzioni e le macro [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) . Questo gruppo di funzioni e macro gestisce singoli frame, anziché l'intera sequenza. Ad esempio, l'applicazione può identificare i frame da comprimere come fotogrammi chiave tramite la funzione **ICCompress** .

Un commediatore riceve i dati in un formato, comprime i dati e restituisce una versione compressa dei dati usando un formato specificato. Il formato di input tipico specifica la precedenza usando la struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Il formato di output tipico specifica la precedenza compressa, usando anche la struttura **BITMAPINFO** .

> [!Note]  
> Per ridurre al minimo la riduzione di immagini e audio durante la riproduzione, evitare di comprimere un file AVI più di una volta. Combinare parti del video non compresse nel sistema di modifica e quindi comprimere il prodotto finale.

 

## <a name="compressor-and-compression-format-selection"></a>Selezione formato compressore e compressione

Se si desidera comprimere i dati e l'applicazione richiede un formato di output specifico, inviare il messaggio di [**\_ \_ query Compress Comprimi**](icm-compress-query.md) (oppure utilizzare la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) ) per eseguire una query sul compressore per determinare se supporta i formati di input e di output.

Se il formato di output non è importante per l'applicazione, è necessario trovare solo un compressore in grado di gestire il formato di input. Per determinare se un compressore è in grado di gestire il formato di input, è possibile inviare la **\_ \_ query ICM Compress**, specificando **null** per il parametro *lParam* . Questo messaggio non restituisce il formato di output per l'applicazione. L'applicazione è in grado di determinare le dimensioni del buffer necessarie per i dati che specificano il formato di compressione inviando il messaggio [**MCI \_ compress \_ get \_ Format**](icm-compress-get-format.md) (oppure usare la macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) ). È anche possibile recuperare i dati del formato inviando \_ il formato di compressione MCI \_ get \_ (o la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) ).

Se si desidera determinare il buffer più grande che il compensatore potrebbe richiedere per la compressione, inviare il messaggio [**MCI \_ compress \_ get \_ size**](icm-compress-get-size.md) (oppure utilizzare la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) ). È possibile usare il numero di byte restituiti dalla funzione [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) per allocare un buffer per le compressioni successive delle immagini.

## <a name="compressor-initialization"></a>Inizializzazione compressore

Dopo che l'applicazione ha selezionato un compressore in grado di gestire i formati di input e di output necessari, è possibile inizializzare il [**\_ comprimer \_**](icm-compress-begin.md) usando il messaggio di inizio della compressione MCI (o usare la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) ). Questo messaggio richiede l'handle del compressore e i formati di input e output.

## <a name="data-compression"></a>Compressione dei dati

Per comprimere un frame, è possibile usare la funzione [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) . L'applicazione deve usare questa funzione ripetutamente fino a quando non vengono compressi tutti i frame di una sequenza. L'applicazione deve anche tenere traccia e incrementare il numero di ogni frame compresso con **ICCompress**. Il comprimetore utilizza questo valore per verificare se i frame vengono inviati fuori sequenza durante la compressione temporale rapida (archiviando le differenze tra i frame successivi). Se l'applicazione ricomprime un frame, deve usare lo stesso numero di frame della prima compressione del frame. Se l'applicazione comprime un'immagine ancora cornice, può specificare un numero di frame pari a zero.

L'applicazione può usare il flag del **\_ fotogramma chiave ICCOMPRESS** per rendere il frame compresso [**ICCOMPRESS**](/windows/desktop/api/Vfw/nf-vfw-iccompress) un fotogramma chiave.

Quando VCM restituisce il controllo all'applicazione dopo la compressione di un frame, VCM archivia i dati compressi nelle strutture a cui fanno riferimento i parametri *lpbiOutput* e *lpData* . Se l'applicazione deve spostare i dati compressi, può individuarne le dimensioni nel membro *biSizeImage* della struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) specificata in *lpbiOutput*.

> [!Note]  
> L'applicazione deve allocare le strutture e i buffer che archiviano i dati non compressi e compressi. Se il commutatore supporta la compressione temporale, l'applicazione deve allocare anche una struttura e un buffer per conservare il formato e i dati per il frame di informazioni precedente.

 

## <a name="ending-compression"></a>Compressione finale

Dopo che l'applicazione ha compresso i dati, può usare la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) per notificare al Compressor che è stata completata. Se si vuole riavviare la compressione dopo l'uso di questa funzione, l'applicazione deve reinizializzare il compressore inviando il messaggio di [**\_ \_ inizio compressione MCI**](icm-compress-begin.md) (oppure usare la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) ).

 

 