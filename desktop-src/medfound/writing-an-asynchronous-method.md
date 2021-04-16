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
# <a name="writing-an-asynchronous-method"></a><span data-ttu-id="8cc07-103">Scrittura di un metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="8cc07-103">Writing an Asynchronous Method</span></span>

<span data-ttu-id="8cc07-104">In questo argomento viene descritto come implementare un metodo asincrono in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8cc07-104">This topic describes how to implement an asynchronous method in Microsoft Media Foundation.</span></span>

<span data-ttu-id="8cc07-105">I metodi asincroni sono universali nella pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8cc07-105">Asynchronous methods are ubiquitous in the Media Foundation pipeline.</span></span> <span data-ttu-id="8cc07-106">I metodi asincroni semplificano la distribuzione del lavoro tra più thread.</span><span class="sxs-lookup"><span data-stu-id="8cc07-106">Asynchronous methods make it easier to distribute work among several threads.</span></span> <span data-ttu-id="8cc07-107">È particolarmente importante eseguire l'I/O in modo asincrono, in modo che la lettura da un file o da una rete non blocchi il resto della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8cc07-107">It is particularly important to perform I/O asynchronously, so that reading from a file or network does not block the rest of the pipeline.</span></span>

<span data-ttu-id="8cc07-108">Se si scrive un'origine multimediale o un sink multimediale, è fondamentale gestire correttamente le operazioni asincrone, perché le prestazioni del componente incidono sull'intera pipeline.</span><span class="sxs-lookup"><span data-stu-id="8cc07-108">If you are writing a media source or media sink, it is crucial to handle asynchronous operations correctly, because your component's performance has an impact on the entire pipeline.</span></span>

> [!Note]  
> <span data-ttu-id="8cc07-109">Per impostazione predefinita, le trasformazioni Media Foundation (MFTs) utilizzano metodi sincroni.</span><span class="sxs-lookup"><span data-stu-id="8cc07-109">Media Foundation transforms (MFTs) use synchronous methods by default.</span></span>

 

### <a name="work-queues-for-asynchronous-operations"></a><span data-ttu-id="8cc07-110">Code di lavoro per le operazioni asincrone</span><span class="sxs-lookup"><span data-stu-id="8cc07-110">Work Queues For Asynchronous Operations</span></span>

<span data-ttu-id="8cc07-111">In Media Foundation, esiste una relazione di chiusura tra i [metodi di callback asincrono](asynchronous-callback-methods.md) e le [code di lavoro](work-queues.md).</span><span class="sxs-lookup"><span data-stu-id="8cc07-111">In Media Foundation, there is a close relationship between [Asynchronous Callback Methods](asynchronous-callback-methods.md) and [Work Queues](work-queues.md).</span></span> <span data-ttu-id="8cc07-112">Una coda di lavoro è un'astrazione per lo trasferimento di lavoro dal thread del chiamante a un thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-112">A work queue is an abstraction for moving work from the caller's thread to a worker thread.</span></span> <span data-ttu-id="8cc07-113">Per eseguire operazioni su una coda di lavoro, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc07-113">To perform work on a work queue, do the following:</span></span>

1.  <span data-ttu-id="8cc07-114">Implementare l'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="8cc07-114">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="8cc07-115">Chiamare [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) per creare un oggetto *risultato* .</span><span class="sxs-lookup"><span data-stu-id="8cc07-115">Call [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a *result* object.</span></span> <span data-ttu-id="8cc07-116">L'oggetto risultato espone [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span><span class="sxs-lookup"><span data-stu-id="8cc07-116">The result object exposes the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult).</span></span> <span data-ttu-id="8cc07-117">L'oggetto risultato contiene tre puntatori:</span><span class="sxs-lookup"><span data-stu-id="8cc07-117">The result object contains three pointers:</span></span>

    -   <span data-ttu-id="8cc07-118">Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.</span><span class="sxs-lookup"><span data-stu-id="8cc07-118">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="8cc07-119">Puntatore facoltativo a un oggetto di stato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-119">An optional pointer to a state object.</span></span> <span data-ttu-id="8cc07-120">Se specificato, l'oggetto di stato deve implementare **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="8cc07-120">If specified, the state object must implement **IUnknown**.</span></span>
    -   <span data-ttu-id="8cc07-121">Puntatore facoltativo a un oggetto privato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-121">An optional pointer to a private object.</span></span> <span data-ttu-id="8cc07-122">Se specificato, questo oggetto deve implementare anche **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="8cc07-122">If specified, this object also must implement **IUnknown**.</span></span>

    <span data-ttu-id="8cc07-123">Gli ultimi due puntatori possono essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8cc07-123">The last two pointers can be **NULL**.</span></span> <span data-ttu-id="8cc07-124">In caso contrario, utilizzarli per conservare informazioni sull'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="8cc07-124">Otherwise, use them to hold information about the asynchronous operation.</span></span>

