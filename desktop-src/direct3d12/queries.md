---
title: Query
description: In Direct3D 12, le query vengono raggruppate in matrici di query chiamate heap di query. Un heap di query dispone di un tipo che definisce i tipi di query validi che possono essere utilizzati con tale heap.
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c4db895eb0d4a727db2e32757f7ab0f1f9b1e2
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104548867"
---
# <a name="queries"></a>Query

In Direct3D 12, le query vengono raggruppate in matrici di query chiamate heap di query. Un heap di query dispone di un tipo che definisce i tipi di query validi che possono essere utilizzati con tale heap.

-   [Differenze nelle query da Direct3D 11 a Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Heap di query](#query-heaps)
-   [Creazione di heap di query](#creating-query-heaps)
-   [Estrazione di dati da una query](#extracting-data-from-a-query)
-   [Argomenti correlati](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Differenze nelle query da Direct3D 11 a Direct3D 12

I tipi di query seguenti non sono più presenti in Direct3D 12, le cui funzionalità sono incorporate in altri processi:

-   **Query evento** : l'evento è ora gestito da recinzioni.
-   **Query di timestamp non contigui** : gli orologi GPU possono essere impostati su uno stato stabile in Direct3D 12 (vedere la sezione relativa alla [temporizzazione](timing.md) ). I confronti di clock GPU non sono significativi se la GPU è inattiva tra i timestamp, nota come query non contigua. Con una potenza stabile due query di timestamp emesse da elenchi di comandi diversi sono in grado di confrontare in modo affidabile. Due timestamp inclusi nello stesso elenco di comandi sono sempre confrontabili in modo affidabile.
-   **Query statistiche output flusso** : in Direct3D 12 non è presente alcuna query di overflow per tutti i flussi di output. Le app devono eseguire più query a flusso singolo e quindi correlare i risultati.
-   Query sul predicato del **flusso di statistiche di output e di predicato di occlusione** : le query (che scrivono in memoria) e [predicazione](predication.md) (che leggono dalla memoria) non sono più associate, quindi questi tipi di query non sono necessari.

A Direct3D 12 è stato aggiunto un nuovo tipo di query di occlusione binaria. Ciò consente alle strategie predicazione che si occupano solo se un oggetto è stato completamente nascosto o meno (anziché il numero di pixel bloccati) per indicare questo al dispositivo, che potrebbe essere in grado di eseguire le query in modo più efficiente.

## <a name="query-heaps"></a>Heap di query

Le query possono essere una da un numero di tipi [**( \_ \_ \_ tipo di heap di query D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) e raggruppate in heap di query prima di essere inviate alla GPU.

È disponibile un nuovo tipo di query D3D12 \_ \_ . l' \_ \_ occlusione binaria del tipo di query è disponibile e agisce come l' \_ \_ occlusione del tipo di query D3D12 \_ , ad eccezione del fatto che restituisce un risultato binario 0/1:0 indica che nessun campione ha superato il test di profondità e stencil, 1 indica che almeno un campione ha superato il test Ciò consente alle query di occlusione di non interferire con l'ottimizzazione delle prestazioni della GPU associata a test depth/stencil.

## <a name="creating-query-heaps"></a>Creazione di heap di query

Le API rilevanti per la creazione di heap di query sono [**il \_ \_ \_ tipo di heap della query D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)enum, lo struct [**D3D12 \_ query \_ heap \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)e il metodo [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

Il runtime di base consentirà di verificare che il tipo di heap della query sia un membro valido dell'enumerazione del [**\_ \_ tipo di heap D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) e che il conteggio sia maggiore di 0.

Ogni singolo elemento query in un heap di query può essere avviato e arrestato separatamente.

Le API per l'uso degli heap di query sono il [**\_ \_ tipo di query enum D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)e i metodi [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

\_ \_ Il tipo di query D3D12 \_ timestamp è l'unica query che supporta solo [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) . Tutti gli altri tipi di query richiedono [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e **EndQuery**.

Il livello di debug convaliderà quanto segue:

-   Non è consentito iniziare una query timestamp. è &mdash; possibile terminare solo
-   Non è consentito iniziare una query due volte senza terminarla (per un determinato elemento). Per le query che richiedono sia Begin che end, non è consentito terminare una query prima dell'inizio corrispondente (per un determinato elemento).
-   Il tipo di query passato a [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) deve corrispondere al tipo di query passato a [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

Il runtime di base convaliderà quanto segue:

-   Impossibile chiamare [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) su una query timestamp.
-   Per i tipi di query che supportano sia [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) che [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) (tutti ad eccezione di timestamp), una query per un dato elemento non deve estendersi sui limiti degli elenchi di comandi.
-   *ElementIndex* deve essere compreso nell'intervallo.
-   Il tipo di query è un membro valido dell'enumerazione del [**\_ \_ tipo di query D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type) .
-   Il tipo di query deve essere compatibile con l'heap della query. La tabella seguente mostra il tipo di heap della query richiesto per ogni tipo di query:

    

    | Tipo di query                                  | Tipo di heap query                                |
    |---------------------------------------------|------------------------------------------------|
    | \_ \_ Occlusione del tipo di query D3D12 \_               | \_ \_ \_ Occlusione tipo di heap query \_ D3D12            |
    | \_ \_ \_ Occlusione binaria del tipo di query D3D12 \_       | \_ \_ \_ Occlusione tipo di heap query \_ D3D12            |
    | \_Timestamp del \_ tipo di query D3D12 \_               | \_ \_ \_ Timestamp tipo heap query \_ D3D12            |
    | \_Statistiche della \_ pipeline del tipo di query D3D12 \_ \_    | \_Statistiche della \_ \_ pipeline del tipo di heap query \_ D3D12 \_ |
    | Tipo di query D3D12, \_ \_ \_ quindi \_ statistiche \_ STREAM0 | \_Tipo di \_ heap query D3D12 \_ \_ per \_ statistiche       |
    | Tipo di query D3D12, \_ \_ \_ quindi \_ statistiche \_ stream1 | \_Tipo di \_ heap query D3D12 \_ \_ per \_ statistiche       |
    | Tipo di query D3D12, \_ \_ \_ quindi \_ statistiche \_ STREAM2 | \_Tipo di \_ heap query D3D12 \_ \_ per \_ statistiche       |
    | Tipo di query D3D12, \_ \_ \_ quindi \_ statistiche \_ STREAM3 | \_Tipo di \_ heap query D3D12 \_ \_ per \_ statistiche       |

    

     

-   Il tipo di query è supportato dal tipo di elenco dei comandi. Nella tabella seguente vengono illustrate le query supportate per i tipi di elenco dei comandi.

    

    | Tipo di query                                  | Tipi di elenco di comandi supportati         |
    |---------------------------------------------|--------------------------------------|
    | \_ \_ Occlusione del tipo di query D3D12 \_               | Connessione diretta                               |
    | \_ \_ \_ Occlusione binaria del tipo di query D3D12 \_       | Connessione diretta                               |
    | \_Timestamp del \_ tipo di query D3D12 \_               | Direct, COMPUTE e facoltativamente copia |
    | \_Statistiche della \_ pipeline del tipo di query D3D12 \_ \_    | Connessione diretta                               |
    | Tipo di query D3D12, \_ \_ \_ quindi \_ statistiche \_ STREAM0 | Connessione diretta                               |
    | Tipo di query D3D12, \_ \_ \_ quindi \_ statistiche \_ stream1 | Connessione diretta                               |
    | Tipo di query D3D12, \_ \_ \_ quindi \_ statistiche \_ STREAM2 | Connessione diretta                               |
    | Tipo di query D3D12, \_ \_ \_ quindi \_ statistiche \_ STREAM3 | Connessione diretta                               |

    

     

## <a name="extracting-data-from-a-query"></a>Estrazione di dati da una query

Per estrarre i dati da una query, è possibile usare il metodo [**ResolveQueryData**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) . **ResolveQueryData** funziona con tutti i tipi di memoria (indipendentemente dal fatto che si tratti di memoria di sistema o memoria locale del dispositivo), ma richiede che la risorsa di destinazione sia in [**D3D12_RESOURCE_STATE_COPY_DEST**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states). 

## <a name="related-topics"></a>Argomenti correlati

* [Contatori e query](counters-and-queries.md)
* [Procedura dettagliata per le query predicazione](predication-queries.md)
