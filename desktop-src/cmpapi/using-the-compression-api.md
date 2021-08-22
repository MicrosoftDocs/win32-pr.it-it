---
description: Molte applicazioni devono usare la compressione e la decompressione dei dati senza perdita di dati. L'API di compressione semplifica questa operazione esponendo Windows di compressione tramite un'API pubblica.
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: Uso dell'API di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedc1d57ad48196290500383686b35f557c87c34099aad842b1e8ff18f00d318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551385"
---
# <a name="using-the-compression-api"></a>Uso dell'API di compressione

Molte applicazioni devono usare la compressione e la decompressione dei dati senza perdita di dati. L'API di compressione semplifica questa operazione esponendo Windows di compressione tramite un'API pubblica. Ogni algoritmo di compressione ha un set di proprietà che ne controlla il comportamento. L'API di compressione espone un'interfaccia che consente allo sviluppatore di impostare i valori di queste proprietà o di eseguire query su di essi. Tutte le proprietà per gli algoritmi di compressione supportati hanno valori predefiniti che rappresentano i valori di uso comune di queste proprietà. Se è necessaria una proprietà sia per la compressione che per la decompressione, i valori predefiniti saranno identici, assicurando che per la compressione e la decompressione siano utilizzati valori identici.

## <a name="selecting-the-compression-algorithm"></a>Selezione dell'algoritmo di compressione

Dopo che uno sviluppatore ha deciso che un'applicazione deve comprimere o decomprimere i dati, il passaggio successivo consiste nel scegliere un algoritmo di compressione. Ciò può dipendere dai test per trovare la combinazione con le migliori prestazioni di velocità, rapporto di compressione e requisito di memoria per una determinata applicazione. L'elenco seguente offre un confronto relativo degli algoritmi di compressione attualmente supportati dall'API di compressione. Non tutte le opzioni sono disponibili per ogni algoritmo di compressione e il confronto è approssimativo perché le prestazioni possono dipendere dai dati di input.

XPRESS (**COMPRESS \_ ALGORITHM \_ XPRESS**)

-   Molto veloce con requisiti di risorse bassi
-   Rapporto di compressione medio
-   Velocità di compressione e decompressione elevate
-   Requisito di memoria insufficiente
-   Supporta **l'opzione COMPRESS INFORMATION CLASS \_ \_ \_ LEVEL** disponibile nell'enumerazione [**COMPRESS INFORMATION \_ \_ CLASS.**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) Il valore predefinito è **(DWORD)0.** Per alcuni dati, il **valore (DWORD)1** può migliorare il rapporto di compressione con una velocità di compressione leggermente più lenta.

XPRESS con codifica Huffman (**COMPRESS \_ ALGORITHM \_ XPRESS \_ HUFF**)

-   Il rapporto di compressione è superiore a **COMPRESS \_ ALGORITHM \_ XPRESS**
-   Rapporto di compressione medio
-   Velocità di compressione e decompressione medio-alta
-   Requisito di memoria insufficiente
-   Supporta **l'opzione COMPRESS INFORMATION CLASS \_ \_ \_ LEVEL** nell'enumerazione [**COMPRESS INFORMATION \_ \_ CLASS.**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) Il valore predefinito è **(DWORD)0.** Per alcuni dati, il **valore (DWORD)1** può migliorare il rapporto di compressione con una velocità di compressione leggermente più lenta.

MSZIP (**\_ COMPRIMI \_ ALGORITMO MSZIP**)

-   Usa più risorse rispetto **a COMPRESS \_ ALGORITHM \_ XPRESS \_ HUFF**
-   Genera un blocco compresso simile a RFC 1951.
-   Rapporto di compressione medio-alto
-   Velocità di compressione media e velocità di decompressione elevata
-   Requisito di memoria media

LZMS (**COMPRESS \_ ALGORITHM \_ LZMS**)

-   Algoritmo valido se le dimensioni dei dati da comprimere sono oltre 2 MB.
-   Rapporto di compressione elevato
-   Bassa velocità di compressione e velocità di decompressione elevata
-   Requisito di memoria medio-alto
-   Supporta **l'opzione COMPRESS INFORMATION CLASS BLOCK \_ \_ \_ \_ SIZE** nell'enumerazione [**COMPRESS INFORMATION \_ \_ CLASS.**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) Per ottenere un rapporto di compressione migliore, è consigliabile una dimensione minima di 1 MB.

## <a name="deciding-which-compression-api-mode-to-use"></a>Scelta della modalità dell'API di compressione da usare

Dopo che uno sviluppatore ha selezionato l'algoritmo di compressione, la decisione successiva è quale delle due modalità dell'API di compressione usare: modalità buffer o modalità blocco. La modalità buffer è stata sviluppata per semplificare l'uso ed è consigliata per la maggior parte dei casi.

La modalità buffer suddivide automaticamente il buffer di input in blocchi di dimensioni appropriate per l'algoritmo di compressione selezionato. La modalità buffer formatta e archivia automaticamente le dimensioni del buffer non compresso nel buffer compresso. Le dimensioni del buffer compresso non vengono salvate automaticamente e l'applicazione deve salvarla per la decompressione. Non includere il flag **COMPRESS \_ RAW** nel parametro *Algorithm* quando si chiama [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) e [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) per usare la modalità buffer. Per un esempio di codice di un'applicazione in modalità buffer, vedere la [sezione Uso dell'API di compressione in modalità buffer.](using-the-compression-api-in-buffer-mode.md)

La modalità blocco consente allo sviluppatore di controllare le dimensioni del blocco, ma richiede più lavoro da parte dell'applicazione. Quando si usa la modalità blocco, l'applicazione deve suddividere i dati di input in parti di dimensioni appropriate durante la compressione e quindi ricomporla durante la decompressione. La modalità blocco ha esito negativo se la dimensione del buffer di input è maggiore della dimensione del blocco interno dell'algoritmo di compressione. Le dimensioni del blocco interno sono 32 KB per MSZIP e 1 GB per gli algoritmi di compressione XPRESS. Le dimensioni del blocco interno per LZMS possono essere configurate fino a 64 GB con un aumento corrispondente dell'uso della memoria. Le dimensioni del buffer compresso non vengono salvate automaticamente e l'applicazione deve anche salvarlo per la decompressione. Il valore del *parametro UncompressedBufferSize* di [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) deve essere esattamente uguale alla dimensione originale dei dati non compressi e non solo alla dimensione del buffer di output. Ciò significa che l'applicazione deve salvare le dimensioni originali esatte dei dati non compressi, nonché i dati compressi e le dimensioni compresse, quando si usa la modalità blocco. Includere il flag **COMPRESS \_ RAW** nel *parametro Algorithm* quando si chiamano [**sia CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) che [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) per usare la modalità blocco. Per un esempio di codice di un'applicazione in modalità blocco, vedere la [sezione Uso dell'API di compressione in modalità](using-the-compression-api-in-block-mode.md) blocco.

## <a name="custom-memory-allocation"></a>Allocazione di memoria personalizzata

Le applicazioni in modalità buffer e blocco hanno la possibilità di specificare una routine di allocazione di memoria personalizzata quando chiamano [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) [**e CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor). Il *parametro AllocationRoutines* specifica la struttura [**COMPRESS ALLOCATION \_ \_ ROUTINES**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines) che contiene la routine di allocazione della memoria. L'applicazione può quindi impostare le dimensioni del blocco per l'oggetto usando [**SetCompressorInformation.**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation) Vedere la [sezione Uso dell'API di compressione in modalità](using-the-compression-api-in-block-mode.md) blocco per un esempio di una semplice routine di allocazione personalizzata.

 

 



