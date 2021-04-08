---
description: Sono disponibili diversi tipi di query progettati per eseguire query sullo stato delle risorse.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Query (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875961"
---
# <a name="queries-direct3d-9"></a>Query (Direct3D 9)

Sono disponibili diversi tipi di query progettati per eseguire query sullo stato delle risorse. Lo stato di una determinata risorsa include lo stato della GPU (Graphics Processing Unit), lo stato del driver o lo stato di Runtime. Per comprendere la differenza tra i diversi tipi di query, è necessario comprendere gli Stati della query. Il diagramma di transizione di stato seguente illustra ogni stato della query.

![diagramma che mostra le transizioni tra gli Stati di query](images/queries.png)

Il diagramma mostra tre stati, ognuno definito da cerchi. Ognuna delle linee continue è costituita da eventi basati su applicazioni che provocano una transizione di stato. La linea tratteggiata è un evento basato sulle risorse che passa una query dallo stato emesso allo stato segnalato. Ognuno di questi Stati ha uno scopo diverso:

-   Lo stato segnalato è come uno stato inattivo. L'oggetto query è stato generato ed è in attesa del rilascio della query da parte dell'applicazione. Una volta completata la query e la transizione allo stato segnalato, è possibile recuperare la risposta alla query.
-   Lo stato di compilazione è analogo a un'area di gestione temporanea di una query. Dallo stato di compilazione è stata eseguita una query (chiamando [**\_ Begin D3DISSUE**](d3dissue-begin.md)) ma non è ancora stata eseguita la transizione allo stato emesso. Quando un'applicazione invia una query end (chiamando [**D3DISSUE \_ end**](d3dissue-end.md)), la query esegue la transizione allo stato emesso.
-   Lo stato emesso indica che la risorsa sottoposta a query ha il controllo della query. Al termine del lavoro della risorsa, la risorsa esegue la transizione della macchina a stati verso lo stato segnalato. Durante lo stato emesso, l'applicazione deve eseguire il polling per rilevare la transizione allo stato segnalato. Una volta eseguita la transizione allo stato segnalato, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituisce il risultato della query (tramite un argomento) all'applicazione.

Nella tabella seguente sono elencati i tipi di query disponibili.



| Tipo di query        | Evento Issue                                                                      | Buffer GetData                                                              | Runtime      | Inizio implicito della query                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| BANDWIDTHTIMINGS  | [**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md) | [**\_D3D9BANDWIDTHTIMINGS D3DDEVINFO**](d3ddevinfo-d3d9bandwidthtimings.md) | Vendita al dettaglio/debug | N/D                                              |
| CACHEUTILIZATION  | [**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md) | [**\_D3D9CACHEUTILIZATION D3DDEVINFO**](d3ddevinfo-d3d9cacheutilization.md) | Vendita al dettaglio/debug | N/D                                              |
| EVENTO             | [**\_Fine D3DISSUE**](d3dissue-end.md)                                            | BOOL                                                                        | Vendita al dettaglio/debug | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| INTERFACETIMINGS  | [**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md) | [**\_D3D9INTERFACETIMINGS D3DDEVINFO**](d3ddevinfo-d3d9interfacetimings.md) | Vendita al dettaglio/debug | N/D                                              |
| OCCLUSIONE         | [**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md) | DWORD                                                                       | Vendita al dettaglio/debug | N/D                                              |
| PIPELINETIMINGS   | [**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md) | [**\_D3D9PIPELINETIMINGS D3DDEVINFO**](d3ddevinfo-d3d9pipelinetimings.md)   | Vendita al dettaglio/debug | N/D                                              |
| RESOURCEMANAGER   | [**\_Fine D3DISSUE**](d3dissue-end.md)                                            | [**\_RESOURCEMANAGER D3DDEVINFO**](d3ddevinfo-resourcemanager.md)           | Solo debug   | [**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**\_Fine D3DISSUE**](d3dissue-end.md)                                            | UINT64                                                                      | Vendita al dettaglio/debug | N/D                                              |
| TIMESTAMPDISJOINT | [**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md) | BOOL                                                                        | Vendita al dettaglio/debug | N/D                                              |
| TIMESTAMPFREQ     | [**\_Fine D3DISSUE**](d3dissue-end.md)                                            | UINT64                                                                      | Vendita al dettaglio/debug | N/D                                              |
| VCACHE            | [**\_Fine D3DISSUE**](d3dissue-end.md)                                            | [**\_VCACHE D3DDEVINFO**](d3ddevinfo-vcache.md)                             | Vendita al dettaglio/debug | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| VERTEXSTATS       | [**\_Fine D3DISSUE**](d3dissue-end.md)                                            | [**\_D3DVERTEXSTATS D3DDEVINFO**](d3ddevinfo-d3dvertexstats.md)             | Solo debug   | [**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| VERTEXTIMINGS     | [**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md) | [**\_D3D9STAGETIMINGS D3DDEVINFO**](d3ddevinfo-d3d9stagetimings.md)         | Vendita al dettaglio/debug | N/D                                              |



 

Alcune query richiedono un evento Begin e end, mentre altre richiedono solo un evento End. Le query che richiedono solo un evento End iniziano quando si verifica un altro evento implicito, elencato nella tabella. Tutte le query restituiscono una risposta, ad eccezione della query di eventi la cui risposta è sempre **true**. Un'applicazione utilizza lo stato della query o il codice restituito di [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Creare una query

Prima di creare una query, è possibile verificare se il runtime supporta le query chiamando [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) con un puntatore **null** analogo al seguente:


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Questo metodo restituisce un codice di esito positivo se è possibile creare una query. in caso contrario, restituisce un codice di errore. Quando [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) ha esito positivo, è possibile creare un oggetto query analogo al seguente:


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Se la chiamata ha esito positivo, viene creato un oggetto query. La query è essenzialmente inattiva nello stato segnalato (con una risposta non inizializzata) in attesa di essere rilasciata. Una volta completata la query, rilasciarla come qualsiasi altra interfaccia.

## <a name="issue-a-query"></a>Eseguire una query

Un'applicazione modifica lo stato di una query eseguendo una query. Di seguito è riportato un esempio di esecuzione di una query:


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Una query nello stato segnalato verrà transizione come questa quando viene eseguita:



| Tipo di problema                                | Esegue una query sulle transizioni a. . . |
|-------------------------------------------|--------------------------------|
| [**\_Inizio D3DISSUE**](d3dissue-begin.md) | Stato di compilazione.                |
| [**\_Fine D3DISSUE**](d3dissue-end.md)     | Stato emesso.                  |



 

Una query nello stato di compilazione eseguirà la transizione come questa quando viene eseguita:



| Tipo di problema                                | Esegue una query sulle transizioni a. . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**\_Inizio D3DISSUE**](d3dissue-begin.md) | (Nessuna transizione, rimane nello stato di compilazione. Riavvia la parentesi della query. |
| [**\_Fine D3DISSUE**](d3dissue-end.md)     | Stato emesso.                                                             |



 

Una query nello stato emesso verrà transizione come questa quando viene eseguita:



| Tipo di problema                                | Esegue una query sulle transizioni a. . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**\_Inizio D3DISSUE**](d3dissue-begin.md) | Compilazione dello stato e riavvio della parentesi di query.    |
| [**\_Fine D3DISSUE**](d3dissue-end.md)     | Stato emesso dopo l'abbandono della query esistente. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Controllare lo stato della query e ottenere la risposta alla query

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) esegue due operazioni:

