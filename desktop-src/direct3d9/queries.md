---
description: Esistono diversi tipi di query progettate per eseguire query sullo stato delle risorse.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Query (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2113500673def3e2cca5816e534b567a29fc322fb51f853db98eada20ba62674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068996"
---
# <a name="queries-direct3d-9"></a>Query (Direct3D 9)

Esistono diversi tipi di query progettate per eseguire query sullo stato delle risorse. Lo stato di una determinata risorsa include lo stato dell'unità di elaborazione grafica (GPU), lo stato del driver o lo stato di runtime. Per comprendere la differenza tra i diversi tipi di query, è necessario comprendere gli stati della query. Il diagramma di transizione dello stato seguente illustra ognuno degli stati della query.

![Diagramma che illustra le transizioni tra gli stati delle query](images/queries.png)

Il diagramma mostra tre stati, ognuno definito da cerchi. Ognuna delle linee solide è un evento basato sull'applicazione che causa una transizione di stato. La linea tratteggiata è un evento basato su risorse che passa una query dallo stato emesso allo stato segnalato. Ognuno di questi stati ha uno scopo diverso:

-   Lo stato segnalato è simile a uno stato di inattività. L'oggetto query è stato generato ed è in attesa che l'applicazione esere la query. Al termine di una query e dopo la transizione allo stato segnalato, è possibile recuperare la risposta alla query.
-   Lo stato di compilazione è simile a un'area di staging per una query. Dallo stato di compilazione è stata eseguita una query (chiamando [**D3DISSUE \_ BEGIN),**](d3dissue-begin.md)ma non è ancora stata eseguita la transizione allo stato rilasciato. Quando un'applicazione emette un termine della query (chiamando [**D3DISSUE \_ END),**](d3dissue-end.md)la query passa allo stato emesso.
-   Lo stato emesso indica che la risorsa su cui viene eseguita una query ha il controllo della query. Al termine del lavoro della risorsa, la risorsa esegue la transizione della macchina a stati allo stato segnalato. Durante lo stato emesso, l'applicazione deve eseguire il polling per rilevare la transizione allo stato segnalato. Una volta eseguita la transizione allo stato segnalato, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituisce il risultato della query (tramite un argomento) all'applicazione.

Nella tabella seguente sono elencati i tipi di query disponibili.



| Tipo di query        | Evento di problema                                                                      | Buffer GetData                                                              | Runtime      | Inizio implicito della query                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| BANDWIDTHTIMINGS  | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | Vendita al dettaglio/debug | N/A                                              |
| CACHEUTILIZATION  | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | Vendita al dettaglio/debug | N/A                                              |
| Evento             | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | BOOL                                                                        | Vendita al dettaglio/debug | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| INTERFACETIMINGS  | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | Vendita al dettaglio/debug | N/A                                              |
| Occlusione         | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | DWORD                                                                       | Vendita al dettaglio/debug | N/A                                              |
| PIPELINETIMING   | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | Vendita al dettaglio/debug | N/A                                              |
| Resourcemanager   | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md)           | Solo debug   | [**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | UINT64                                                                      | Vendita al dettaglio/debug | N/A                                              |
| TIMESTAMPDISJOINT | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | BOOL                                                                        | Vendita al dettaglio/debug | N/A                                              |
| TIMESTAMPFREQ     | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | UINT64                                                                      | Vendita al dettaglio/debug | N/A                                              |
| Vcache            | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ VCACHE**](d3ddevinfo-vcache.md)                             | Vendita al dettaglio/debug | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| VERTEXSTATS       | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | Solo debug   | [**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| VERTEXTIMING     | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | Vendita al dettaglio/debug | N/A                                              |



 

Alcune query richiedono un evento di inizio e di fine, mentre altre richiedono solo un evento finale. Le query che richiedono un evento finale iniziano solo quando si verifica un altro evento implicito (elencato nella tabella). Tutte le query restituiscono una risposta, ad eccezione della query di eventi la cui risposta è sempre **TRUE.** Un'applicazione usa lo stato della query o il codice restituito di [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Creare una query

Prima di creare una query, è possibile verificare se il runtime supporta le query chiamando [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) con un **puntatore NULL** simile al seguente:


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Questo metodo restituisce un codice di esito positivo se è possibile creare una query. in caso contrario, restituisce un codice di errore. Al [**termine di CreateQuery,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) è possibile creare un oggetto query simile al seguente:


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Se questa chiamata ha esito positivo, viene creato un oggetto query. La query è essenzialmente inattiva nello stato segnalato (con una risposta non inizializzata) in attesa di essere emessa. Al termine della query, rilasciarla come qualsiasi altra interfaccia.

## <a name="issue-a-query"></a>Eseguire una query

Un'applicazione modifica lo stato di una query emettendo una query. Di seguito è riportato un esempio di esecuzione di una query:


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Quando viene eseguita una query nello stato segnalato, la transizione sarà simile alla seguente:



| Tipo di problema                                | Transizioni di query a . . . |
|-------------------------------------------|--------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | Stato di compilazione.                |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Stato emesso.                  |



 

Quando viene eseguita una query nello stato di compilazione, la transizione sarà simile alla seguente:



| Tipo di problema                                | Transizioni di query a . . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | (Nessuna transizione, rimane nello stato di compilazione. Riavvia la parentesi quadra di query. |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Stato emesso.                                                             |



 

Una query nello stato emesso esegue una transizione simile alla seguente quando viene eseguita:



| Tipo di problema                                | Transizioni di query a . . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | Compilazione dello stato e riavvio della parentesi di query.    |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Stato rilasciato dopo l'abbandono della query esistente. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Controllare lo stato della query e ottenere la risposta alla query

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) esegue due operazioni:

1.  Restituisce lo stato della query nel codice restituito.
2.  Restituisce la risposta alla query in *pData*.

Da ognuno dei tre stati di query, ecco i [**codici restituiti GetData:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)



| Stato delle query | Codice restituito getData |
|-------------|---------------------|
| Segnalato    | S \_ OK               |
| Compilazione    | Codice di errore          |
| Rilasciato      | S \_ FALSE            |



 

Ad esempio, quando una query è nello stato emesso e la risposta alla query non è disponibile, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituisce S \_ FALSE. Quando la risorsa termina il lavoro e l'applicazione ha eseguito una fine della query, la risorsa esegue la transizione della query allo stato segnalato. Dallo stato segnalato, **GetData** restituisce S OK, il che significa che la risposta alla query viene restituita \_ anche in *pData*. Ad esempio, ecco la sequenza di eventi per restituire il numero di pixel disegnati in una sequenza di rendering:

-   Creare la query.
-   Emettere un evento begin.
-   Disegnare qualcosa.
-   Emettere un evento finale.

Di seguito è riportata la sequenza di codice corrispondente:


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



Queste righe di codice esere diverse operazioni:

-   Chiamare [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) per restituire il numero di pixel disegnati.
-   Specificare [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) per consentire alla risorsa di eseguire la transizione della query allo stato segnalato.
-   Eseguire il polling della risorsa query [**chiamando GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) da un ciclo. Se **GetData restituisce** S \_ FALSE, significa che la risorsa non ha ancora restituito la risposta.

Il valore restituito di [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) indica essenzialmente lo stato della query. I valori possibili sono S \_ OK, S \_ FALSE e un errore. Non chiamare **GetData** su una query che si trova nello stato di compilazione.

-   S \_ OK indica che la risorsa (GPU o driver o runtime) è stata completata. La query sta tornando allo stato segnalato. La risposta (se presente) viene restituita da [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).
-   S \_ FALSE indica che la risorsa (GPU, driver o runtime) non può ancora restituire una risposta. Ciò potrebbe essere dovuto al fatto che la GPU non è stata completata o non ha ancora visto il lavoro.
-   Un errore indica che la query ha generato un errore da cui non è possibile eseguire il ripristino. Questo potrebbe essere il caso in cui il dispositivo viene perso durante una query. Dopo che una query ha generato un errore (diverso da S FALSE), è necessario ricreare la query che riavvierà la sequenza di \_ query dallo stato segnalato.

Anziché specificare [**D3DGETDATA \_ FLUSH,**](d3dgetdata-flush.md)che fornisce informazioni più aggiornate, è possibile specificare zero, ovvero un controllo più leggero se la query si trova nello stato emesso. Se si specifica zero, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) non scarica il buffer dei comandi. Per questo motivo, è necessario fare attenzione per evitare cicli di infinizione (per informazioni dettagliate, vedere **GetData).** Poiché il runtime accoda il lavoro nel buffer dei comandi, **D3DGETDATA \_ FLUSH** è un meccanismo per scaricare il buffer dei comandi nel driver (e quindi la GPU; vedere [Profiling Accurate Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Durante lo scaricamento del buffer dei comandi, una query può passare allo stato segnalato.

## <a name="example-an-event-query"></a>Esempio: una query di eventi

Una query di eventi non supporta un evento begin.

-   Creare la query.
-   Emettere un evento finale.
-   Eseguire il polling fino a quando la GPU non è inattiva.
-   Emettere un evento finale.


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



Si tratta della sequenza di comandi che una query di eventi usa per profilare le chiamate API (Application Programming Interface) (Profilatura accurata delle chiamate [API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Questa sequenza usa marcatori per controllare la quantità di lavoro nel buffer dei comandi.

Si noti che le applicazioni devono prestare particolare attenzione al costo elevato associato allo scaricamento del buffer dei comandi, perché in questo modo il sistema operativo passa alla modalità kernel, causando una riduzione delle prestazioni. Le applicazioni devono anche essere consapevoli di sprecare i cicli della CPU attendendo il completamento delle query.

Le query sono un'ottimizzazione da usare durante il rendering per migliorare le prestazioni. Pertanto, non è utile dedicare tempo all'attesa del completamento di una query. Se viene eseguita una query e se i risultati non sono ancora pronti al momento in cui l'applicazione li verifica, il tentativo di ottimizzazione non ha avuto esito positivo e il rendering dovrebbe continuare come di consueto.

L'esempio classico è durante Occlusion Culling. Anziché il ciclo **while** precedente, un'applicazione che usa query può implementare l'eliminazione dell'occlusione per verificare se una query è stata completata nel momento in cui è necessario il risultato. Se la query non è stata completata, continuare (come scenario peggiore) come se l'oggetto testato non fosse occluded (ovvero è visibile) ed eseguirne il rendering. Il codice sarà simile al seguente.


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> </dl>

 

 
