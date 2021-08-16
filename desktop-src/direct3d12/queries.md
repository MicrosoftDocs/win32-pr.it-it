---
title: Query
description: In Direct3D 12 le query sono raggruppate in matrici di query denominate heap delle query. Un heap di query ha un tipo che definisce i tipi validi di query che possono essere usati con tale heap.
ms.assetid: d7403b5d-7e1b-4dd2-ae45-52e1153233c6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71279c09b59b417535f3155683747ac4c153d7d0fd9f668f79cab9b63ca79805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241951"
---
# <a name="queries"></a>Query

In Direct3D 12 le query sono raggruppate in matrici di query denominate heap delle query. Un heap di query ha un tipo che definisce i tipi validi di query che possono essere usati con tale heap.

-   [Differenze nelle query da Direct3D 11 a Direct3D 12](#differences-in-queries-from-direct3d-11-to-direct3d-12)
-   [Heap delle query](#query-heaps)
-   [Creazione di heap di query](#creating-query-heaps)
-   [Estrazione di dati da una query](#extracting-data-from-a-query)
-   [Argomenti correlati](#related-topics)

## <a name="differences-in-queries-from-direct3d-11-to-direct3d-12"></a>Differenze nelle query da Direct3D 11 a Direct3D 12

I tipi di query seguenti non sono più presenti in Direct3D 12 e le relative funzionalità vengono incorporate in altri processi:

-   **Query di** eventi: l'evento dal punto di vista funzionale è ora gestito da recinti.
-   **Query timestamp non contigue:** gli orologi della GPU possono essere impostati su uno stato stabile in Direct3D 12 (vedere la [sezione Intervallo).](timing.md) I confronti di clock GPU non sono significativi se la GPU è inattiva tra i timestamp (nota come query non contigua). Con la potenza stabile due query timestamp eseguite da elenchi di comandi diversi sono confrontabili in modo affidabile. Due timestamp all'interno dello stesso elenco di comandi sono sempre confrontabili in modo affidabile.
-   **Query di statistiche di output** del flusso: in Direct3D 12 non è disponibile una singola query di overflow dell'output del flusso per tutti i flussi di output. Le app devono eseguire più query a flusso singolo e quindi correlare i risultati.
-   [Query](predication.md) sul predicato delle statistiche di output del flusso e sul predicato di **occlusione:** le query (che scrivono in memoria) e il predicato (che legge dalla memoria) non sono più accoppiati e quindi questi tipi di query non sono necessari.

È stato aggiunto un nuovo tipo di query di occlusione binaria a Direct3D 12. In questo modo, le strategie di predicazione che prescindono solo se un oggetto è completamente occluso o meno (anziché il numero di pixel occluded) per indicare questo al dispositivo, che potrebbe essere in grado di eseguire le query in modo più efficiente.

## <a name="query-heaps"></a>Heap delle query

Le query possono essere di vari tipi ([**D3D12 \_ QUERY \_ HEAP \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)) e vengono raggruppate in heap di query prima di essere inviate alla GPU.

È disponibile un nuovo tipo di query D3D12 QUERY TYPE BINARY OCCLUSION e funziona come D3D12 QUERY TYPE OCCLUSION, ad eccezione del fatto che restituisce un risultato \_ \_ \_ \_ \_ \_ \_ 0/1 binario: 0 indica che nessun campione ha superato i test di profondità e stencil, 1 indica che almeno un campione ha superato la profondità e il test degli stencil. In questo modo le query di occlusione non interferiscono con l'ottimizzazione delle prestazioni della GPU associata al test di profondità/stencil.

## <a name="creating-query-heaps"></a>Creazione di heap di query

Le API rilevanti per la creazione di heap di query sono l'enumerazione [**D3D12 \_ QUERY \_ HEAP \_ TYPE,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_heap_type)lo struct [**D3D12 \_ QUERY HEAP \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_query_heap_desc)e il metodo [**CreateQueryHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createqueryheap).

Il runtime principale convaliderà che il tipo di heap della query è un membro valido dell'enumerazione [**D3D12 \_ HEAP \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type) e che il conteggio è maggiore di 0.

Ogni singolo elemento di query all'interno di un heap di query può essere avviato e arrestato separatamente.

Le API per l'uso degli heap di query sono l'enumerazione [**D3D12 \_ QUERY \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)e i metodi [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) [**ed EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery).

D3D12 \_ QUERY TYPE TIMESTAMP è \_ \_ l'unica query che supporta solo [**EndQuery.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) Tutti gli altri tipi di query [**richiedono BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) **ed EndQuery**.

Il livello di debug convaliderà quanto segue:

-   Non è valido iniziare una query di timestamp &mdash; che è possibile terminare solo
-   Non è valido avviare una query due volte senza terminarla (per un determinato elemento). Per le query che richiedono sia begin che end, non è valido terminare una query prima dell'inizio corrispondente (per un determinato elemento).
-   Il tipo di query passato [**a BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) deve corrispondere al tipo di query passato a [**EndQuery.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)

Il runtime di base convaliderà quanto segue:

-   [**Non è possibile**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) chiamare BeginQuery su una query timestamp.
-   Per i tipi di query che supportano [**sia BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) che [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) (tutti tranne timestamp), una query per un determinato elemento non deve estendersi oltre i limiti dell'elenco dei comandi.
-   *ElementIndex deve* essere compreso nell'intervallo.
-   Il tipo di query è un membro valido [**dell'enumerazione D3D12 \_ QUERY \_ TYPE.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)
-   Il tipo di query deve essere compatibile con l'heap delle query. La tabella seguente illustra il tipo di heap di query richiesto per ogni tipo di query:

    

    | Tipo di query                                  | Tipo di heap delle query                                |
    |---------------------------------------------|------------------------------------------------|
    | \_OCCLUSIONE DEL TIPO DI QUERY D3D12 \_ \_               | OCCLUSIONE DEL TIPO \_ \_ DI HEAP \_ DELLE QUERY D3D12 \_            |
    | \_OCCLUSIONE BINARIA DEL TIPO DI QUERY D3D12 \_ \_ \_       | OCCLUSIONE DEL TIPO \_ \_ DI HEAP \_ DELLE QUERY D3D12 \_            |
    | TIMESTAMP DEL TIPO DI QUERY D3D12 \_ \_ \_               | TIMESTAMP TIPO \_ HEAP QUERY D3D12 \_ \_ \_            |
    | STATISTICHE PIPELINE DEL TIPO DI QUERY D3D12 \_ \_ \_ \_    | STATISTICHE PIPELINE TIPO \_ \_ HEAP QUERY \_ \_ D3D12 \_ |
    | TIPO DI QUERY D3D12 \_ IN MODO CHE STATISTICS \_ \_ \_ \_ STREAM0 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | TIPO DI QUERY D3D12 \_ IN MODO CHE STATISTICS \_ \_ \_ \_ STREAM1 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | TIPO DI QUERY D3D12 \_ IN MODO CHE STATISTICS \_ \_ \_ \_ STREAM2 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |
    | TIPO DI QUERY D3D12 \_ IN MODO CHE STATISTICS \_ \_ \_ \_ STREAM3 | D3D12 \_ QUERY \_ HEAP \_ TYPE \_ SO \_ STATISTICS       |

    

     

-   Il tipo di query è supportato dal tipo di elenco dei comandi. Nella tabella seguente vengono illustrate le query supportate per i tipi di elenco dei comandi.

    

    | Tipo di query                                  | Tipi di elenco di comandi supportati         |
    |---------------------------------------------|--------------------------------------|
    | \_OCCLUSIONE DEL TIPO DI QUERY D3D12 \_ \_               | Connessione diretta                               |
    | \_OCCLUSIONE BINARIA DEL TIPO DI QUERY D3D12 \_ \_ \_       | Connessione diretta                               |
    | TIMESTAMP DEL TIPO DI QUERY D3D12 \_ \_ \_               | Direct, Compute e facoltativamente Copy |
    | STATISTICHE PIPELINE DEL TIPO DI QUERY D3D12 \_ \_ \_ \_    | Connessione diretta                               |
    | TIPO DI QUERY D3D12 \_ IN MODO CHE STATISTICS \_ \_ \_ \_ STREAM0 | Connessione diretta                               |
    | TIPO DI QUERY D3D12 \_ IN MODO CHE STATISTICS \_ \_ \_ \_ STREAM1 | Connessione diretta                               |
    | TIPO DI QUERY D3D12 \_ IN MODO CHE STATISTICS \_ \_ \_ \_ STREAM2 | Connessione diretta                               |
    | TIPO DI QUERY D3D12 \_ IN MODO CHE STATISTICS \_ \_ \_ \_ STREAM3 | Connessione diretta                               |

    

     

## <a name="extracting-data-from-a-query"></a>Estrazione di dati da una query

Il modo per estrarre dati da una query è usare il [**metodo ResolveQueryData.**](/windows/win32p/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) **ResolveQueryData funziona** con tutti i tipi di memoria (che si tratta di memoria di sistema o memoria locale del dispositivo), ma richiede che la risorsa di destinazione si D3D12_RESOURCE_STATE_COPY_DEST [**.**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) 

## <a name="related-topics"></a>Argomenti correlati

* [Contatori e query](counters-and-queries.md)
* [Procedura per le query di predicato](predication-queries.md)