1.  Restituisce lo stato della query nel codice restituito.
2.  Restituisce la risposta alla query in *pData*.

Da ognuno dei tre stati di query, di seguito sono riportati i codici restituiti [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :



| Stato delle query | Codice restituito GetData |
|-------------|---------------------|
| Segnalato    | \_OK               |
| Compilazione    | Codice di errore          |
| Rilasciato      | S \_ false            |



 

Ad esempio, quando una query è nello stato emesso e la risposta alla query non è disponibile, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituisce S \_ false. Quando la risorsa termina il lavoro e l'applicazione ha emesso una query end, la risorsa esegue la transizione della query allo stato segnalato. Dallo stato segnalato, **GetData** restituisce S OK, \_ il che significa che la risposta alla query viene restituita anche in *pData*. Ad esempio, di seguito è illustrata la sequenza di eventi per restituire il numero di pixel disegnati in una sequenza di rendering:

-   Creare la query.
-   Rilascia un evento Begin.
-   Creare qualcosa.
-   Eseguire un evento di fine.

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



Queste righe di codice eseguono diverse operazioni:

-   Chiamare [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) per restituire il numero di pixel disegnati.
-   Specificare [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md) per consentire alla risorsa di eseguire la transizione della query allo stato segnalato.
-   Eseguire il polling della risorsa di query chiamando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) da un ciclo. Fino a quando **GetData** restituisce \_ false, significa che la risorsa non ha ancora restituito la risposta.

