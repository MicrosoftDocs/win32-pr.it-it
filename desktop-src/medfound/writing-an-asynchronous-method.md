---
description: In questo argomento viene descritto come implementare un metodo asincrono in Microsoft Media Foundation.
ms.assetid: cd94280d-7267-4d35-8333-aa4a5bd81b73
title: Scrittura di un metodo asincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d8360d0c15fe25661b8cd0f0f5adc9768db8ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348236"
---
# <a name="writing-an-asynchronous-method"></a>Scrittura di un metodo asincrono

In questo argomento viene descritto come implementare un metodo asincrono in Microsoft Media Foundation.

I metodi asincroni sono universali nella pipeline Media Foundation. I metodi asincroni semplificano la distribuzione del lavoro tra più thread. È particolarmente importante eseguire l'I/O in modo asincrono, in modo che la lettura da un file o da una rete non blocchi il resto della pipeline.

Se si scrive un'origine multimediale o un sink multimediale, è fondamentale gestire correttamente le operazioni asincrone, perché le prestazioni del componente incidono sull'intera pipeline.

> [!Note]  
> Per impostazione predefinita, le trasformazioni Media Foundation (MFTs) utilizzano metodi sincroni.

 

### <a name="work-queues-for-asynchronous-operations"></a>Code di lavoro per le operazioni asincrone

In Media Foundation, esiste una relazione di chiusura tra i [metodi di callback asincrono](asynchronous-callback-methods.md) e le [code di lavoro](work-queues.md). Una coda di lavoro è un'astrazione per lo trasferimento di lavoro dal thread del chiamante a un thread di lavoro. Per eseguire operazioni su una coda di lavoro, eseguire le operazioni seguenti:

1.  Implementare l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
2.  Chiamare [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) per creare un oggetto *risultato* . L'oggetto risultato espone [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult). L'oggetto risultato contiene tre puntatori:

    -   Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.
    -   Puntatore facoltativo a un oggetto di stato. Se specificato, l'oggetto di stato deve implementare **IUnknown**.
    -   Puntatore facoltativo a un oggetto privato. Se specificato, questo oggetto deve implementare anche **IUnknown**.

    Gli ultimi due puntatori possono essere **null**. In caso contrario, utilizzarli per conservare informazioni sull'operazione asincrona.

3.  Chiamare [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) per accodare l'elemento di lavoro.
4.  Il thread della coda di lavoro chiama il metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .
5.  Eseguire l'operazione all'interno del metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Il parametro *pAsyncResult* di questo metodo è il puntatore [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) del passaggio 2. Utilizzare questo puntatore per ottenere l'oggetto di stato e l'oggetto privato:
    -   Per ottenere l'oggetto di stato, chiamare [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).
    -   Per ottenere l'oggetto privato, chiamare [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).

In alternativa, è possibile combinare i passaggi 2 e 3 chiamando la funzione [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) . Internamente, questa funzione chiama [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) per creare l'oggetto risultato.

Il diagramma seguente illustra le relazioni tra il chiamante, l'oggetto risultato, l'oggetto stato e l'oggetto privato.

![diagramma che mostra un oggetto risultato asincrono](images/workqueues01.png)

Il diagramma di sequenza seguente illustra il modo in cui un oggetto Accoda un elemento di lavoro. Quando il thread della coda di lavoro chiama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), l'oggetto esegue l'operazione asincrona su tale thread.

![diagramma che illustra il modo in cui un oggetto Accoda un elemento di lavoro](images/workqueues02.png)

