---
description: Descrive l'introduzione dell'indicizzazione delle priorità e degli eventi del set di righe per Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indicizzazione di priorità ed eventi del set di righe in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92491300127c60ebdf2a265583fca77e77a09907b7f42b471f6d3d047a7f6aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680502"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>Indicizzazione di priorità ed eventi del set di righe in Windows 7

Questo argomento descrive l'introduzione dell'indicizzazione degli eventi di priorità e set di righe per Windows 7.

Questo argomento è organizzato come segue:

-   [Priorità di indicizzazione ed eventi del set di righe](#indexing-prioritization-and-rowset-events)
    -   [Esempi di IRowsetPriorization](#irowsetpriorization-examples)
    -   [Eventi IRowsetPrioritization](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Priorità di indicizzazione ed eventi del set di righe

In Windows 7?e versioni successive è presente uno stack di priorità all'interno del quale il contesto di una determinata query può richiedere che gli ambiti usati in tale query siano prioritari rispetto a quello degli elementi normali.

Questo stack di priorità presenta le caratteristiche seguenti:

-   Gli elementi nello stack possono avere priorità in primo piano, alta o bassa:
    -   **Primo** piano: la logica di backoff viene ignorata e l'indicizzazione procede alla stessa velocità del computer.
    -   **Alta:** la priorità è stata richiesta con backoff.
    -   **Bassa:** è stata richiesta la priorità, non a scapito di altri ambiti nello stack, ma sopra l'indicizzazione senza priorità.
-   Qualsiasi richiesta di priorità alta o in primo piano genera automaticamente l'urto della query richiedente all'inizio dello stack.
-   Solo l'elemento all'inizio dello stack può avere la priorità in primo piano.
-   Una query con priorità in primo piano con priorità elevata riceve un evento che notifica che ha perso la priorità in primo piano ed è diventata una priorità alta con backoff.

Lo stack di priorità imposta una priorità complessiva degli elementi elaborati nell'indicizzatore come indicato di seguito:

-   Le notifiche con priorità alta non hanno backoff e vengono in genere inviate solo per un numero ridotto di elementi. Ad esempio, Windows Explorer usa questa priorità per le piccole operazioni del motore di copia.
-   Lo stack di priorità è all'inizio dello stack, ha backoff ed è l'ultima query di priorità richiesta.
-   Seconda query nello stack.
-   Terza query nello stack.
-   Quarta query nello stack e così via.
-   Elementi con priorità normale.
-   Elementi eliminati.
    > [!Note]  
    > Gli elementi all'interno di ogni gruppo vengono classificati in ordine di priorità internamente tramite la semantica per elemento precedente.

     

### <a name="irowsetpriorization-examples"></a>Esempi di IRowsetPriorization

L'API primaria per il lavoro di assegnazione delle priorità è disponibile tramite l'interfaccia seguente, che può essere chiamata tramite query sul set di righe restituito:


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



La priorità dei set di righe funziona come segue:

1.  [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) viene acquisito con [il metodo IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) in un set di righe dell'indicizzatore. **DBPROP \_ ENABLEROWSETEVENTS** deve essere impostato su **TRUE** con il metodo [OLE DB ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) prima di eseguire la query per usare la priorità del set di righe.
2.  [**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) imposta la priorità per gli ambiti appartenenti alla query e l'intervallo in cui viene generato l'evento delle statistiche di ambito quando sono presenti documenti in sospeso da indicizzare all'interno degli ambiti della query. Questo evento viene generato se il livello di priorità è impostato su predefinito.
3.  [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) può essere usato per ottenere il numero di elementi indicizzati nell'ambito, il numero di documenti in sospeso da aggiungere nell'ambito e il numero di documenti che devono essere indicizzati nuovamente all'interno di questo ambito.

### <a name="irowsetprioritization-events"></a>Eventi IRowsetPrioritization

Esistono tre eventi di set di righe in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) [**nell'enumerazione ROWSETEVENT \_ TYPE:**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)


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

-   **L'evento ROWSETEVENT \_ TYPE \_ DATAEXPIRED** indica che i dati di backup del set di righe sono scaduti e che deve essere richiesto un nuovo set di righe.
-   **L'evento ROWSET \_ TYPE \_ FOREGROUNDLOST** indica che un elemento con priorità in primo piano nello stack di priorità è stato abbassato di livello, perché un altro utente ha impostato la priorità prima di questa query.
-   **L'evento ROWSETEVENT \_ TYPE \_ SCOPESTATISTICS** fornisce le stesse informazioni disponibili dalla chiamata al metodo [**IRowsetPrioritization::GetScopeStatistics,**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) ma tramite un meccanismo di push, come indicato di seguito:
    -   L'evento si verifica se l'API di assegnazione delle priorità è stata usata per richiedere un livello di priorità non predefinito e una frequenza di eventi di statistiche diversa da zero.
    -   L'evento si verifica solo quando le statistiche cambiano effettivamente e l'intervallo specificato in [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) è trascorso (l'intervallo non garantisce la frequenza dell'evento).
    -   Questo evento genera uno stato "bounce zero" (zero elementi rimanenti da aggiungere, zero modifica i rimanenti), a condizione che sia stato generato un evento diverso da zero.
    -   L'indicizzatore può elaborare gli elementi senza inviare questo evento, se la coda si svuota prima della frequenza degli eventi delle statistiche.

## <a name="additional-resources"></a>Risorse aggiuntive

Vedere le risorse seguenti correlate alla definizione delle priorità e ai set di righe:

-   Interfacce:
    -   [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Enumerazioni:
    -   [**ASSEGNARE PRIORITÀ AI \_ FLAG**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**LIVELLO DI \_ PRIORITÀ**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**TIPO \_ ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows 7 Ricerca](./-search-3x-wds-overview.md)
</dt> <dt>

[Novità della Windows 7](new-for-windows-7-search.md)
</dt> <dt>

[Windows Librerie shell in Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 