Il valore restituito da [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) indica essenzialmente lo stato della query. I valori possibili sono S \_ OK, s \_ false e un errore. Non chiamare **GetData** per una query che si trova nello stato di compilazione.

-   S \_ OK indica che la risorsa (GPU, driver o Runtime) è stata completata. La query viene restituita allo stato segnalato. La risposta, se presente, viene restituita da [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).
-   S \_ false significa che la risorsa (GPU, driver o Runtime) non può restituire ancora una risposta. Il problema potrebbe essere dovuto al fatto che la GPU non è stata completata o non ha ancora visto il lavoro.
-   Un errore indica che la query ha generato un errore dal quale non è possibile eseguire il ripristino. Questa situazione può verificarsi se il dispositivo viene perso durante una query. Una volta che una query ha generato un errore \_ , ad eccezione di false, è necessario ricreare la query che riavvierà la sequenza di query dallo stato segnalato.

Anziché specificare [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md), che fornisce informazioni più aggiornate, è possibile fornire zero, ovvero un controllo più leggero se la query è nello stato emesso. Se si specifica zero, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) non Scarica il buffer dei comandi. Per questo motivo, è necessario prestare attenzione per evitare i cicli infinate (vedere **GetData** per informazioni dettagliate). Poiché il runtime Accoda il lavoro nel buffer dei comandi, lo **\_ scaricamento di D3DGETDATA** è un meccanismo per scaricare il buffer dei comandi al driver e, di conseguenza, la GPU; vedere [profilatura accurata delle chiamate API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md). Durante lo scaricamento del buffer dei comandi, una query può passare allo stato segnalato.

## <a name="example-an-event-query"></a>Esempio: una query di eventi

Una query di eventi non supporta un evento Begin.

-   Creare la query.
-   Eseguire un evento di fine.
-   Eseguire il polling finché la GPU non è inattiva.
-   Eseguire un evento di fine.


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



Questa è la sequenza dei comandi usati da una query di eventi per profilare le chiamate di Application Programming Interface (API) (vedere [profilatura accurata delle chiamate API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md). Questa sequenza usa i marcatori per controllare la quantità di lavoro nel buffer dei comandi.

Si noti che le applicazioni devono prestare particolare attenzione al costo elevato associato allo scaricamento del buffer dei comandi, in quanto in questo modo il sistema operativo passa alla modalità kernel, causando così una notevole riduzione delle prestazioni. Le applicazioni devono inoltre tenere presente che gli sprechi di cicli della CPU attendono il completamento delle query.

Le query sono un'ottimizzazione da utilizzare durante il rendering per migliorare le prestazioni. Pertanto, non è vantaggioso dedicare tempo in attesa del completamento di una query. Se viene eseguita una query e se i risultati non sono ancora pronti nel momento in cui l'applicazione li controlla, il tentativo di ottimizzazione non riesce e il rendering dovrebbe continuare normalmente.

L'esempio classico è l'abbattimento dell'occlusione. Anziché il ciclo **while** precedente, un'applicazione che usa le query può implementare l'abbattimento dell'occlusione per verificare se una query è stata completata in base al tempo necessario per il risultato. Se la query non è stata completata, continuare (come scenario peggiore) come se l'oggetto sottoposto a test non fosse nascosto (ovvero è visibile) ed eseguirne il rendering. Il codice avrà un aspetto simile al seguente.


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

 

 
