---
title: Image-Data compressione
description: Image-Data compressione
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- gestione compressione video(VCM), compressione dei dati di immagine
- VCM (gestione compressione video), compressione dei dati di immagine
- Funzione ICCompress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf638467e3685b24a65cd47492faed6660e77e5c49864a339a3874eb81e9b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038681"
---
# <a name="image-data-compression"></a>Image-Data compressione

L'applicazione può usare una serie di funzioni e macro [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) per comprimere i dati. Le funzioni e le macro consentono di eseguire le attività seguenti:

-   Determinare il formato di compressione da usare per un formato di input specificato.
-   Preparare il compressore.
-   Comprimere i dati.
-   Compressione finale.

L'applicazione può aumentare il controllo sul processo di compressione usando le macro e le funzioni [**ICCompress.**](/windows/desktop/api/Vfw/nf-vfw-iccompress) Questo gruppo di funzioni e macro gestisce singoli fotogrammi, anziché l'intera sequenza. Ad esempio, l'applicazione può identificare i fotogrammi da comprimere come fotogrammi chiave usando la **funzione ICCompress.**

Un compresso riceve i dati in un formato, comprime i dati e restituisce una versione compressa dei dati usando un formato specificato. Il formato di input tipico specifica i DIB usando la [**struttura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Il formato di output tipico specifica dib compressi, usando anche la **struttura BITMAPINFO.**

> [!Note]  
> Per ridurre al minimo la riduzione dell'immagine e dell'audio durante la riproduzione, evitare di comprimere più volte un file AVI. Combinare parti non compresse di video nel sistema di modifica e quindi comprimere il prodotto finale.

 

## <a name="compressor-and-compression-format-selection"></a>Selezione del formato di compressione e compressione

Se si desidera comprimere i dati e l'applicazione richiede un formato di output specifico, inviare il messaggio [**ICM \_ COMPRESS \_ QUERY**](icm-compress-query.md) (o usare la macro [**ICCompressQuery)**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) per eseguire una query sul compilatore per determinare se supporta i formati di input e output.

Se il formato di output non è importante per l'applicazione, è necessario trovare solo un compressore in grado di gestire il formato di input. Per determinare se un compressore è in grado di gestire il formato di input, è possibile inviare ICM **\_ COMPRESS \_ QUERY,** specificando **NULL** per il *parametro lParam.* Questo messaggio non restituisce il formato di output all'applicazione. L'applicazione può determinare le dimensioni del buffer necessarie per i dati che specificano il formato di compressione inviando il messaggio [**\_ ICM COMPRESS GET \_ \_ FORMAT**](icm-compress-get-format.md) (o usare la macro [**ICCompressGetFormatSize).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) È anche possibile recuperare i dati di formato inviando ICM \_ COMPRESS \_ GET FORMAT \_ (o la macro [**ICCompressGetFormat).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat)

Se si vuole determinare il buffer più grande che il compresso potrebbe richiedere per la compressione, inviare il messaggio [**\_ ICM COMPRESS GET \_ \_ SIZE**](icm-compress-get-size.md) (o usare la macro [**ICCompressGetSize).**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) È possibile usare il numero di byte restituiti dalla [**funzione ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) per allocare un buffer per le compressioni di immagini successive.

## <a name="compressor-initialization"></a>Inizializzazione del vettore di compressione

Dopo che l'applicazione ha selezionato un compressore in grado di gestire i formati di input e output di cui ha bisogno, è possibile inizializzare il compressore usando il messaggio [**ICM \_ COMPRESS \_ BEGIN**](icm-compress-begin.md) (o usare la macro [**ICCompressBegin).**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) Questo messaggio richiede l'handle di compressione e i formati di input e output.

## <a name="data-compression"></a>Compressione dei dati

È possibile usare la [**funzione ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) per comprimere un frame. L'applicazione deve usare questa funzione ripetutamente finché non vengono compressi tutti i fotogrammi di una sequenza. L'applicazione deve anche tenere traccia e incrementare il numero di ogni frame compresso con **ICCompress**. Il compressore usa questo valore per verificare se i fotogrammi vengono inviati in ordine durante la compressione temporale veloce (archiviando le differenze tra i fotogrammi successivi). Se l'applicazione ricomprime un frame, deve usare lo stesso numero di frame della prima compressione del frame. Se l'applicazione comprime un'immagine con fotogramma fermo, può specificare un numero di fotogramma pari a zero.

L'applicazione può usare il flag **\_ KEYFRAME ICCOMPRESS** per rendere il fotogramma compresso da [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) un fotogramma chiave.

Quando VCM restituisce il controllo all'applicazione dopo la compressione di un frame, VCM archivia i dati compressi nelle strutture a cui fanno riferimento i parametri *lpbiOutput* *e lpData.* Se l'applicazione deve spostare i dati compressi, può individuarne le dimensioni nel membro *biSizeImage* della struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) specificata in *lpbiOutput*.

> [!Note]  
> L'applicazione deve allocare le strutture e i buffer che archiviano i dati non compressi e compressi. Se il compressore supporta la compressione temporale, l'applicazione deve allocare anche una struttura e un buffer per contenere il formato e i dati per il frame di informazioni precedente.

 

## <a name="ending-compression"></a>Fine della compressione

Dopo che l'applicazione ha compresso i dati, può usare la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) per notificare al compresso che i dati sono stati completati. Se si vuole riavviare la compressione dopo aver utilizzato questa funzione, l'applicazione deve reinizializzare il compresso inviando il messaggio [**\_ ICM COMPRESS \_ BEGIN**](icm-compress-begin.md) (o usare la macro [**ICCompressBegin).**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin)

 

 