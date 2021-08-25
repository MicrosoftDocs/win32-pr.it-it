---
title: API delle risorse affiancate
description: Le API descritte in questa sezione funzionano con le risorse affiancate e il pool di riquadri.
ms.assetid: 02DCF9BA-F9EA-4176-AD6F-AA620CE968BA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f433b6c70d475d4da511b85fdcc2b1c273de1efa8e1186215b25ce6b9b95d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894391"
---
# <a name="tiled-resource-apis"></a>API delle risorse affiancate

Le API descritte in questa sezione funzionano con le risorse affiancate e il pool di riquadri.

-   [Assegnazione di riquadri da un pool di riquadri a una risorsa](#assigning-tiles-from-a-tile-pool-to-a-resource)
-   [Esecuzione di query sul supporto e sulla affiancamento delle risorse](#querying-resource-tiling-and-support)
-   [Copia di dati affiancati](#copying-tiled-data)
-   [Ridimensionamento del pool di riquadri](#resizing-tile-pool)
-   [Barriera delle risorse affiancate](#tiled-resource-barrier)
-   [Argomenti correlati](#related-topics)

## <a name="assigning-tiles-from-a-tile-pool-to-a-resource"></a>Assegnazione di riquadri da un pool di riquadri a una risorsa

Le [**API ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) modificano ed e interrogano i mapping dei riquadri. Le chiamate di aggiornamento influiscono solo sui riquadri identificati nella chiamata e altre vengono lasciati come definito in precedenza.

Qualsiasi riquadro specificato da un pool di riquadri può essere mappato a più posizioni in una risorsa e anche a più risorse. Questo mapping include i riquadri in una risorsa che hanno un layout scelto dall'implementazione (creazione di un pacchetto[Mipmap)](mipmap-packing.md)in cui più mipmap vengono riunite in un unico riquadro. Il problema è che se i dati vengono scritti nel riquadro tramite un mapping, ma letti tramite un mapping configurato in modo diverso, i risultati non sono definiti. Un uso attento di questa flessibilità può comunque essere utile per un'applicazione, ad esempio la condivisione di un riquadro tra risorse che non verranno usate contemporaneamente, in cui il contenuto del riquadro viene sempre inizializzato tramite lo stesso mapping delle risorse da cui verranno successivamente lette. Analogamente, un riquadro mappato per contenere le mipmap di più risorse diverse con le stesse dimensioni di superficie funzionerà correttamente: i dati verranno visualizzati nello stesso modo in entrambi i mapping.

Le modifiche alle assegnazioni di riquadri per una risorsa possono essere apportate in qualsiasi momento in un contesto immediato o posticipato.

## <a name="querying-resource-tiling-and-support"></a>Esecuzione di query sul supporto e sulla affiancamento delle risorse

Per eseguire query sulla affiancamento delle risorse, [**usare ID3D11Device2::GetResourceTiling.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)

Per altre risorse supportate, usare [**ID3D11Device2::CheckMultisampleQualityLevels1**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1).

## <a name="copying-tiled-data"></a>Copia di dati affiancati

Tutti i metodi in Direct3D per lo spostamento dei dati funzionano con le risorse affiancate come se non fossero affiancate, ad eccezione del fatto che le scritture nelle aree non mappate vengono eliminate e le operazioni di lettura da aree non mappate producono 0. Se un'operazione di copia comporta la scrittura più volte nella stessa posizione di memoria perché viene eseguito il mapping di più posizioni nella risorsa di destinazione alla stessa memoria del riquadro, le scritture risultanti in riquadri con più mappe sono non deterministiche e non ripetibili. In altri casi, gli accessi vengono eseguiti nell'ordine in cui l'hardware esegue la copia.

Direct3D 11.2 introduce metodi per questi metodi aggiuntivi per la copia:

-   Copiare tra riquadri in una risorsa affiancata (con granularità del riquadro di 64 KB) e (da/verso) un buffer nella memoria dell'unità di elaborazione grafica (o risorsa di staging) - [ **ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   Copiare dalla memoria fornita dall'applicazione ai riquadri in una risorsa affiancata - [ **ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)

Questi metodi swizzle/deswizzle in base alle esigenze e consentono un flag D3D11 TILE COPY NO OVERWRITE quando il chiamante promise che alla memoria di destinazione non viene fatto riferimento dalle operazioni \_ \_ \_ \_ GPU in esecuzione.

I riquadri coinvolti nella copia non possono includere riquadri contenenti mipmap di tipo packed o con risultati non definiti. Per trasferire i dati da e verso mipmap che l'hardware contiene in un unico riquadro, è necessario usare le API di copia/aggiornamento standard (non specifiche del riquadro) o [**ID3D11DeviceContext::GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) per l'intera catena mip.

**Nota su [**GenerateMips:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips)** l'uso di [**ID3D11DeviceContext::GenerateMips**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-generatemips) in una risorsa con riquadri parzialmente mappati produrrà risultati che seguono semplicemente le regole per la lettura e la scrittura **di VALORI NULL** applicati a qualsiasi algoritmo che l'hardware e il driver di visualizzazione usano per **GenerateMips.** Pertanto, non è particolarmente utile per un'applicazione eseguire questa operazione, a meno che in qualche modo le aree con mapping **NULL** (e il relativo effetto su altri mip durante la fase di generazione) non avranno alcuna conseguenza sulle parti della superficie di cui l'applicazione si occupa.

La copia dei dati dei riquadri da una superficie di gestione temporanea o dalla memoria dell'applicazione sarebbe il modo per caricare i riquadri che potrebbero essere stati trasmessi dal disco, ad esempio. Una variazione durante lo streaming dal disco è il caricamento di alcuni dati compressi nella memoria GPU e quindi la decodifica nella GPU. La destinazione di decodifica potrebbe essere una risorsa buffer nella memoria GPU, da cui [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) copia quindi nella risorsa affiancata effettiva. Questo passaggio di copia consente alla GPU di eseguire lo swizzle quando il modello di swizzle non è noto. Lo swizzling non è necessario se la risorsa affiancata stessa è una risorsa buffer( ad esempio, anziché una trama).

Il layout della memoria dei riquadri nel lato della risorsa buffer non affiancato della copia è semplicemente lineare in memoria all'interno di riquadri da 64 KB, che il driver hardware e di visualizzazione esegue lo swizzle/deswizzle per riquadro in base alle esigenze durante il trasferimento da e verso una risorsa affiancata. Per le superfici di anti-aliasing multicampionamento (MSAA), i campioni di ogni pixel vengono attraversati in ordine di indice del campione prima di passare al pixel successivo. Per i riquadri parzialmente riempiti sul lato destro (per una superficie con una larghezza non multipla di larghezza in pixel), l'altezza/stride per spostarsi verso il basso di una riga è la dimensione completa in byte del numero di pixel che si adatterebbe all'interno del riquadro se il riquadro fosse pieno. Può quindi esserci uno spazio tra ogni riga di pixel in memoria. Per semplicità di specifica, le mipmap più piccole di un riquadro non vengono riunite nel layout lineare. Questo sembra uno spreco di spazio di memoria, ma come accennato, la copia in mips che l'hardware si riunisce non è consentita tramite [**CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) [**o UpdateTiles.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) L'applicazione può usare solo API Generic UpdateSubresource () o CopySubresource () per copiare singoli mip di piccole dimensioni, anche se nel caso di CopySubresource () ciò significa che la memoria lineare deve essere della stessa dimensione della risorsa affiancata. CopySubresource () non può, ad esempio, copiare da una risorsa \* \* buffer a \* \* texture2D.

Se viene definito uno swizzle standard hardware, è possibile aggiungere flag per indicare che i dati nel buffer devono essere interpretati in tale formato (non è necessario uno swizzle al trasferimento), anche se in questo caso possono essere sensato anche approcci alternativi al caricamento dei dati, ad esempio consentire alle applicazioni l'accesso diretto alla memoria del pool di riquadri.

Le operazioni di copia possono essere eseguite in un contesto immediato o posticipato.

## <a name="resizing-tile-pool"></a>Ridimensionamento del pool di riquadri

Per ridimensionare un pool di riquadri, [**usare ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool).

## <a name="tiled-resource-barrier"></a>Barriera delle risorse affiancate

Per specificare un vincolo di ordinamento dell'accesso ai dati tra più risorse affiancate, usare [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

 




