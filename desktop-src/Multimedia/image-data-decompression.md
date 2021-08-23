---
title: Image-Data decompressione
description: Image-Data decompressione
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- gestione compressione video(VCM), decompressione dei dati di immagine
- VCM (video compression manager),decompressione dei dati di immagine
- Funzioni ICDecompressEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5006a019fd3fcf24a08f620186af8eb09d9516e103722395ed96722b48696cb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495601"
---
# <a name="image-data-decompression"></a>Image-Data decompressione

L'applicazione usa una serie [**di funzioni ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) per controllare il decompressore. Le funzioni consentono di eseguire le attività seguenti:

-   Selezionare un decompressore.
-   Preparare il decompressore.
-   Decomprimere i dati.
-   Decompressione finale.

L'applicazione gestisce la decompressione in modo analogo al modo in cui gestisce la compressione, ad eccezione del fatto che il formato di input è un formato compresso e il formato di output è un formato visualizzabile. Il formato di input per la decompressione viene in genere ottenuto dall'intestazione del flusso. Dopo aver determinato il formato di input, l'applicazione può usare le funzioni [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) o [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) per trovare un decompressore in grado di gestirlo.

Le funzioni e le macro [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) sono un superset del gruppo di funzioni [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) e offrono altre funzionalità. La funzionalità **di ICDecompressEx**, [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin), [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)e [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) sostituisce quella delle funzioni **ICDecompress**, [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin), [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)e [**ICDecompressQuery.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) Usare le funzioni e le macro **ICDecompressEx** al posto degli equivalenti **ICDecompress.**

## <a name="decompressor-and-decompression-format-selection"></a>Selezione del formato di decompressione e decompressione

Se si desidera decomprimere i dati e l'applicazione richiede un formato di output specifico, è possibile usare la funzione [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) per eseguire una query sul decompressore per determinare se supporta i formati di input e output.

Se il formato di output non è importante nell'applicazione, è necessario trovare solo un decompressore in grado di gestire il formato di input. Per determinare se un decompressore può gestire il formato di input, usare [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) e specificare **NULL** per il *parametro lpbiDst.* L'applicazione può determinare le dimensioni del buffer necessarie per i dati che specificano il formato di decompressione inviando il messaggio [**ICM \_ DECOMPRESS \_ GET \_ FORMAT**](icm-decompress-get-format.md) (o usare la macro [**ICDecompressGetFormatSize).**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) È anche possibile inviare **ICM \_ DECOMPRESS \_ GET \_ FORMAT** (o la macro [**ICDecompressGetFormat)**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) per recuperare i dati del formato. Il decompressore restituisce il formato suggerito in una [**struttura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Questo formato in genere mantiene la maggior parte delle informazioni durante la decompressione. L'applicazione deve garantire che il decompressore venga restituito correttamente prima di decomprimere le informazioni.

Poiché l'applicazione alloca la memoria necessaria per la decompressione, deve determinare la memoria massima che il decompressore può richiedere per il formato di output. Il **ICM \_ DECOMPRESS \_ GET \_ FORMAT** ottiene il numero di byte utilizzati dal decompressore per il formato predefinito.

Se l'applicazione definisce il proprio formato tramite [**ICDecompressExQuery,**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)deve anche ottenere una tavolozza per la bitmap. **ICDecompressExQuery** non fornisce definizioni della tavolozza. La maggior parte delle applicazioni usa formati standard e non è necessario ottenere una tavolozza. L'applicazione può ottenere la tavolozza inviando il [**ICM \_ DECOMPRESS \_ GET \_ PALETTE**](icm-decompress-get-palette.md) (o usare la macro [**ICDecompressGetPalette).**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette)

## <a name="decompressor-initialization"></a>Inizializzazione decompressore

Dopo che l'applicazione ha selezionato un decompressore in grado di gestire i formati di input e output di cui ha bisogno, è possibile inizializzare il decompressore usando la [**funzione ICDecompressExBegin.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) Questa funzione richiede l'handle del decompressore e i formati di input e output.

## <a name="data-decompression"></a>Decompressione dei dati

È possibile usare la [**funzione ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) per decomprimere un frame. L'applicazione deve usare questa funzione ripetutamente fino a quando non vengono decompressi tutti i frame di una sequenza.

Se il flusso video è in ritardo rispetto ad altri componenti ,ad esempio l'audio, durante la riproduzione, l'applicazione può specificare il flag **ICDECOMPRESS \_ PER LA** DECOMPRESSIONE PER velocizzare la decompressione. A tale scopo, un decompressore potrebbe estrarre solo le informazioni necessarie per decomprimere il frame successivo e non decomprimere completamente il frame corrente. Pertanto, l'applicazione non deve tentare di disegnare i dati decompressi quando usa questo flag.

Dopo che l'applicazione ha decompresso i dati, può inviare il messaggio [**ICM \_ DECOMPRESSEX \_ END**](icm-decompressex-end.md) (o usare la macro [**ICDecompressExEnd)**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) per notificare al decompressore che è stato completato. Se si vuole riavviare la decompressione dopo aver utilizzato questa funzione, l'applicazione deve reinizializzare il decompressore usando [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi VCM](vcm-services.md)
</dt> </dl>

 

 