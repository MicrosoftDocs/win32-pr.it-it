---
description: Molte applicazioni devono usare la compressione e la decompressione dei dati senza perdita di dati. L'API di compressione semplifica questa operazione esponendo gli algoritmi di compressione Windows tramite un'API pubblica.
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: Uso dell'API di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01eff163f4ea1ccf03e1cd4ac9cb16a26afeb265
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127414"
---
# <a name="using-the-compression-api"></a>Uso dell'API di compressione

Molte applicazioni devono usare la compressione e la decompressione dei dati senza perdita di dati. L'API di compressione semplifica questa operazione esponendo gli algoritmi di compressione Windows tramite un'API pubblica. Ogni algoritmo di compressione dispone di un set di proprietà che ne controlla il comportamento. L'API di compressione espone un'interfaccia che consente allo sviluppatore di impostare o eseguire query sui valori di queste proprietà. Per tutte le proprietà degli algoritmi di compressione supportati sono disponibili valori predefiniti che rappresentano i valori di queste proprietà usati comunemente. Se una proprietà è necessaria per la compressione e la decompressione, i valori predefiniti saranno identici, assicurando che i valori identici vengano usati per la compressione e la decompressione.

## <a name="selecting-the-compression-algorithm"></a>Selezione dell'algoritmo di compressione

Quando uno sviluppatore decide che un'applicazione deve comprimere o decomprimere i dati, il passaggio successivo consiste nel scegliere un algoritmo di compressione. Questo può dipendere da test per trovare la combinazione di velocità, compressione e requisiti di memoria migliori per una particolare applicazione. L'elenco seguente fornisce un confronto relativo degli algoritmi di compressione attualmente supportati dall'API di compressione. Non tutte le opzioni sono disponibili per ogni algoritmo di compressione e il confronto è approssimativo poiché le prestazioni possono dipendere dai dati di input.

XPRESS (**Comprimi \_ algoritmo \_ Xpress**)

-   Molto veloce con requisiti di risorse limitati
-   Rapporto di compressione medio
-   Velocità elevata di compressione e decompressione
-   Requisito di memoria insufficiente
-   Supporta l'opzione **Comprimi \_ informazioni a \_ \_ livello di classe** disponibile nell'enumerazione della [**\_ \_ classe Compress Information**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . Il valore predefinito è **(DWORD) 0**. Per alcuni dati, il valore **(DWORD) 1** può migliorare il rapporto di compressione con una velocità di compressione leggermente più lenta.

XPRESS con codifica Huffman (**Comprimi \_ algoritmo \_ Xpress \_ Huff**)

-   Il rapporto di compressione è superiore a **Comprimi \_ algoritmo \_ Xpress**
-   Rapporto di compressione medio
-   Velocità di compressione e decompressione da media ad elevata
-   Requisito di memoria insufficiente
-   Supporta l'opzione **Comprimi \_ informazioni a \_ \_ livello di classe** nell'enumerazione della [**\_ \_ classe Compress Information**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . Il valore predefinito è **(DWORD) 0**. Per alcuni dati, il valore **(DWORD) 1** può migliorare il rapporto di compressione con una velocità di compressione leggermente più lenta.

MSZIP (**Comprimi \_ algoritmo \_ MSZIP**)

-   USA più risorse rispetto a **Comprimi \_ algoritmo \_ Xpress \_ Huff**
-   Genera un blocco compresso simile a RFC 1951.
-   Rapporto di compressione medio-alto
-   Velocità di compressione media e velocità elevata di decompressione
-   Requisito di memoria media

LZMS (**Comprimi \_ algoritmo \_ LZMS**)

-   Algoritmo valido se le dimensioni dei dati da comprimere sono superiori a 2 MB.
-   Rapporto di compressione elevato
-   Velocità di compressione bassa e velocità elevata di decompressione
-   Requisito di memoria medio-alto
-   Supporta l'opzione **compress \_ Information \_ Class \_ Block \_ size** nell'enumerazione [**compress \_ Information \_ Class**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . È consigliabile avere una dimensione minima di 1 MB per ottenere un rapporto di compressione migliore.

## <a name="deciding-which-compression-api-mode-to-use"></a>Scelta della modalità API di compressione da usare

Quando uno sviluppatore seleziona l'algoritmo di compressione, la decisione successiva è quella delle due modalità di utilizzo dell'API di compressione, ovvero la modalità del buffer o la modalità di blocco. La modalità buffer è stata sviluppata per semplicità d'uso ed è consigliata per la maggior parte dei casi.

La modalità buffer suddivide automaticamente il buffer di input in blocchi di dimensioni appropriate per l'algoritmo di compressione selezionato. La modalità buffer formatta e archivia automaticamente le dimensioni del buffer non compresso nel buffer compresso. La dimensione del buffer compresso non viene salvata automaticamente e l'applicazione deve salvare questa operazione per la decompressione. Non includere il flag **compress \_ RAW** nel parametro *Algorithm* quando si chiama [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) e [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) per usare la modalità buffer. Per un esempio di codice di un'applicazione in modalità buffer, vedere la sezione [uso dell'API di compressione in modalità buffer](using-the-compression-api-in-buffer-mode.md) .

La modalità blocco consente allo sviluppatore di controllare le dimensioni del blocco, ma richiede un maggior numero di operazioni da parte dell'applicazione. Quando si usa la modalità blocco, l'applicazione deve suddividere i dati di input in parti opportunamente dimensionate quando si comprimono e quindi riportare insieme i componenti durante la decompressione. La modalità di blocco ha esito negativo se la dimensione del buffer di input è maggiore della dimensione interna del blocco dell'algoritmo di compressione. La dimensione del blocco interno è 32 KB per MSZIP e 1GB per gli algoritmi di compressione XPRESS. Le dimensioni del blocco interno per LZMS sono configurabili fino a 64 GB con un aumento corrispondente nell'uso della memoria. La dimensione del buffer compresso non viene salvata automaticamente e l'applicazione deve anche salvare questa operazione per la decompressione. Il valore del parametro *UncompressedBufferSize* di [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) deve essere esattamente uguale alla dimensione originale dei dati non compressi e non solo alle dimensioni del buffer di output. Ciò significa che l'applicazione deve salvare la dimensione originale esatta dei dati non compressi, nonché i dati compressi e le dimensioni compresse, quando si usa la modalità blocco. Includere il **flag compress \_ RAW** nel parametro *Algorithm* quando si chiamano sia [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) che [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) per usare la modalità di blocco. Per un esempio di codice di un'applicazione in modalità blocco, vedere la sezione [uso dell'API di compressione in modalità blocco](using-the-compression-api-in-block-mode.md) .

## <a name="custom-memory-allocation"></a>Allocazione di memoria personalizzata

Le applicazioni in modalità blocco e di buffer hanno la possibilità di specificare una routine di allocazione della memoria personalizzata quando chiamano [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) e [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor). Il parametro *AllocationRoutines* specifica la struttura delle [**\_ \_ routine di allocazione di compressione**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines) che contiene la routine di allocazione della memoria. L'applicazione può quindi impostare le dimensioni del blocco per il compressore usando [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation). Per un esempio di una semplice routine di allocazione personalizzata, vedere la sezione [utilizzo dell'API di compressione in modalità blocco](using-the-compression-api-in-block-mode.md) .

 

 



