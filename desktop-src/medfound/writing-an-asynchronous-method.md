---
description: Questo argomento descrive come implementare un metodo asincrono in Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Scrittura di un metodo asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2efc9b38212f729dc840dde1ad1976a1b523103312710a0f316369637f3b66d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237025"
---
# <a name="writing-an-asynchronous-method"></a>Scrittura di un metodo asincrono

Questo argomento descrive come implementare un metodo asincrono in Microsoft Media Foundation.

I metodi asincroni sono onnipresenti nella pipeline Media Foundation asincrona. I metodi asincroni semplificano la distribuzione del lavoro tra più thread. È particolarmente importante eseguire operazioni di I/O in modo asincrono, in modo che la lettura da un file o da una rete non blocchi il resto della pipeline.

Se si scrive un'origine multimediale o un sink multimediale, è fondamentale gestire correttamente le operazioni asincrone, perché le prestazioni del componente influiscono sull'intera pipeline.

> [!Note]  
> Media Foundation trasformazioni (MFT) usano metodi sincroni per impostazione predefinita.

 

### <a name="work-queues-for-asynchronous-operations"></a>Code di lavoro per operazioni asincrone

In Media Foundation esiste una relazione stretta tra i metodi [di callback](asynchronous-callback-methods.md) asincroni e le code [di lavoro.](work-queues.md) Una coda di lavoro è un'astrazione per lo spostamento del lavoro dal thread del chiamante a un thread di lavoro. Per eseguire operazioni su una coda di lavoro, eseguire le operazioni seguenti:

1.  Implementare [**l'interfaccia IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
2.  Chiamare [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) per creare un *oggetto* risultato. L'oggetto risultato espone [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult). L'oggetto risultato contiene tre puntatori:

    -   Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.
    -   Puntatore facoltativo a un oggetto stato. Se specificato, l'oggetto stato deve implementare **IUnknown**.
    -   Puntatore facoltativo a un oggetto privato. Se specificato, questo oggetto deve implementare **anche IUnknown.**

    Gli ultimi due puntatori possono essere **NULL.** In caso contrario, usarli per contenere informazioni sull'operazione asincrona.

3.  Chiamare [**MFPutWorkItemEx per**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) accodare l'elemento di lavoro.
4.  Il thread della coda di lavoro chiama il [**metodo IMFAsyncCallback::Invoke.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)
5.  Eseguire il lavoro all'interno [**del metodo Invoke.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Il *parametro pAsyncResult* di questo metodo è il [**puntatore IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) del passaggio 2. Usare questo puntatore per ottenere l'oggetto stato e l'oggetto privato:
    -   Per ottenere l'oggetto stato, chiamare [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).
    -   Per ottenere l'oggetto privato, chiamare [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).

In alternativa, è possibile combinare i passaggi 2 e 3 chiamando la [**funzione MFPutWorkItem.**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) Internamente, questa funzione chiama [**MFCreateAsyncResult per**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) creare l'oggetto risultato.

Il diagramma seguente illustra le relazioni tra il chiamante, l'oggetto risultato, l'oggetto stato e l'oggetto privato.

![Diagramma che mostra un oggetto risultato asincrono](images/workqueues01.png)

Il diagramma di sequenza seguente illustra come un oggetto accoda un elemento di lavoro. Quando il thread della coda di lavoro chiama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), l'oggetto esegue l'operazione asincrona su tale thread.

![Diagramma che mostra come un oggetto accoda un elemento di lavoro](images/workqueues02.png)

È importante ricordare che [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) viene chiamato da un thread di proprietà della coda di lavoro. L'implementazione **di Invoke** deve essere thread-safe. Inoltre, se si usa la coda di lavoro della piattaforma **(MFASYNC \_ CALLBACK \_ QUEUE \_ STANDARD),** è fondamentale non bloccare mai il thread, perché ciò può impedire all'intera pipeline Media Foundation di elaborare i dati. Se è necessario eseguire un'operazione che blocchi o richiedere molto tempo, usare una coda di lavoro privata. Per creare una coda di lavoro privata, chiamare [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Qualsiasi componente della pipeline che esegue operazioni di I/O deve evitare di bloccare le chiamate di I/O per lo stesso motivo. [**L'interfaccia IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) fornisce un'astrazione utile per l'I/O di file asincrono.

### <a name="implementing-the-beginend-pattern"></a>Implementazione di Begin.../End... Modello

Come descritto in [Chiamata di metodi asincroni,](calling-asynchronous-methods.md)i metodi asincroni in Media Foundation usano spesso **Begin...** / **End....** Modello. In questo modello, un'operazione asincrona usa due metodi con firme simili ai seguenti:

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Per rendere il metodo realmente asincrono, l'implementazione di **BeginX** deve eseguire il lavoro effettivo su un altro thread. È qui che le code di lavoro vengono all'interno dell'immagine. Nei passaggi seguenti, il *chiamante è* il codice che chiama **BeginX** ed **EndX**. Potrebbe trattarsi di un'applicazione o Media Foundation pipeline. Il *componente* è il codice che implementa **BeginX** ed **EndX**.