3.  <span data-ttu-id="8cc07-125">Chiamare [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) per accodare l'elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-125">Call [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue to the work item.</span></span>
4.  <span data-ttu-id="8cc07-126">Il thread della coda di lavoro chiama il metodo [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="8cc07-126">The work-queue thread calls your [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span>
5.  <span data-ttu-id="8cc07-127">Eseguire l'operazione all'interno del metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="8cc07-127">Do the work inside your [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="8cc07-128">Il parametro *pAsyncResult* di questo metodo è il puntatore [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) del passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="8cc07-128">The *pAsyncResult* parameter of this method is the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) pointer from step 2.</span></span> <span data-ttu-id="8cc07-129">Utilizzare questo puntatore per ottenere l'oggetto di stato e l'oggetto privato:</span><span class="sxs-lookup"><span data-stu-id="8cc07-129">Use this pointer to get the state object and private object:</span></span>
    -   <span data-ttu-id="8cc07-130">Per ottenere l'oggetto di stato, chiamare [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="8cc07-130">To get the state object, call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>
    -   <span data-ttu-id="8cc07-131">Per ottenere l'oggetto privato, chiamare [**IMFAsyncResult:: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span><span class="sxs-lookup"><span data-stu-id="8cc07-131">To get the private object, call [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject).</span></span>

<span data-ttu-id="8cc07-132">In alternativa, è possibile combinare i passaggi 2 e 3 chiamando la funzione [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) .</span><span class="sxs-lookup"><span data-stu-id="8cc07-132">As an alternative, you can combine steps 2 and 3 by calling the [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) function.</span></span> <span data-ttu-id="8cc07-133">Internamente, questa funzione chiama [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) per creare l'oggetto risultato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-133">Internally, this function calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create the result object.</span></span>

<span data-ttu-id="8cc07-134">Il diagramma seguente illustra le relazioni tra il chiamante, l'oggetto risultato, l'oggetto stato e l'oggetto privato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-134">The following diagram shows the relationships between the caller, the result object, the state object, and the private object.</span></span>

![diagramma che mostra un oggetto risultato asincrono](images/workqueues01.png)

<span data-ttu-id="8cc07-136">Il diagramma di sequenza seguente illustra il modo in cui un oggetto Accoda un elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-136">The following sequence diagram shows how an object queues a work item.</span></span> <span data-ttu-id="8cc07-137">Quando il thread della coda di lavoro chiama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), l'oggetto esegue l'operazione asincrona su tale thread.</span><span class="sxs-lookup"><span data-stu-id="8cc07-137">When the work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), the object performs the asynchronous operation on that thread.</span></span>

![diagramma che illustra il modo in cui un oggetto Accoda un elemento di lavoro](images/workqueues02.png)

<span data-ttu-id="8cc07-139">È importante ricordare che [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) viene chiamato da un thread di proprietà della coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-139">It is important to remember [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from a thread that is owned by the work queue.</span></span> <span data-ttu-id="8cc07-140">L'implementazione di **Invoke** deve essere thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8cc07-140">Your implementation of **Invoke** must be thread safe.</span></span> <span data-ttu-id="8cc07-141">Inoltre, se si usa la coda di lavoro della piattaforma (**MFASYNC \_ callback \_ Queue \_ standard**), è fondamentale che non si blocchi mai il thread, perché ciò può bloccare l'intera pipeline Media Foundation dall'elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="8cc07-141">In addition, if you use the platform work queue (**MFASYNC\_CALLBACK\_QUEUE\_STANDARD**), it is critical that you never block the thread, because that can block the entire Media Foundation pipeline from processing data.</span></span> <span data-ttu-id="8cc07-142">Se è necessario eseguire un'operazione che blocca o richiede molto tempo per il completamento, utilizzare una coda di lavoro privata.</span><span class="sxs-lookup"><span data-stu-id="8cc07-142">If you need to perform an operation that will block or take a long time to complete, use a private work queue.</span></span> <span data-ttu-id="8cc07-143">Per creare una coda di lavoro privata, chiamare [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span><span class="sxs-lookup"><span data-stu-id="8cc07-143">To create a private work queue, call [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span> <span data-ttu-id="8cc07-144">Qualsiasi componente della pipeline che esegue operazioni di I/O deve evitare il blocco delle chiamate di I/O per lo stesso motivo.</span><span class="sxs-lookup"><span data-stu-id="8cc07-144">Any pipeline component that performs I/O operations should avoid blocking I/O calls for the same reason.</span></span> <span data-ttu-id="8cc07-145">L'interfaccia [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) fornisce un'astrazione utile per l'I/O di file asincrono.</span><span class="sxs-lookup"><span data-stu-id="8cc07-145">The [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface provides a useful abstraction for asynchronous file I/O.</span></span>

### <a name="implementing-the-beginend-pattern"></a><span data-ttu-id="8cc07-146">Implementazione di Begin. ../end... Modello</span><span class="sxs-lookup"><span data-stu-id="8cc07-146">Implementing the Begin.../End... Pattern</span></span>

<span data-ttu-id="8cc07-147">Come descritto in [chiamata di metodi asincroni](calling-asynchronous-methods.md), i metodi asincroni in Media Foundation spesso usano il metodo **Begin...** / **Fine.** .. modello.</span><span class="sxs-lookup"><span data-stu-id="8cc07-147">As described in [Calling Asynchronous Methods](calling-asynchronous-methods.md), asynchronous methods in Media Foundation often use the **Begin...**/**End....** pattern.</span></span> <span data-ttu-id="8cc07-148">In questo modello, un'operazione asincrona utilizza due metodi con firme simili alle seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc07-148">In this pattern, an asynchronous operation uses two methods with signatures similar to the following:</span></span>

``` syntax
// Starts the asynchronous operation.
HRESULT BeginX(IMFAsyncCallback *pCallback, IUnknown *punkState);

// Completes the asynchronous operation. 
// Call this method from inside the caller's Invoke method.
HRESULT EndX(IMFAsyncResult *pResult);
```

<span data-ttu-id="8cc07-149">Per rendere il metodo realmente asincrono, l'implementazione di **BeginX** deve eseguire il lavoro effettivo su un altro thread.</span><span class="sxs-lookup"><span data-stu-id="8cc07-149">To make the method truly asynchronous, the implementation of **BeginX** must perform the actual work on another thread.</span></span> <span data-ttu-id="8cc07-150">Questo è il punto in cui le code di lavoro entrano nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="8cc07-150">This is where work queues come into the picture.</span></span> <span data-ttu-id="8cc07-151">Nei passaggi successivi, il *chiamante* è il codice che chiama **BeginX** e **EndX**.</span><span class="sxs-lookup"><span data-stu-id="8cc07-151">In the steps that follow, the *caller* is the code that calls **BeginX** and **EndX**.</span></span> <span data-ttu-id="8cc07-152">Potrebbe trattarsi di un'applicazione o della pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8cc07-152">This might be an application or the Media Foundation pipeline.</span></span> <span data-ttu-id="8cc07-153">Il *componente* è il codice che implementa **BeginX** e **EndX**.</span><span class="sxs-lookup"><span data-stu-id="8cc07-153">The *component* is the code that implements **BeginX** and **EndX**.</span></span>

1.  <span data-ttu-id="8cc07-154">Il chiamante chiama **Begin...**, passando un puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.</span><span class="sxs-lookup"><span data-stu-id="8cc07-154">The caller calls **Begin...**, passing in a pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
2.  <span data-ttu-id="8cc07-155">Il componente crea un nuovo oggetto risultato asincrono.</span><span class="sxs-lookup"><span data-stu-id="8cc07-155">The component creates a new asynchronous result object.</span></span> <span data-ttu-id="8cc07-156">Questo oggetto archivia l'interfaccia di callback del chiamante e l'oggetto di stato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-156">This object stores the caller's callback interface and state object.</span></span> <span data-ttu-id="8cc07-157">In genere, archivia anche le informazioni sullo stato privato necessarie al componente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8cc07-157">Typically, it also stores any private state information that the component needs to complete the operation.</span></span> <span data-ttu-id="8cc07-158">L'oggetto risultato di questo passaggio è denominato "risultato 1" nel diagramma successivo.</span><span class="sxs-lookup"><span data-stu-id="8cc07-158">The result object from this step is labeled "Result 1" in the next diagram.</span></span>
3.  <span data-ttu-id="8cc07-159">Il componente crea un secondo oggetto risultato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-159">The component creates a second result object.</span></span> <span data-ttu-id="8cc07-160">Questo oggetto risultato archivia due puntatori: il primo oggetto risultato e l'interfaccia di callback del chiamato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-160">This result object stores two pointers: The first result object, and the callback interface of the callee.</span></span> <span data-ttu-id="8cc07-161">Questo oggetto risultato è denominato "result 2" nel diagramma successivo.</span><span class="sxs-lookup"><span data-stu-id="8cc07-161">This result object is labeled "Result 2" in the next diagram.</span></span>
4.  <span data-ttu-id="8cc07-162">Il componente chiama [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) per accodare un nuovo elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-162">The component calls [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) to queue a new work item.</span></span>
5.  <span data-ttu-id="8cc07-163">Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) il componente esegue l'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="8cc07-163">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the component does the asynchronous work.</span></span>
6.  <span data-ttu-id="8cc07-164">Il componente chiama [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) per richiamare il metodo di callback del chiamante.</span><span class="sxs-lookup"><span data-stu-id="8cc07-164">The component calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>
7.  <span data-ttu-id="8cc07-165">Il chiamante chiama il metodo **EndX** .</span><span class="sxs-lookup"><span data-stu-id="8cc07-165">The caller calls the **EndX** method.</span></span>

![diagramma che illustra il modo in cui un oggetto implementa il modello Begin/End](images/workqueues03.png)

## <a name="asynchronous-method-example"></a><span data-ttu-id="8cc07-167">Esempio di metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="8cc07-167">Asynchronous Method Example</span></span>

<span data-ttu-id="8cc07-168">Per illustrare questa discussione, verrà usato un esempio artificioso.</span><span class="sxs-lookup"><span data-stu-id="8cc07-168">To illustrate this discussion, we will use a contrived example.</span></span> <span data-ttu-id="8cc07-169">Si consideri un metodo asincrono per il calcolo di una radice quadrata:</span><span class="sxs-lookup"><span data-stu-id="8cc07-169">Consider an asynchronous method for computing a square root:</span></span>


```C++
    HRESULT BeginSquareRoot(double x, IMFAsyncCallback *pCB, IUnknown *pState);
    HRESULT EndSquareRoot(IMFAsyncResult *pResult, double *pVal);
```



<span data-ttu-id="8cc07-170">Il parametro *x* di `BeginSquareRoot` è il valore di cui verrà calcolata la radice quadrata.</span><span class="sxs-lookup"><span data-stu-id="8cc07-170">The *x* parameter of `BeginSquareRoot` is the value whose square root will be calculated.</span></span> <span data-ttu-id="8cc07-171">La radice quadrata viene restituita nel parametro *pval* di `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="8cc07-171">The square root is returned in the *pVal* parameter of `EndSquareRoot`.</span></span>

<span data-ttu-id="8cc07-172">Di seguito è illustrata la dichiarazione di una classe che implementa i due metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc07-172">Here is the declaration of a class that implements these two methods:</span></span>


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



<span data-ttu-id="8cc07-173">La `SqrRoot` classe implementa [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) in modo che possa inserire l'operazione radice quadrata in una coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-173">The `SqrRoot` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) so that it can put the square root operation on a work queue.</span></span> <span data-ttu-id="8cc07-174">Il `DoCalculateSquareRoot` metodo è il metodo della classe privata che calcola la radice quadrata.</span><span class="sxs-lookup"><span data-stu-id="8cc07-174">The `DoCalculateSquareRoot` method is the private class method that calculates the square root.</span></span> <span data-ttu-id="8cc07-175">Questo metodo verrà chiamato dal thread della coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-175">This method will be called from the work queue thread.</span></span>

<span data-ttu-id="8cc07-176">Per prima cosa, è necessario un modo per archiviare il valore di *x*, in modo che possa essere recuperato durante la chiamata del thread della coda di lavoro `SqrRoot::Invoke` .</span><span class="sxs-lookup"><span data-stu-id="8cc07-176">First, we need a way to store the value of *x*, so that it can be retrieved when the work queue thread calls `SqrRoot::Invoke`.</span></span> <span data-ttu-id="8cc07-177">Ecco una semplice classe che archivia le informazioni:</span><span class="sxs-lookup"><span data-stu-id="8cc07-177">Here is a simple class that stores the information:</span></span>


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



<span data-ttu-id="8cc07-178">Questa classe implementa **IUnknown** in modo che possa essere archiviata in un oggetto risultato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-178">This class implements **IUnknown** so that it can be stored in a result object.</span></span>

<span data-ttu-id="8cc07-179">Il codice seguente implementa il `BeginSquareRoot` Metodo:</span><span class="sxs-lookup"><span data-stu-id="8cc07-179">The following code implements the `BeginSquareRoot` method:</span></span>


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



<span data-ttu-id="8cc07-180">Il codice esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc07-180">This code does the following:</span></span>

1.  <span data-ttu-id="8cc07-181">Crea una nuova istanza della `AsyncOp` classe per mantenere il valore di *x*.</span><span class="sxs-lookup"><span data-stu-id="8cc07-181">Creates a new instance of the `AsyncOp` class to hold the value of *x*.</span></span>
2.  <span data-ttu-id="8cc07-182">Chiama [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) per creare un oggetto risultato.</span><span class="sxs-lookup"><span data-stu-id="8cc07-182">Calls [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) to create a result object.</span></span> <span data-ttu-id="8cc07-183">Questo oggetto include diversi puntatori:</span><span class="sxs-lookup"><span data-stu-id="8cc07-183">This object holds several pointers:</span></span>
    -   <span data-ttu-id="8cc07-184">Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) del chiamante.</span><span class="sxs-lookup"><span data-stu-id="8cc07-184">A pointer to the caller's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="8cc07-185">Puntatore all'oggetto di stato del chiamante (*pState*).</span><span class="sxs-lookup"><span data-stu-id="8cc07-185">A pointer to the caller's state object (*pState*).</span></span>
    -   <span data-ttu-id="8cc07-186">Puntatore all'oggetto `AsyncOp`.</span><span class="sxs-lookup"><span data-stu-id="8cc07-186">A pointer to the `AsyncOp` object.</span></span>
3.  <span data-ttu-id="8cc07-187">Chiama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) per accodare un nuovo elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-187">Calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item.</span></span> <span data-ttu-id="8cc07-188">Questa chiamata crea in modo implicito un oggetto risultato esterno, che contiene i puntatori seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc07-188">This call implicitly creates an outer result object, which holds the following pointers:</span></span>
    -   <span data-ttu-id="8cc07-189">Puntatore all' `SqrRoot` interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8cc07-189">A pointer to the `SqrRoot` object's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
    -   <span data-ttu-id="8cc07-190">Puntatore all'oggetto risultato interno del passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="8cc07-190">A pointer to the inner result object from step 2.</span></span>

<span data-ttu-id="8cc07-191">Il codice seguente implementa il `SqrRoot::Invoke` Metodo:</span><span class="sxs-lookup"><span data-stu-id="8cc07-191">The following code implements the `SqrRoot::Invoke` method:</span></span>


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



<span data-ttu-id="8cc07-192">Questo metodo ottiene l'oggetto risultato interno e l' `AsyncOp` oggetto.</span><span class="sxs-lookup"><span data-stu-id="8cc07-192">This method gets the inner result object and the `AsyncOp` object.</span></span> <span data-ttu-id="8cc07-193">Quindi passa l' `AsyncOp` oggetto a `DoCalculateSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="8cc07-193">Then it passes the `AsyncOp` object to `DoCalculateSquareRoot`.</span></span> <span data-ttu-id="8cc07-194">Infine, viene chiamato [**IMFAsyncResult:: sestatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) per impostare il codice di stato e [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) per richiamare il metodo di callback del chiamante.</span><span class="sxs-lookup"><span data-stu-id="8cc07-194">Finally, it calls [**IMFAsyncResult::SetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-setstatus) to set the status code and [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the caller's callback method.</span></span>

<span data-ttu-id="8cc07-195">Il `DoCalculateSquareRoot` metodo esegue esattamente ciò che ci si aspetta:</span><span class="sxs-lookup"><span data-stu-id="8cc07-195">The `DoCalculateSquareRoot` method does exactly what you would expect:</span></span>


```C++
HRESULT SqrRoot::DoCalculateSquareRoot(AsyncOp *pOp)
{
    pOp->m_value = sqrt(pOp->m_value);

    return S_OK;
}
```



<span data-ttu-id="8cc07-196">Quando viene richiamato il metodo di callback del chiamante, è responsabilità del chiamante chiamare il metodo **end...** , in questo caso `EndSquareRoot` .</span><span class="sxs-lookup"><span data-stu-id="8cc07-196">When the caller's callback method is invoked, it is the caller's responsibility to call the **End...** method—in this case, `EndSquareRoot`.</span></span> <span data-ttu-id="8cc07-197">`EndSquareRoot`È il modo in cui il chiamante Recupera il risultato dell'operazione asincrona, che in questo esempio è la radice quadrata calcolata.</span><span class="sxs-lookup"><span data-stu-id="8cc07-197">The `EndSquareRoot` is how the caller retrieves the result of the asynchronous operation, which in this example is the computed square root.</span></span> <span data-ttu-id="8cc07-198">Queste informazioni vengono archiviate nell'oggetto risultato:</span><span class="sxs-lookup"><span data-stu-id="8cc07-198">This information is stored in the result object:</span></span>


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



## <a name="operation-queues"></a><span data-ttu-id="8cc07-199">Code operazioni</span><span class="sxs-lookup"><span data-stu-id="8cc07-199">Operation Queues</span></span>

<span data-ttu-id="8cc07-200">Fino a questo punto, si presuppone che un'operazione asincrona possa essere eseguita in qualsiasi momento, indipendentemente dallo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8cc07-200">So far, it has been tacitly assumed that an asynchronous operation could be done at any time, regardless of the object's current state.</span></span> <span data-ttu-id="8cc07-201">Si consideri, ad esempio, cosa accade se un'applicazione chiama `BeginSquareRoot` mentre una chiamata precedente allo stesso metodo è ancora in sospeso.</span><span class="sxs-lookup"><span data-stu-id="8cc07-201">For example, consider what happens if an application calls `BeginSquareRoot` while an earlier call to the same method is still pending.</span></span> <span data-ttu-id="8cc07-202">La `SqrRoot` classe potrebbe accodare il nuovo elemento di lavoro prima di eseguire l'elemento di lavoro precedente.</span><span class="sxs-lookup"><span data-stu-id="8cc07-202">The `SqrRoot` class might queue the new work item before the previous work item is done.</span></span> <span data-ttu-id="8cc07-203">Tuttavia, le code di lavoro non garantiscono la serializzazione degli elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-203">However, work queues are not guaranteed to serialize work items.</span></span> <span data-ttu-id="8cc07-204">Tenere presente che una coda di lavoro può usare più di un thread per inviare elementi di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8cc07-204">Recall that a work queue can use more than one thread to dispatch work items.</span></span> <span data-ttu-id="8cc07-205">In un ambiente con multithreading, un elemento di lavoro potrebbe essere richiamato prima del completamento di quello precedente.</span><span class="sxs-lookup"><span data-stu-id="8cc07-205">In a multithreaded environment, a work item might be invoked before the previous one has completed.</span></span> <span data-ttu-id="8cc07-206">Gli elementi di lavoro possono anche essere richiamati in modo non corretto, se si verifica un cambio di contesto immediatamente prima che venga richiamato il callback.</span><span class="sxs-lookup"><span data-stu-id="8cc07-206">Work items can even be invoked out of order, if a context switch happens to occur just before the callback is invoked.</span></span>

<span data-ttu-id="8cc07-207">Per questo motivo, è responsabilità dell'oggetto serializzare le operazioni su se stesso, se necessario.</span><span class="sxs-lookup"><span data-stu-id="8cc07-207">For this reason, it is the object's responsibility to serialize operations on itself, if required.</span></span> <span data-ttu-id="8cc07-208">In altre parole, se l'oggetto *richiede che l'operazione a venga* completata prima che l'operazione *b* possa essere avviata, l'oggetto non deve accodare un elemento di lavoro per *B* fino al completamento dell'operazione *a* .</span><span class="sxs-lookup"><span data-stu-id="8cc07-208">In other words, if the object requires operation *A* to finish before operation *B* can start, the object must not queue a work item for *B* until operation *A* has completed.</span></span> <span data-ttu-id="8cc07-209">Un oggetto può soddisfare questo requisito con una propria coda di operazioni in sospeso.</span><span class="sxs-lookup"><span data-stu-id="8cc07-209">An object can meet this requirement by having its own queue of pending operations.</span></span> <span data-ttu-id="8cc07-210">Quando un metodo asincrono viene chiamato sull'oggetto, l'oggetto inserisce la richiesta nella propria coda.</span><span class="sxs-lookup"><span data-stu-id="8cc07-210">When an asynchronous method is called on the object, the object puts the request on its own queue.</span></span> <span data-ttu-id="8cc07-211">Quando ogni operazione asincrona viene completata, l'oggetto esegue il pull della richiesta successiva dalla coda.</span><span class="sxs-lookup"><span data-stu-id="8cc07-211">As each asynchronous operation is completed, the object pulls the next request from the queue.</span></span> <span data-ttu-id="8cc07-212">Nell' [esempio MPEG1Source](mpeg1source-sample.md) viene illustrato un esempio di come implementare una coda di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="8cc07-212">The [MPEG1Source Sample](mpeg1source-sample.md) shows an example of how to implement such a queue.</span></span>

<span data-ttu-id="8cc07-213">Un singolo metodo può coinvolgere diverse operazioni asincrone, in particolare quando vengono utilizzate chiamate di I/O.</span><span class="sxs-lookup"><span data-stu-id="8cc07-213">A single method might involve several asynchronous operations, particularly when I/O calls are used.</span></span> <span data-ttu-id="8cc07-214">Quando si implementano metodi asincroni, valutare con attenzione i requisiti di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="8cc07-214">When you implement asynchronous methods, think carefully about serialization requirements.</span></span> <span data-ttu-id="8cc07-215">Ad esempio, è possibile che l'oggetto avvii una nuova operazione mentre una richiesta di I/O precedente è ancora in sospeso?</span><span class="sxs-lookup"><span data-stu-id="8cc07-215">For example, is it valid for the object to start a new operation while a previous I/O request is still pending?</span></span> <span data-ttu-id="8cc07-216">Se la nuova operazione modifica lo stato interno dell'oggetto, cosa accade quando una richiesta di I/O precedente viene completata e restituisce dati che potrebbero essere obsoleti?</span><span class="sxs-lookup"><span data-stu-id="8cc07-216">If the new operation changes the object's internal state, what happens when a previous I/O request completes and returns data that might now be stale?</span></span> <span data-ttu-id="8cc07-217">Un diagramma di stato valido può aiutare a identificare le transizioni di stato valide.</span><span class="sxs-lookup"><span data-stu-id="8cc07-217">A good state diagram can help to identify the valid state transitions.</span></span>

## <a name="cross-thread-and-cross-process-considerations"></a><span data-ttu-id="8cc07-218">Considerazioni tra thread e tra processi</span><span class="sxs-lookup"><span data-stu-id="8cc07-218">Cross-Thread and Cross-Process Considerations</span></span>

<span data-ttu-id="8cc07-219">Le code di lavoro non utilizzano il marshalling COM per eseguire il marshalling di puntatori a interfaccia tra i limiti dei thread.</span><span class="sxs-lookup"><span data-stu-id="8cc07-219">Work queues do not use COM marshaling to marshal interface pointers across thread boundaries.</span></span> <span data-ttu-id="8cc07-220">Pertanto, anche se un oggetto viene registrato come thread-apartment o il thread dell'applicazione è entrato in un Apartment a thread singolo, i callback [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) verranno richiamati da un thread diverso.</span><span class="sxs-lookup"><span data-stu-id="8cc07-220">Therefore, even if an object is registered as apartment-threaded or the application thread has entered a single-threaded apartment (STA), [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callbacks will be invoked from a different thread.</span></span> <span data-ttu-id="8cc07-221">In ogni caso, tutti i componenti della pipeline Media Foundation devono usare il modello di threading "both".</span><span class="sxs-lookup"><span data-stu-id="8cc07-221">In any case, all Media Foundation pipeline components should use the "Both" threading model.</span></span>

<span data-ttu-id="8cc07-222">Alcune interfacce in Media Foundation definiscono versioni remote di alcuni metodi asincroni.</span><span class="sxs-lookup"><span data-stu-id="8cc07-222">Some interfaces in Media Foundation define remote versions of some asynchronous methods.</span></span> <span data-ttu-id="8cc07-223">Quando uno di questi metodi viene chiamato tra i limiti del processo, la DLL Media Foundation Proxy/Stub chiama la versione remota del metodo, che esegue il marshalling personalizzato dei parametri del metodo.</span><span class="sxs-lookup"><span data-stu-id="8cc07-223">When one of these methods is called across process boundaries, the Media Foundation proxy/stub DLL calls the remote version of the method, which performs custom marshaling of the method parameters.</span></span> <span data-ttu-id="8cc07-224">Nel processo remoto lo stub converte la chiamata nel metodo locale nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8cc07-224">In the remote process, the stub translates the call back into the local method on the object.</span></span> <span data-ttu-id="8cc07-225">Questo processo è trasparente per l'applicazione e l'oggetto remoto.</span><span class="sxs-lookup"><span data-stu-id="8cc07-225">This process is transparent to both the application and the remote object.</span></span> <span data-ttu-id="8cc07-226">Questi metodi di marshalling personalizzati vengono forniti principalmente per gli oggetti caricati nel percorso multimediale protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="8cc07-226">These custom marshaling methods are provided primarily for objects that are loaded in the protected media path (PMP).</span></span> <span data-ttu-id="8cc07-227">Per ulteriori informazioni su PMP, vedere il [percorso multimediale protetto](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="8cc07-227">For more information about the PMP, see [Protected Media Path](protected-media-path.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cc07-228">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cc07-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cc07-229">Metodi di callback asincroni</span><span class="sxs-lookup"><span data-stu-id="8cc07-229">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> <dt>

[<span data-ttu-id="8cc07-230">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="8cc07-230">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 



