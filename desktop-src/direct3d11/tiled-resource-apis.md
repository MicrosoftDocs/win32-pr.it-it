---
title: API di risorse affiancate
description: Le API descritte in questa sezione funzionano con le risorse affiancate e il pool di sezioni.
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0d97f5272f4f96db56e6e89b871951de035105
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395427"
---
# <a name="tiled-resource-apis"></a>API di risorse affiancate

Le API descritte in questa sezione funzionano con le risorse affiancate e il pool di sezioni.

-   [Assegnazione di riquadri da un pool di sezioni a una risorsa](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [Esecuzione di query su affiancamento e supporto delle risorse](#querying-resource-tiling-and-support)
-   [Copia di dati affiancati](#copying-tiled-data)
-   [Ridimensionamento del pool di sezioni](#resizing-tile-pool)
-   [Barriera risorse affiancate](#tiled-resource-barrier)
-   [Argomenti correlati](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>Assegnazione di riquadri da un pool di sezioni a una risorsa

Le API [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) modificano ed eseguono query sui mapping dei riquadri. Le chiamate di aggiornamento hanno effetto solo sui riquadri identificati nella chiamata e altri vengono lasciati come definito in precedenza.

Qualsiasi riquadro specificato da un pool di sezioni può essere mappato a più posizioni in una risorsa e anche a più risorse. Questo mapping include i riquadri in una risorsa che hanno un layout scelto dall'implementazione ([mipmap](mipmap-packing.md)) in cui più mipmap sono raggruppati in un unico riquadro. L'elemento catch è che se i dati vengono scritti nel riquadro tramite un mapping, ma letti tramite un mapping configurato in modo diverso, i risultati non sono definiti. Un uso accurato di questa flessibilità può comunque essere utile per un'applicazione, come la condivisione di un riquadro tra le risorse che non verranno usate simultaneamente, in cui il contenuto del riquadro viene sempre inizializzato tramite lo stesso mapping delle risorse che verrà successivamente letto da. Analogamente, viene eseguito il mapping di un riquadro per conservare i mipmap di più risorse diverse con le stesse dimensioni di superficie. i dati verranno visualizzati nello stesso modo in entrambi i mapping.

È possibile apportare modifiche alle assegnazioni di sezioni per una risorsa in qualsiasi momento in un contesto immediato o posticipato.

## <a name="querying-resource-tiling-and-support"></a>Esecuzione di query su affiancamento e supporto delle risorse

Per eseguire una query sul affiancamento delle risorse, usare [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling).

Per il supporto di altre risorse di affiancamento, usare [**ID3D11Device2:: CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1).

## <a name="copying-tiled-data"></a>Copia di dati affiancati

Tutti i metodi in Direct3D per lo spostamento dei dati funzionano con le risorse affiancate come se non fossero affiancati, ad eccezione del fatto che le Scritture in aree non mappate vengono eliminate e le letture da aree non mappate producono 0. Se un'operazione di copia comporta la scrittura più volte nella stessa posizione di memoria perché più percorsi nella risorsa di destinazione sono mappati alla stessa memoria del riquadro, le Scritture risultanti nei riquadri con mapping multiplo sono non deterministiche e non ripetibili. In altre circostanze, gli accessi avvengono in qualsiasi ordine in cui l'hardware esegue la copia.

Direct3D 11,2 introduce metodi che consentono di copiare:

-   Copia tra i riquadri in una risorsa affiancata (in granularità del riquadro 64KB) e (a/da) un buffer nella memoria di unità di elaborazione grafica (GPU) (o risorsa di staging)- [ **ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   Copia dalla memoria fornita dall'applicazione ai riquadri in una risorsa affiancata- [ **ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

Questi metodi swizzle/deswizzle in base alle esigenze e consentono a \_ una \_ Copia \_ del riquadro d3d11 senza \_ flag di sovrascrittura quando il chiamante promette che la memoria di destinazione non è presente nel lavoro GPU in corso.

I riquadri interessati dalla copia non possono includere riquadri contenenti mipmap compressi o che hanno risultati non definiti. Per trasferire i dati da e verso mipmap che l'hardware comprime in un riquadro, è necessario usare le API di copia/aggiornamento standard (non specifiche del riquadro) o [**sul ID3D11DeviceContext:: GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) per l'intera catena MIP.

**Nota in [**GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips):** l'uso di [**sul ID3D11DeviceContext:: GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) in una risorsa con riquadri con mapping parziale genera risultati che seguono semplicemente le regole per la lettura e la scrittura di **valori null** applicati a qualsiasi algoritmo che l'hardware e il driver di visualizzazione devono usare per **GenerateMips**. Quindi, non è particolarmente utile per un'applicazione preoccuparsi di questa operazione, a meno che in qualche modo le aree con mapping **null** (e il loro effetto su altri MIP durante la fase di generazione) non abbiano alcuna conseguenza sulle parti della superficie a cui l'applicazione si occupa.

La copia dei dati del riquadro da una superficie di staging o dalla memoria dell'applicazione è il modo in cui caricare i riquadri che potrebbero essere stati trasmessi dal disco, ad esempio. Una variazione quando lo streaming del disco è il caricamento di un tipo di dati compressi nella memoria GPU, quindi la decodifica della GPU. La destinazione Decode può essere una risorsa buffer nella memoria GPU, da cui [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) copia quindi nella risorsa affiancata effettiva. Questo passaggio di copia consente alla GPU di swizzle quando il modello swizzle non è noto. Swizzling non è necessario se la risorsa affiancata è una risorsa di buffer (ad esempio, in contrapposizione a una trama).

Il layout della memoria dei riquadri nel lato della risorsa del buffer non affiancato della copia è semplicemente lineare in memoria all'interno dei riquadri 64KB, che i driver hardware e display swizzle/deswizzle per riquadro in base alle esigenze durante il trasferimento da e verso una risorsa affiancata. Per le superfici con aliasing a più campioni (MSAA), i campioni di ogni pixel vengono attraversati nell'ordine di indice di esempio prima di passare al pixel successivo. Per i riquadri che sono parzialmente riempiti sul lato destro (per una superficie che ha una larghezza non un multiplo della larghezza del riquadro in pixel), il pitch/stride per spostarsi verso il basso di una riga è la dimensione massima in byte del numero di pixel che si adattano al riquadro se il riquadro era pieno. Quindi, può esserci un divario tra ogni riga di pixel in memoria. Per semplicità di specifica, mipmap inferiori a un riquadro non vengono compressi nel layout lineare. Si tratta di uno spreco di spazio di memoria, ma come indicato in precedenza per la copia in MIPS, i pacchetti hardware non sono consentiti tramite [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) o [**UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles). L'applicazione può usare solo API UpdateSubresource \* () o CopySubresource \* () generiche per copiare i piccoli MIP singolarmente, anche se nel caso di CopySubresource \* () che significa che la memoria lineare deve essere della stessa dimensione della risorsa affiancata-CopySubresource () non è in grado di \* copiare da una risorsa buffer a una Texture2D per l'istanza.

Se è stato definito un swizzle standard hardware, è possibile aggiungere i flag per indicare che i dati nel buffer devono essere interpretati in tale formato (nessun swizzle necessario per il trasferimento), anche se approcci alternativi al caricamento dei dati può essere utile anche in questo caso, ad esempio consentendo alle applicazioni di accedere direttamente alla memoria del pool di riquadri.

Le operazioni di copia possono essere eseguite in un contesto immediato o posticipato.

## <a name="resizing-tile-pool"></a>Ridimensionamento del pool di sezioni

Per ridimensionare un pool di sezioni, utilizzare [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool).

## <a name="tiled-resource-barrier"></a>Barriera risorse affiancate

Per specificare un vincolo di ordinamento per l'accesso ai dati tra più risorse affiancate, usare [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

 




