---
description: Descrive l'introduzione dell'indicizzazione delle priorità e degli eventi del set di righe per Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indicizzazione delle priorità e degli eventi del set di righe in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320335"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>Indicizzazione delle priorità e degli eventi del set di righe in Windows 7

In questo argomento viene illustrata l'introduzione dell'indicizzazione delle priorità e degli eventi del set di righe per Windows 7.

Questo argomento è organizzato nel modo seguente:

-   [Indicizzazione delle priorità e degli eventi del set di righe](#indexing-prioritization-and-rowset-events)
    -   [Esempi di IRowsetPriorization](#irowsetpriorization-examples)
    -   [Eventi IRowsetPrioritization](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Indicizzazione delle priorità e degli eventi del set di righe

In Windows 7 e versioni successive esiste uno stack di priorità entro il quale il contesto di una query specifica, il client può richiedere che agli ambiti utilizzati nella query venga assegnata la priorità sopra quella degli elementi normali.

Questo stack di assegnazione delle priorità presenta le caratteristiche seguenti:

-   Gli elementi nello stack possono avere priorità in primo piano, alta o bassa:
    -   **Primo piano**: la logica backoff viene ignorata e l'indicizzazione viene eseguita con la massima rapidità consentita dal computer.
    -   **Alta**: la priorità è stata richiesta con backoff.
    -   **Bassa**: è stata richiesta la priorità, non a scapito di altri ambiti nello stack, ma sopra l'indicizzazione senza priorità.
-   Qualsiasi richiesta di priorità alta o in primo piano urta automaticamente la query richiedente all'inizio dello stack.
-   Solo l'elemento all'inizio dello stack può avere priorità in primo piano.
-   Una query con priorità in primo piano arrestata in priorità riceve un evento che informa che ha perso la priorità di primo piano e che è diventata una priorità alta con backoff.

Lo stack di priorità imposta una priorità complessiva degli elementi elaborati nell'indicizzatore come indicato di seguito:

-   Le notifiche con priorità alta non hanno backoff e vengono in genere inviate solo per un numero ridotto di elementi. Ad esempio, Esplora risorse utilizza questa priorità per le operazioni del motore di copia di piccole dimensioni.
-   Lo stack di priorità è parte superiore dello stack, contiene backoff ed è l'ultima query di priorità richiesta.
-   Seconda query nello stack.
-   Terza query nello stack.
-   Quarta query nello stack e così via.
-   Elementi con priorità normale.
-   Elementi eliminati.
    > [!Note]  
    > Gli elementi all'interno di ogni gruppo vengono classificati in ordine di priorità internamente tramite la semantica per elemento precedente.

     

### <a name="irowsetpriorization-examples"></a>Esempi di IRowsetPriorization

L'API primaria per il lavoro di assegnazione delle priorità è disponibile tramite l'interfaccia seguente, che può essere chiamata eseguendo una query sul set di righe restituito:


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



La priorità del set di righe funziona nel modo seguente:

1.  [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) viene acquisito con il [metodo IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un set di righe dell'indicizzatore. **DBPROP \_ ENABLEROWSETEVENTS** deve essere impostato su **true** con il metodo OLE DB [ICommandProperties::](/previous-versions/windows/desktop/ms711497(v=vs.85)) SetValue prima di eseguire la query in modo da utilizzare le priorità dei set di righe.
2.  [**IRowsetPrioritization:: SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) imposta la priorità per gli ambiti che appartengono alla query e l'intervallo in cui viene generato l'evento Statistics di ambito quando sono presenti documenti in attesa da indicizzare all'interno degli ambiti di query. Questo evento viene generato se il livello di priorità è impostato sul valore predefinito.
3.  [**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) può essere utilizzato per ottenere il numero di elementi indicizzati nell'ambito, il numero di documenti in attesa da aggiungere nell'ambito e il numero di documenti che devono essere reindicizzati all'interno di questo ambito.

### <a name="irowsetprioritization-events"></a>Eventi IRowsetPrioritization

Sono presenti tre eventi del set di righe in [**IRowsetEvents:: OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) nell'enumerazione del [**\_ tipo ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



Gli eventi del set di righe sono i seguenti:

-   L' **evento \_ \_ dataexpire di tipo ROWSETEVENT** indica che il backup dei dati del set di righe è scaduto e che è necessario richiedere un nuovo set di righe.
-   Il **tipo di set di righe evento \_ \_ FOREGROUNDLOST** indica che un elemento con priorità di primo piano nello stack di assegnazione delle priorità è stato abbassato di grado, perché qualcun altro ha assegnato priorità a questa query.
-   L'evento **ROWSETEVENT di \_ tipo \_ SCOPESTATISTICS** fornisce le stesse informazioni disponibili dalla chiamata al metodo [**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , ma tramite un Mechanical push, come indicato di seguito:
    -   L'evento si verifica se l'API per la definizione delle priorità è stata usata per richiedere un livello di priorità non predefinito e una frequenza di eventi delle statistiche diverse da zero.
    -   L'evento si verifica solo quando le statistiche cambiano effettivamente e l'intervallo specificato in [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) è scaduto (l'intervallo non garantisce la frequenza dell'evento).
    -   Questo evento è garantito per generare uno stato di "rimbalzo zero" (zero elementi rimanenti da aggiungere, zero modifiche rimanenti), a condizione che sia stato generato un evento diverso da zero.
    -   L'indicizzatore può elaborare elementi senza inviare questo evento, se la coda viene svuotata prima della frequenza dell'evento Statistics.

## <a name="additional-resources"></a>Risorse aggiuntive

Vedere le risorse seguenti relative alla priorità e ai set di righe:

-   Interfacce:
    -   [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Enumerazioni:
    -   [**ASSEGNARE priorità ai \_ flag**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**livello di priorità \_**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**\_ITEMSTATE ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**\_tipo ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca di Windows 7](./-search-3x-wds-overview.md)
</dt> <dt>

[Novità per ricerca Windows 7](new-for-windows-7-search.md)
</dt> <dt>

[Librerie shell di Windows in Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 