1.  Il chiamante **chiama Begin...**, passando un puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.
2.  Il componente crea un nuovo oggetto risultato asincrono. Questo oggetto archivia l'interfaccia di callback e l'oggetto stato del chiamante. In genere, archivia anche le informazioni sullo stato privato necessarie al componente per completare l'operazione. L'oggetto risultato di questo passaggio è etichettato come "Risultato 1" nel diagramma successivo.
3.  Il componente crea un secondo oggetto risultato. Questo oggetto risultato archivia due puntatori: il primo oggetto risultato e l'interfaccia di callback del chiamato. Questo oggetto risultato è etichettato come "Risultato 2" nel diagramma successivo.
4.  Il componente chiama [**MFPutWorkItemEx per**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) accodare un nuovo elemento di lavoro.
5.  Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) il componente esegue il lavoro asincrono.
6.  Il componente chiama [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) per richiamare il metodo di callback del chiamante.
7.  Il chiamante chiama il **metodo EndX.**

![Diagramma che illustra come un oggetto implementa il modello begin/end](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Esempio di metodo asincrono

Per illustrare questa discussione, verrà utilizzato un esempio contrived. Si consideri un metodo asincrono per il calcolo di una radice quadrata:


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



Il *parametro x* di è il valore di cui verrà calcolata la radice `BeginSquareRoot` quadrata. La radice quadrata viene restituita nel *parametro pVal* di `EndSquareRoot` .

Ecco la dichiarazione di una classe che implementa questi due metodi:


```C++
class SqrRoot : public IMFAsyncCallback
{
    LONG    m_cRef;
    double  m_sqrt;

    HRESULT DoCalculateSquareRoot(AsyncOp *pOp);

public:

    SqrRoot() : m_cRef(1)
    {

    }

    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(SqrRoot, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    // IMFAsyncCallback methods.

    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;  
    }
    // Invoke is where the work is performed.
    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



La `SqrRoot` classe implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) in modo che possa inserire l'operazione radice quadrata in una coda di lavoro. Il `DoCalculateSquareRoot` metodo è il metodo della classe privata che calcola la radice quadrata. Questo metodo verrà chiamato dal thread della coda di lavoro.

Prima di tutto, è necessario un modo per archiviare il valore di *x*, in modo che possa essere recuperato quando il thread della coda di lavoro chiama `SqrRoot::Invoke` . Ecco una semplice classe che archivia le informazioni:


```C++
class AsyncOp : public IUnknown
{
    LONG    m_cRef;

public:

    double  m_value;

    AsyncOp(double val) : m_cRef(1), m_value(val) { }

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(AsyncOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



Questa classe implementa **IUnknown** in modo che possa essere archiviata in un oggetto risultato.

Il codice seguente implementa il `BeginSquareRoot` metodo :


```C++
HRESULT SqrRoot::BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState)
{
    AsyncOp *pOp = new (std::nothrow) AsyncOp(x);
    if (pOp == NULL)
    {
        return E_OUTOFMEMORY;
    }

    IMFAsyncResult *pResult = NULL;

    // Create the inner result object. This object contains pointers to:
    // 
    //   1. The caller's callback interface and state object. 
    //   2. The AsyncOp object, which contains the operation data.
    //

    HRESULT hr = MFCreateAsyncResult(pOp, pCB, pState, &pResult);

    if (SUCCEEDED(hr))
    {
        // Queue a work item. The work item contains pointers to:
        // 
        // 1. The callback interface of the SqrRoot object.
        // 2. The inner result object.

        hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_STANDARD, this, pResult);

        pResult->Release();
    }

    return hr;
}
```



Il codice esegue le attività seguenti:

1.  Crea una nuova istanza della `AsyncOp` classe per contenere il valore di *x*.
2.  Chiama [**MFCreateAsyncResult per**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) creare un oggetto risultato. Questo oggetto contiene diversi puntatori:
    -   Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.
    -   Puntatore all'oggetto stato del chiamante (*pState*).
    -   Puntatore all'oggetto `AsyncOp`.
3.  Chiama [**MFPutWorkItem per**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) accodare un nuovo elemento di lavoro. Questa chiamata crea in modo implicito un oggetto risultato esterno, che contiene i puntatori seguenti:
    -   Puntatore `SqrRoot` all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dell'oggetto.
    -   Puntatore all'oggetto risultato interno del passaggio 2.

Il codice seguente implementa il `SqrRoot::Invoke` metodo :


```C++
// Invoke is called by the work queue. This is where the object performs the
// asynchronous operation.

STDMETHODIMP SqrRoot::Invoke(IMFAsyncResult* pResult)
{
    HRESULT hr = S_OK;

    IUnknown *pState = NULL;
    IUnknown *pUnk = NULL;
    IMFAsyncResult *pCallerResult = NULL;

    AsyncOp *pOp = NULL; 

    // Get the asynchronous result object for the application callback. 

    hr = pResult->GetState(&pState);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pState->QueryInterface(IID_PPV_ARGS(&pCallerResult));
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the object that holds the state information for the asynchronous method.
    hr = pCallerResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    pOp = static_cast<AsyncOp*>(pUnk);

    // Do the work.

    hr = DoCalculateSquareRoot(pOp);

done:
    // Signal the application.
    if (pCallerResult)
    {
        pCallerResult->SetStatus(hr);
        MFInvokeCallback(pCallerResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pUnk);
    SafeRelease(&pCallerResult);
    return S_OK;
}
```



Questo metodo ottiene l'oggetto risultato interno e `AsyncOp` l'oggetto . Quindi passa `AsyncOp` l'oggetto a `DoCalculateSquareRoot` . Infine, chiama [**IMFAsyncResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) per impostare il codice di stato e [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) per richiamare il metodo di callback del chiamante.

Il `DoCalculateSquareRoot` metodo esegue esattamente ciò che ci si aspetterebbe:


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Quando viene richiamato il metodo di callback del chiamante, è responsabilità del chiamante chiamare il metodo **End...** in questo caso, `EndSquareRoot` . è `EndSquareRoot` il modo in cui il chiamante recupera il risultato dell'operazione asincrona, che in questo esempio è la radice quadrata calcolata. Queste informazioni vengono archiviate nell'oggetto risultato:


```C++
HRESULT SqrRoot::EndSquareRoot(IMFAsyncResult *pResult, double *pVal)
{
    *pVal = 0;

    IUnknown *pUnk = NULL;

    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    AsyncOp *pOp = static_cast<AsyncOp*>(pUnk);

    // Get the result.
    *pVal = pOp->m_value;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="operation-queues"></a>Code di operazioni

Finora si è ritenuto che un'operazione asincrona possa essere eseguita in qualsiasi momento, indipendentemente dallo stato corrente dell'oggetto. Si consideri ad esempio cosa accade se un'applicazione chiama mentre una chiamata `BeginSquareRoot` precedente allo stesso metodo è ancora in sospeso. La `SqrRoot` classe potrebbe accodato il nuovo elemento di lavoro prima che venga eseguito l'elemento di lavoro precedente. Tuttavia, non è garantito che le code di lavoro serializzano gli elementi di lavoro. Tenere presenti che una coda di lavoro può usare più thread per inviare elementi di lavoro. In un ambiente multithreading un elemento di lavoro potrebbe essere richiamato prima del completamento di quello precedente. Gli elementi di lavoro possono anche essere richiamati in ordine, se si verifica un cambio di contesto poco prima che venga richiamato il callback.

Per questo motivo, è responsabilità dell'oggetto serializzare le operazioni su se stesso, se necessario. In altre parole, se l'oggetto richiede il completamento dell'operazione *A* prima dell'avvio dell'operazione *B,* l'oggetto non deve accodare un elemento di lavoro per *B* fino al completamento dell'operazione *A.* Un oggetto può soddisfare questo requisito con una propria coda di operazioni in sospeso. Quando viene chiamato un metodo asincrono sull'oggetto , l'oggetto inserisce la richiesta nella propria coda. Al termine di ogni operazione asincrona, l'oggetto esegue il pull della richiesta successiva dalla coda. [L'esempio MPEG1Source](mpeg1source-sample.md) mostra un esempio di come implementare una coda di questo tipo.

Un singolo metodo può comportare diverse operazioni asincrone, in particolare quando vengono usate chiamate di I/O. Quando si implementano metodi asincroni, considerare attentamente i requisiti di serializzazione. Ad esempio, è valido per l'oggetto avviare una nuova operazione mentre una richiesta di I/O precedente è ancora in sospeso? Se la nuova operazione modifica lo stato interno dell'oggetto, cosa accade quando una richiesta di I/O precedente viene completata e restituisce dati che potrebbero ora essere obsoleti? Un diagramma di stato valido può essere utile per identificare le transizioni di stato valide.

## <a name="cross-thread-and-cross-process-considerations"></a>Considerazioni su cross-thread e cross-process

Le code di lavoro non usano il marshalling COM per effettuare il marshalling dei puntatori a interfaccia attraverso i limiti dei thread. Pertanto, anche se un oggetto è registrato come apartment-threaded o il thread dell'applicazione è stato inserito in un apartment a thread singolo (STA), i callback [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) verranno richiamati da un thread diverso. In ogni caso, tutti Media Foundation componenti della pipeline devono usare il modello di threading "Both".

Alcune interfacce in Media Foundation definire versioni remote di alcuni metodi asincroni. Quando uno di questi metodi viene chiamato oltre i limiti del processo, la DLL proxy/stub Media Foundation chiama la versione remota del metodo, che esegue il marshalling personalizzato dei parametri del metodo. Nel processo remoto, lo stub converte la chiamata nel metodo locale sull'oggetto . Questo processo è trasparente sia per l'applicazione che per l'oggetto remoto. Questi metodi di marshalling personalizzati vengono forniti principalmente per gli oggetti caricati nel percorso del supporto protetto (PMP). Per altre informazioni sul PMP, vedere [Percorso supporto protetto](protected-media-path.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metodi di callback asincroni](asynchronous-callback-methods.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> </dl>

 

 



