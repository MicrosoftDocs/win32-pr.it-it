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
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a><span data-ttu-id="00c9c-103">Indicizzazione delle priorità e degli eventi del set di righe in Windows 7</span><span class="sxs-lookup"><span data-stu-id="00c9c-103">Indexing Prioritization and Rowset Events in Windows 7</span></span>

<span data-ttu-id="00c9c-104">In questo argomento viene illustrata l'introduzione dell'indicizzazione delle priorità e degli eventi del set di righe per Windows 7.</span><span class="sxs-lookup"><span data-stu-id="00c9c-104">This topic outlines the introduction of indexing prioritization and rowset events for Windows 7.</span></span>

<span data-ttu-id="00c9c-105">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="00c9c-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="00c9c-106">Indicizzazione delle priorità e degli eventi del set di righe</span><span class="sxs-lookup"><span data-stu-id="00c9c-106">Indexing Prioritization and Rowset Events</span></span>](#indexing-prioritization-and-rowset-events)
    -   [<span data-ttu-id="00c9c-107">Esempi di IRowsetPriorization</span><span class="sxs-lookup"><span data-stu-id="00c9c-107">IRowsetPriorization Examples</span></span>](#irowsetpriorization-examples)
    -   [<span data-ttu-id="00c9c-108">Eventi IRowsetPrioritization</span><span class="sxs-lookup"><span data-stu-id="00c9c-108">IRowsetPrioritization Events</span></span>](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [<span data-ttu-id="00c9c-109">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="00c9c-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="00c9c-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00c9c-110">Related topics</span></span>](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a><span data-ttu-id="00c9c-111">Indicizzazione delle priorità e degli eventi del set di righe</span><span class="sxs-lookup"><span data-stu-id="00c9c-111">Indexing Prioritization and Rowset Events</span></span>

<span data-ttu-id="00c9c-112">In Windows 7 e versioni successive esiste uno stack di priorità entro il quale il contesto di una query specifica, il client può richiedere che agli ambiti utilizzati nella query venga assegnata la priorità sopra quella degli elementi normali.</span><span class="sxs-lookup"><span data-stu-id="00c9c-112">In Windows 7?and later, there is a priority stack within which the context of any particular query, the client can request that the scopes used in that query be prioritized above that of normal items.</span></span>

<span data-ttu-id="00c9c-113">Questo stack di assegnazione delle priorità presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="00c9c-113">This prioritization stack has the following characteristics:</span></span>

-   <span data-ttu-id="00c9c-114">Gli elementi nello stack possono avere priorità in primo piano, alta o bassa:</span><span class="sxs-lookup"><span data-stu-id="00c9c-114">Items in the stack can have foreground, high, or low priority:</span></span>
    -   <span data-ttu-id="00c9c-115">**Primo piano**: la logica backoff viene ignorata e l'indicizzazione viene eseguita con la massima rapidità consentita dal computer.</span><span class="sxs-lookup"><span data-stu-id="00c9c-115">**Foreground**: Backoff logic is skipped and indexing proceeds as fast as the machine allows.</span></span>
    -   <span data-ttu-id="00c9c-116">**Alta**: la priorità è stata richiesta con backoff.</span><span class="sxs-lookup"><span data-stu-id="00c9c-116">**High**: Prioritization has been requested with backoff.</span></span>
    -   <span data-ttu-id="00c9c-117">**Bassa**: è stata richiesta la priorità, non a scapito di altri ambiti nello stack, ma sopra l'indicizzazione senza priorità.</span><span class="sxs-lookup"><span data-stu-id="00c9c-117">**Low**: Prioritization has been requested, not at the expense of other scopes on the stack, but above non-prioritized indexing.</span></span>
-   <span data-ttu-id="00c9c-118">Qualsiasi richiesta di priorità alta o in primo piano urta automaticamente la query richiedente all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="00c9c-118">Any request for high or foreground priority bumps the requesting query to the top of the stack automatically.</span></span>
-   <span data-ttu-id="00c9c-119">Solo l'elemento all'inizio dello stack può avere priorità in primo piano.</span><span class="sxs-lookup"><span data-stu-id="00c9c-119">Only the item on top of the stack can have foreground priority.</span></span>
-   <span data-ttu-id="00c9c-120">Una query con priorità in primo piano arrestata in priorità riceve un evento che informa che ha perso la priorità di primo piano e che è diventata una priorità alta con backoff.</span><span class="sxs-lookup"><span data-stu-id="00c9c-120">A query with foreground priority that is bumped down in priority receives an event notifying it that it has lost foreground priority and has become a high priority with backoff.</span></span>

<span data-ttu-id="00c9c-121">Lo stack di priorità imposta una priorità complessiva degli elementi elaborati nell'indicizzatore come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="00c9c-121">The priority stack sets an overall priority of items that are processed in the indexer as follows:</span></span>

-   <span data-ttu-id="00c9c-122">Le notifiche con priorità alta non hanno backoff e vengono in genere inviate solo per un numero ridotto di elementi.</span><span class="sxs-lookup"><span data-stu-id="00c9c-122">High Priority notifications have no backoff, and are typically sent only for a small number of items.</span></span> <span data-ttu-id="00c9c-123">Ad esempio, Esplora risorse utilizza questa priorità per le operazioni del motore di copia di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="00c9c-123">For example, Windows Explorer uses this priority for small copy engine operations.</span></span>
-   <span data-ttu-id="00c9c-124">Lo stack di priorità è parte superiore dello stack, contiene backoff ed è l'ultima query di priorità richiesta.</span><span class="sxs-lookup"><span data-stu-id="00c9c-124">Priority Stack is top of the stack, has backoff, and is the last requested priority query.</span></span>
-   <span data-ttu-id="00c9c-125">Seconda query nello stack.</span><span class="sxs-lookup"><span data-stu-id="00c9c-125">Second query in the stack.</span></span>
-   <span data-ttu-id="00c9c-126">Terza query nello stack.</span><span class="sxs-lookup"><span data-stu-id="00c9c-126">Third query in the stack.</span></span>
-   <span data-ttu-id="00c9c-127">Quarta query nello stack e così via.</span><span class="sxs-lookup"><span data-stu-id="00c9c-127">Fourth query in the stack, and so forth.</span></span>
-   <span data-ttu-id="00c9c-128">Elementi con priorità normale.</span><span class="sxs-lookup"><span data-stu-id="00c9c-128">Normal Priority items.</span></span>
-   <span data-ttu-id="00c9c-129">Elementi eliminati.</span><span class="sxs-lookup"><span data-stu-id="00c9c-129">Deleted items.</span></span>
    > [!Note]  
    > <span data-ttu-id="00c9c-130">Gli elementi all'interno di ogni gruppo vengono classificati in ordine di priorità internamente tramite la semantica per elemento precedente.</span><span class="sxs-lookup"><span data-stu-id="00c9c-130">Items within each group are prioritized internally through the older per-item semantics.</span></span>

     

### <a name="irowsetpriorization-examples"></a><span data-ttu-id="00c9c-131">Esempi di IRowsetPriorization</span><span class="sxs-lookup"><span data-stu-id="00c9c-131">IRowsetPriorization Examples</span></span>

<span data-ttu-id="00c9c-132">L'API primaria per il lavoro di assegnazione delle priorità è disponibile tramite l'interfaccia seguente, che può essere chiamata eseguendo una query sul set di righe restituito:</span><span class="sxs-lookup"><span data-stu-id="00c9c-132">The primary API for prioritization work is available through the following interface, which can be called by querying the returned rowset:</span></span>


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



<span data-ttu-id="00c9c-133">La priorità del set di righe funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="00c9c-133">Rowset prioritization works as follows:</span></span>

1.  <span data-ttu-id="00c9c-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) viene acquisito con il [metodo IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su un set di righe dell'indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="00c9c-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) is acquired with [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an indexer rowset.</span></span> <span data-ttu-id="00c9c-135">**DBPROP \_ ENABLEROWSETEVENTS** deve essere impostato su **true** con il metodo OLE DB [ICommandProperties::](/previous-versions/windows/desktop/ms711497(v=vs.85)) SetValue prima di eseguire la query in modo da utilizzare le priorità dei set di righe.</span><span class="sxs-lookup"><span data-stu-id="00c9c-135">**DBPROP\_ENABLEROWSETEVENTS** must be set to **TRUE** with the OLE DB [ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) method prior to executing the query in order to use rowset prioritization.</span></span>
2.  <span data-ttu-id="00c9c-136">[**IRowsetPrioritization:: SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) imposta la priorità per gli ambiti che appartengono alla query e l'intervallo in cui viene generato l'evento Statistics di ambito quando sono presenti documenti in attesa da indicizzare all'interno degli ambiti di query.</span><span class="sxs-lookup"><span data-stu-id="00c9c-136">[**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes.</span></span> <span data-ttu-id="00c9c-137">Questo evento viene generato se il livello di priorità è impostato sul valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="00c9c-137">This event is raised if the priority level is set to default.</span></span>
3.  <span data-ttu-id="00c9c-138">[**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) può essere utilizzato per ottenere il numero di elementi indicizzati nell'ambito, il numero di documenti in attesa da aggiungere nell'ambito e il numero di documenti che devono essere reindicizzati all'interno di questo ambito.</span><span class="sxs-lookup"><span data-stu-id="00c9c-138">[**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.</span></span>

### <a name="irowsetprioritization-events"></a><span data-ttu-id="00c9c-139">Eventi IRowsetPrioritization</span><span class="sxs-lookup"><span data-stu-id="00c9c-139">IRowsetPrioritization Events</span></span>

<span data-ttu-id="00c9c-140">Sono presenti tre eventi del set di righe in [**IRowsetEvents:: OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) nell'enumerazione del [**\_ tipo ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :</span><span class="sxs-lookup"><span data-stu-id="00c9c-140">There are three rowset events in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in the [**ROWSETEVENT\_TYPE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) enumeration:</span></span>


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



<span data-ttu-id="00c9c-141">Gli eventi del set di righe sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="00c9c-141">The rowset events are as follows:</span></span>

-   <span data-ttu-id="00c9c-142">L' **evento \_ \_ dataexpire di tipo ROWSETEVENT** indica che il backup dei dati del set di righe è scaduto e che è necessario richiedere un nuovo set di righe.</span><span class="sxs-lookup"><span data-stu-id="00c9c-142">The **ROWSETEVENT\_TYPE\_DATAEXPIRED** event indicates that data backing the rowset has expired, and that a new rowset should be requested.</span></span>
-   <span data-ttu-id="00c9c-143">Il **tipo di set di righe evento \_ \_ FOREGROUNDLOST** indica che un elemento con priorità di primo piano nello stack di assegnazione delle priorità è stato abbassato di grado, perché qualcun altro ha assegnato priorità a questa query.</span><span class="sxs-lookup"><span data-stu-id="00c9c-143">The **ROWSET\_TYPE\_FOREGROUNDLOST** event indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.</span></span>
-   <span data-ttu-id="00c9c-144">L'evento **ROWSETEVENT di \_ tipo \_ SCOPESTATISTICS** fornisce le stesse informazioni disponibili dalla chiamata al metodo [**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , ma tramite un Mechanical push, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="00c9c-144">The **ROWSETEVENT\_TYPE\_SCOPESTATISTICS** event gives you the same information available from the [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) method call, but through a push mechanic, as follows:</span></span>
    -   <span data-ttu-id="00c9c-145">L'evento si verifica se l'API per la definizione delle priorità è stata usata per richiedere un livello di priorità non predefinito e una frequenza di eventi delle statistiche diverse da zero.</span><span class="sxs-lookup"><span data-stu-id="00c9c-145">The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.</span></span>
    -   <span data-ttu-id="00c9c-146">L'evento si verifica solo quando le statistiche cambiano effettivamente e l'intervallo specificato in [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) è scaduto (l'intervallo non garantisce la frequenza dell'evento).</span><span class="sxs-lookup"><span data-stu-id="00c9c-146">The event arises only when statistics actually change, and the interval specified in the [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) has elapsed (the interval does not guarantee the frequency of the event).</span></span>
    -   <span data-ttu-id="00c9c-147">Questo evento è garantito per generare uno stato di "rimbalzo zero" (zero elementi rimanenti da aggiungere, zero modifiche rimanenti), a condizione che sia stato generato un evento diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="00c9c-147">This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</span></span>
    -   <span data-ttu-id="00c9c-148">L'indicizzatore può elaborare elementi senza inviare questo evento, se la coda viene svuotata prima della frequenza dell'evento Statistics.</span><span class="sxs-lookup"><span data-stu-id="00c9c-148">The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00c9c-149">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="00c9c-149">Additional Resources</span></span>

<span data-ttu-id="00c9c-150">Vedere le risorse seguenti relative alla priorità e ai set di righe:</span><span class="sxs-lookup"><span data-stu-id="00c9c-150">See the following resources related to prioritization and rowsets:</span></span>

-   <span data-ttu-id="00c9c-151">Interfacce:</span><span class="sxs-lookup"><span data-stu-id="00c9c-151">Interfaces:</span></span>
    -   [<span data-ttu-id="00c9c-152">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="00c9c-152">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [<span data-ttu-id="00c9c-153">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="00c9c-153">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   <span data-ttu-id="00c9c-154">Enumerazioni:</span><span class="sxs-lookup"><span data-stu-id="00c9c-154">Enumerations:</span></span>
    -   [<span data-ttu-id="00c9c-155">**ASSEGNARE priorità ai \_ flag**</span><span class="sxs-lookup"><span data-stu-id="00c9c-155">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [<span data-ttu-id="00c9c-156">**livello di priorità \_**</span><span class="sxs-lookup"><span data-stu-id="00c9c-156">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [<span data-ttu-id="00c9c-157">**\_ITEMSTATE ROWSETEVENT**</span><span class="sxs-lookup"><span data-stu-id="00c9c-157">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [<span data-ttu-id="00c9c-158">**\_tipo ROWSETEVENT**</span><span class="sxs-lookup"><span data-stu-id="00c9c-158">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a><span data-ttu-id="00c9c-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00c9c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00c9c-160">Ricerca di Windows 7</span><span class="sxs-lookup"><span data-stu-id="00c9c-160">Windows 7 Search</span></span>](./-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="00c9c-161">Novità per ricerca Windows 7</span><span class="sxs-lookup"><span data-stu-id="00c9c-161">New for Windows 7 Search</span></span>](new-for-windows-7-search.md)
</dt> <dt>

[<span data-ttu-id="00c9c-162">Librerie shell di Windows in Windows 7</span><span class="sxs-lookup"><span data-stu-id="00c9c-162">Windows Shell Libraries in Windows 7</span></span>](-search-win7-development-scenarios.md)
</dt> </dl>

 

 