È importante ricordare che [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) viene chiamato da un thread di proprietà della coda di lavoro. L'implementazione di **Invoke** deve essere thread-safe. Inoltre, se si usa la coda di lavoro della piattaforma (**MFASYNC \_ callback \_ Queue \_ standard**), è fondamentale che non si blocchi mai il thread, perché ciò può bloccare l'intera pipeline Media Foundation dall'elaborazione dei dati. Se è necessario eseguire un'operazione che blocca o richiede molto tempo per il completamento, utilizzare una coda di lavoro privata. Per creare una coda di lavoro privata, chiamare [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Qualsiasi componente della pipeline che esegue operazioni di I/O deve evitare il blocco delle chiamate di I/O per lo stesso motivo. L'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) fornisce un'astrazione utile per l'I/O di file asincrono.

### <a name="implementing-the-beginend-pattern"></a>Implementazione di Begin. ../end... Modello

Come descritto in [chiamata di metodi asincroni](calling-asynchronous-methods.md), i metodi asincroni in Media Foundation spesso usano il metodo **Begin...** / **Fine.** .. modello. In questo modello, un'operazione asincrona utilizza due metodi con firme simili alle seguenti:

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

Per rendere il metodo realmente asincrono, l'implementazione di **BeginX** deve eseguire il lavoro effettivo su un altro thread. Questo è il punto in cui le code di lavoro entrano nell'immagine. Nei passaggi successivi, il *chiamante* è il codice che chiama **BeginX** e **EndX**. Potrebbe trattarsi di un'applicazione o della pipeline Media Foundation. Il *componente* è il codice che implementa **BeginX** e **EndX**.

1.  Il chiamante chiama **Begin...**, passando un puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.
2.  Il componente crea un nuovo oggetto risultato asincrono. Questo oggetto archivia l'interfaccia di callback del chiamante e l'oggetto di stato. In genere, archivia anche le informazioni sullo stato privato necessarie al componente per completare l'operazione. L'oggetto risultato di questo passaggio è denominato "risultato 1" nel diagramma successivo.
3.  Il componente crea un secondo oggetto risultato. Questo oggetto risultato archivia due puntatori: il primo oggetto risultato e l'interfaccia di callback del chiamato. Questo oggetto risultato è denominato "result 2" nel diagramma successivo.
4.  Il componente chiama [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) per accodare un nuovo elemento di lavoro.
5.  Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) il componente esegue l'operazione asincrona.
6.  Il componente chiama [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) per richiamare il metodo di callback del chiamante.
7.  Il chiamante chiama il metodo **EndX** .

![diagramma che illustra il modo in cui un oggetto implementa il modello Begin/End](images/workqueues03.png)

## <a name="asynchronous-method-example"></a>Esempio di metodo asincrono

Per illustrare questa discussione, verrà usato un esempio artificioso. Si consideri un metodo asincrono per il calcolo di una radice quadrata:


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



Il parametro *x* di `BeginSquareRoot` è il valore di cui verrà calcolata la radice quadrata. La radice quadrata viene restituita nel parametro *pval* di `EndSquareRoot` .

Di seguito è illustrata la dichiarazione di una classe che implementa i due metodi seguenti:


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

Per prima cosa, è necessario un modo per archiviare il valore di *x*, in modo che possa essere recuperato durante la chiamata del thread della coda di lavoro `SqrRoot::Invoke` . Ecco una semplice classe che archivia le informazioni:


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

Il codice seguente implementa il `BeginSquareRoot` Metodo:


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

1.  Crea una nuova istanza della `AsyncOp` classe per mantenere il valore di *x*.
2.  Chiama [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) per creare un oggetto risultato. Questo oggetto include diversi puntatori:
    -   Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.
    -   Puntatore all'oggetto di stato del chiamante (*pState*).
    -   Puntatore all'oggetto `AsyncOp`.
3.  Chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) per accodare un nuovo elemento di lavoro. Questa chiamata crea in modo implicito un oggetto risultato esterno, che contiene i puntatori seguenti:
    -   Puntatore all' `SqrRoot` interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dell'oggetto.
    -   Puntatore all'oggetto risultato interno del passaggio 2.

Il codice seguente implementa il `SqrRoot::Invoke` Metodo:


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



Questo metodo ottiene l'oggetto risultato interno e l' `AsyncOp` oggetto. Quindi passa l' `AsyncOp` oggetto a `DoCalculateSquareRoot` . Infine, viene chiamato [**IMFAsyncResult:: sestatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) per impostare il codice di stato e [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) per richiamare il metodo di callback del chiamante.

Il `DoCalculateSquareRoot` metodo esegue esattamente ciò che ci si aspetta:


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



