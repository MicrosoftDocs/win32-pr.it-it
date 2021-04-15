---
title: Decompressione Image-Data
description: Decompressione Image-Data
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- Gestione compressione video (VCM), decompressione immagini-dati
- VCM (Gestione compressione video), decompressione immagini-dati
- Funzioni ICDecompressEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25614f157436056f7f24c340f6cc6f4dbc62d9ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337119"
---
# <a name="image-data-decompression"></a>Decompressione Image-Data

L'applicazione usa una serie di funzioni [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) per controllare il decompressore. Le funzioni consentono di eseguire le attività seguenti:

-   Selezionare un decompressore.
-   Preparare il decompressore.
-   Decomprimere i dati.
-   Decompressione finale.

L'applicazione gestisce la decompressione in modo analogo al modo in cui gestisce la compressione, con la differenza che il formato di input è un formato compresso e il formato di output è visualizzabile. Il formato di input per la decompressione viene in genere ottenuto dall'intestazione del flusso. Dopo aver determinato il formato di input, l'applicazione può usare le funzioni [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) o [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) per trovare un decompressore in grado di gestirlo.

Le funzioni e le macro [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) sono un superset del gruppo di funzioni [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress) e forniscono altre funzionalità. La funzionalità di **ICDecompressEx**, [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin), [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)e [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) sostituisce quella delle funzioni **ICDecompress**, [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin), [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)e [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) . Usare le funzioni e le macro **ICDecompressEx** al posto degli equivalenti di **ICDecompress** .

## <a name="decompressor-and-decompression-format-selection"></a>Selezione del formato decompressore e decompressione

Se si desidera decomprimere i dati e l'applicazione richiede un formato di output specifico, è possibile utilizzare la funzione [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) per eseguire una query sul decompressore per determinare se supporta i formati di input e di output.

Se il formato di output non è importante nell'applicazione, è necessario trovare solo un decompressore in grado di gestire il formato di input. Per determinare se un decompressore è in grado di gestire il formato di input, utilizzare [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) e specificare **null** per il parametro *lpbiDst* . L'applicazione è in grado di determinare le dimensioni del buffer necessarie per i dati che specificano il formato di decompressione inviando il messaggio [**MCI \_ Decompress \_ get \_ Format**](icm-decompress-get-format.md) (oppure usare la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) ). Per recuperare i dati di formato, è anche possibile inviare il **\_ \_ \_ formato di Decomprimi di ICM** (o la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) ). Il decompressore restituisce il formato suggerito in una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Questo formato in genere conserva la maggior parte delle informazioni durante la decompressione. L'applicazione deve verificare che il decompressore venga restituito correttamente prima di decomprimere le informazioni.

Poiché l'applicazione alloca la memoria necessaria per la decompressione, deve determinare la quantità massima di memoria che può essere richiesta dal decompressore per il formato di output. Il messaggio **MCI \_ Decompress \_ get \_ Format** ottiene il numero di byte utilizzati dal decompressore per il formato predefinito.

Se l'applicazione definisce il proprio formato usando [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery), è necessario ottenere anche una tavolozza per la bitmap. **ICDecompressExQuery** non fornisce le definizioni della tavolozza. (La maggior parte delle applicazioni usa formati standard e non è necessario ottenere una tavolozza). L'applicazione può ottenere la tavolozza inviando il messaggio [**MCI \_ Decompress \_ get \_ palette**](icm-decompress-get-palette.md) (oppure usare la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) ).

## <a name="decompressor-initialization"></a>Inizializzazione del decompressore

Quando l'applicazione seleziona un decompressore in grado di gestire i formati di input e di output necessari, è possibile inizializzare il decompressore usando la funzione [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) . Questa funzione richiede l'handle di decompressione e i formati di input e output.

## <a name="data-decompression"></a>Decompressione dei dati

Per decomprimere un frame, è possibile usare la funzione [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) . L'applicazione deve usare questa funzione ripetutamente fino a quando non vengono decompressi tutti i frame di una sequenza.

Se il flusso video è in ritardo rispetto ad altri componenti, ad esempio audio, durante la riproduzione, l'applicazione può specificare il flag **ICDECOMPRESS \_ sbrigati** per velocizzare la decompressione. A tale scopo, un decompressore potrebbe estrarre solo le informazioni necessarie per decomprimere il frame successivo e non decomprimere completamente il frame corrente. Pertanto, l'applicazione non deve tentare di creare i dati decompressi quando utilizza questo flag.

Dopo che l'applicazione ha decompresso i dati, può inviare il messaggio di [**\_ \_ fine DECOMPRESSEX ICM**](icm-decompressex-end.md) (oppure usare la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) ) per notificare al decompressore che è terminato. Se si vuole riavviare la decompressione dopo l'uso di questa funzione, l'applicazione deve reinizializzare il decompressore usando [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi VCM](vcm-services.md)
</dt> </dl>

 

 