Quando viene richiamato il metodo di callback del chiamante, è responsabilità del chiamante chiamare il metodo **end...** , in questo caso `EndSquareRoot` . `EndSquareRoot`È il modo in cui il chiamante Recupera il risultato dell'operazione asincrona, che in questo esempio è la radice quadrata calcolata. Queste informazioni vengono archiviate nell'oggetto risultato:


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



## <a name="operation-queues"></a>Code operazioni

Fino a questo punto, si presuppone che un'operazione asincrona possa essere eseguita in qualsiasi momento, indipendentemente dallo stato corrente dell'oggetto. Si consideri, ad esempio, cosa accade se un'applicazione chiama `BeginSquareRoot` mentre una chiamata precedente allo stesso metodo è ancora in sospeso. La `SqrRoot` classe potrebbe accodare il nuovo elemento di lavoro prima di eseguire l'elemento di lavoro precedente. Tuttavia, le code di lavoro non garantiscono la serializzazione degli elementi di lavoro. Tenere presente che una coda di lavoro può usare più di un thread per inviare elementi di lavoro. In un ambiente con multithreading, un elemento di lavoro potrebbe essere richiamato prima del completamento di quello precedente. Gli elementi di lavoro possono anche essere richiamati in modo non corretto, se si verifica un cambio di contesto immediatamente prima che venga richiamato il callback.

Per questo motivo, è responsabilità dell'oggetto serializzare le operazioni su se stesso, se necessario. In altre parole, se l'oggetto *richiede che l'operazione a venga* completata prima che l'operazione *b* possa essere avviata, l'oggetto non deve accodare un elemento di lavoro per *B* fino al completamento dell'operazione *a* . Un oggetto può soddisfare questo requisito con una propria coda di operazioni in sospeso. Quando un metodo asincrono viene chiamato sull'oggetto, l'oggetto inserisce la richiesta nella propria coda. Quando ogni operazione asincrona viene completata, l'oggetto esegue il pull della richiesta successiva dalla coda. Nell' [esempio MPEG1Source](mpeg1source-sample.md) viene illustrato un esempio di come implementare una coda di questo tipo.

Un singolo metodo può coinvolgere diverse operazioni asincrone, in particolare quando vengono utilizzate chiamate di I/O. Quando si implementano metodi asincroni, valutare con attenzione i requisiti di serializzazione. Ad esempio, è possibile che l'oggetto avvii una nuova operazione mentre una richiesta di I/O precedente è ancora in sospeso? Se la nuova operazione modifica lo stato interno dell'oggetto, cosa accade quando una richiesta di I/O precedente viene completata e restituisce dati che potrebbero essere obsoleti? Un diagramma di stato valido può aiutare a identificare le transizioni di stato valide.

## <a name="cross-thread-and-cross-process-considerations"></a>Considerazioni tra thread e tra processi

Le code di lavoro non utilizzano il marshalling COM per eseguire il marshalling di puntatori a interfaccia tra i limiti dei thread. Pertanto, anche se un oggetto viene registrato come thread-apartment o il thread dell'applicazione è entrato in un Apartment a thread singolo, i callback [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) verranno richiamati da un thread diverso. In ogni caso, tutti i componenti della pipeline Media Foundation devono usare il modello di threading "both".

Alcune interfacce in Media Foundation definiscono versioni remote di alcuni metodi asincroni. Quando uno di questi metodi viene chiamato tra i limiti del processo, la DLL Media Foundation Proxy/Stub chiama la versione remota del metodo, che esegue il marshalling personalizzato dei parametri del metodo. Nel processo remoto lo stub converte la chiamata nel metodo locale nell'oggetto. Questo processo è trasparente per l'applicazione e l'oggetto remoto. Questi metodi di marshalling personalizzati vengono forniti principalmente per gli oggetti caricati nel percorso multimediale protetto (PMP). Per ulteriori informazioni su PMP, vedere il [percorso multimediale protetto](protected-media-path.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metodi di callback asincroni](asynchronous-callback-methods.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> </dl>

 

 



