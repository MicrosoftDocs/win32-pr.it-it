---
description: Chiamata di metodi asincroni
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Chiamata di metodi asincroni
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524642"
---
# <a name="calling-asynchronous-methods"></a><span data-ttu-id="77016-103">Chiamata di metodi asincroni</span><span class="sxs-lookup"><span data-stu-id="77016-103">Calling Asynchronous Methods</span></span>

<span data-ttu-id="77016-104">In Media Foundation, molte operazioni vengono eseguite in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="77016-104">In Media Foundation, many operations are performed asynchronously.</span></span> <span data-ttu-id="77016-105">Le operazioni asincrone possono migliorare le prestazioni, perché non bloccano il thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="77016-105">Asynchronous operations can improve performance, because they do not block the calling thread.</span></span> <span data-ttu-id="77016-106">Un'operazione asincrona in Media Foundation viene definita da una coppia di metodi con la convenzione di denominazione **Begin..** . e **end..**...</span><span class="sxs-lookup"><span data-stu-id="77016-106">An asynchronous operation in Media Foundation is defined by a pair of methods with the naming convention **Begin...** and **End....**.</span></span> <span data-ttu-id="77016-107">Insieme, questi due metodi definiscono un'operazione di lettura asincrona sul flusso.</span><span class="sxs-lookup"><span data-stu-id="77016-107">Together, these two methods define an asynchronous read operation on the stream.</span></span>

<span data-ttu-id="77016-108">Per avviare un'operazione asincrona, chiamare il metodo **Begin** .</span><span class="sxs-lookup"><span data-stu-id="77016-108">To start an asynchronous operation, call the **Begin** method.</span></span> <span data-ttu-id="77016-109">Il metodo **Begin** contiene sempre almeno due parametri:</span><span class="sxs-lookup"><span data-stu-id="77016-109">The **Begin** method always contains at least two parameters:</span></span>

-   <span data-ttu-id="77016-110">Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="77016-110">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="77016-111">L'applicazione deve implementare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="77016-111">The application must implement this interface.</span></span>
-   <span data-ttu-id="77016-112">Puntatore a un oggetto di stato facoltativo.</span><span class="sxs-lookup"><span data-stu-id="77016-112">A pointer to an optional state object.</span></span>

<span data-ttu-id="77016-113">L'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) invia una notifica all'applicazione quando l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="77016-113">The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface notifies the application when the operation is completed.</span></span> <span data-ttu-id="77016-114">Per un esempio di come implementare questa interfaccia, vedere [implementazione del callback asincrono](implementing-the-asynchronous-callback.md).</span><span class="sxs-lookup"><span data-stu-id="77016-114">For an example of how to implement this interface, see [Implementing the Asynchronous Callback](implementing-the-asynchronous-callback.md).</span></span> <span data-ttu-id="77016-115">L'oggetto di stato è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="77016-115">The state object is optional.</span></span> <span data-ttu-id="77016-116">Se specificato, deve implementare l'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="77016-116">If specified, it must implement the **IUnknown** interface.</span></span> <span data-ttu-id="77016-117">È possibile usare l'oggetto state per archiviare le informazioni sullo stato necessarie per il callback.</span><span class="sxs-lookup"><span data-stu-id="77016-117">You can use the state object to store any state information that is needed by your callback.</span></span> <span data-ttu-id="77016-118">Se non sono necessarie informazioni sullo stato, è possibile impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="77016-118">If you do not need state information, you can set this parameter to **NULL**.</span></span> <span data-ttu-id="77016-119">Il metodo **Begin** può contenere parametri aggiuntivi specifici di tale metodo.</span><span class="sxs-lookup"><span data-stu-id="77016-119">The **Begin** method might contain additional parameters that are specific to that method.</span></span>

<span data-ttu-id="77016-120">Se il metodo **Begin** restituisce un codice di errore, significa che l'operazione non è riuscita immediatamente e il callback non viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="77016-120">If the **Begin** method returns a failure code, it means the operation has failed immediately, and the callback will not be invoked.</span></span> <span data-ttu-id="77016-121">Se il metodo **Begin** ha esito positivo, significa che l'operazione è in sospeso e il callback verrà richiamato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="77016-121">If the **Begin** method succeeds, it means the operation is pending, and the callback will be invoked when the operation completes.</span></span>

<span data-ttu-id="77016-122">Ad esempio, il metodo [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) avvia un'operazione di lettura asincrona su un flusso di byte:</span><span class="sxs-lookup"><span data-stu-id="77016-122">For example, the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) method starts an asynchronous read operation on a byte stream:</span></span>


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



<span data-ttu-id="77016-123">Il metodo di callback è [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="77016-123">The callback method is [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="77016-124">Ha un solo parametro, *pAsyncResult*, che è un puntatore all'interfaccia [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="77016-124">It has a single parameter, *pAsyncResult*, which is a pointer to the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="77016-125">Per completare l'operazione asincrona, chiamare il metodo **end** che corrisponde al metodo **Begin** asincrono.</span><span class="sxs-lookup"><span data-stu-id="77016-125">To complete the asynchronous operation, call the **End** method that matches the asynchronous **Begin** method.</span></span> <span data-ttu-id="77016-126">Il metodo **end** accetta sempre un puntatore **IMFAsyncResult** .</span><span class="sxs-lookup"><span data-stu-id="77016-126">The **End** method always takes an **IMFAsyncResult** pointer.</span></span> <span data-ttu-id="77016-127">Passare sempre lo stesso puntatore ricevuto nel metodo **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="77016-127">Always pass in the same pointer that you received in the **Invoke** method.</span></span> <span data-ttu-id="77016-128">L'operazione asincrona non è completa fino a quando non si chiama il metodo **end** .</span><span class="sxs-lookup"><span data-stu-id="77016-128">The asynchronous operation is not complete until you call the **End** method.</span></span> <span data-ttu-id="77016-129">È possibile chiamare il metodo **end** dall'interno del metodo **Invoke** oppure è possibile chiamarlo da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="77016-129">You may call the **End** method from inside the **Invoke** method, or you can call it from another thread.</span></span>

<span data-ttu-id="77016-130">Per completare, ad esempio, [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) in un flusso di byte, chiamare [**IMFByteStream:: indread**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span><span class="sxs-lookup"><span data-stu-id="77016-130">For example, to complete the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) on a byte stream, call [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span></span>


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



<span data-ttu-id="77016-131">Il valore restituito del metodo **end** indica lo stato dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="77016-131">The return value of the **End** method indicates the status of the asynchronous operation.</span></span> <span data-ttu-id="77016-132">Nella maggior parte dei casi, l'applicazione eseguirà alcune operazioni dopo il completamento dell'operazione asincrona, indipendentemente dal fatto che venga completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="77016-132">In most cases, your application will perform some work after the asynchronous operation completes, whether it completes successfully or not.</span></span> <span data-ttu-id="77016-133">Sono disponibili diverse opzioni:</span><span class="sxs-lookup"><span data-stu-id="77016-133">You have several options:</span></span>

-   <span data-ttu-id="77016-134">Eseguire l'operazione all'interno del metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="77016-134">Do the work inside the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="77016-135">Questo approccio è accettabile purché l'applicazione non blocchi mai il thread chiamante o attenda qualsiasi elemento all'interno del metodo **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="77016-135">This approach is acceptable as long as your application never blocks the calling thread or waits for anything inside the **Invoke** method.</span></span> <span data-ttu-id="77016-136">Se si blocca il thread chiamante, è possibile bloccare la pipeline di streaming.</span><span class="sxs-lookup"><span data-stu-id="77016-136">If you block the calling thread, you might block the streaming pipeline.</span></span> <span data-ttu-id="77016-137">Ad esempio, è possibile aggiornare alcune variabili di stato, ma non eseguire un'operazione di lettura sincrona o attendere un oggetto mutex.</span><span class="sxs-lookup"><span data-stu-id="77016-137">For example, you might update some state variables, but do not perform a synchronous read operation or wait on a mutex object.</span></span>
-   <span data-ttu-id="77016-138">Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) impostare un evento e restituire immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="77016-138">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, set an event and return immediately.</span></span> <span data-ttu-id="77016-139">Il thread chiamante dell'applicazione attende l'evento ed esegue l'operazione quando viene segnalato l'evento.</span><span class="sxs-lookup"><span data-stu-id="77016-139">The application's calling thread waits for the event and does the work when the event is signaled.</span></span>
-   <span data-ttu-id="77016-140">Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , inviare un messaggio di finestra privata alla finestra dell'applicazione e restituire immediatamente un messaggio.</span><span class="sxs-lookup"><span data-stu-id="77016-140">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, post a private window message to your application window and return immediately.</span></span> <span data-ttu-id="77016-141">L'applicazione esegue il lavoro nel relativo ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="77016-141">The application does the work on its message loop.</span></span> <span data-ttu-id="77016-142">(Assicurarsi di pubblicare il messaggio chiamando **PostMessage**, non **SendMessage**, perché **SendMessage** può bloccare il thread di callback).</span><span class="sxs-lookup"><span data-stu-id="77016-142">(Make sure to post the message by calling **PostMessage**, not **SendMessage**, because **SendMessage** can block the callback thread.)</span></span>

<span data-ttu-id="77016-143">È importante ricordare che [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) viene chiamato da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="77016-143">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from another thread.</span></span> <span data-ttu-id="77016-144">L'applicazione è responsabile di garantire che qualsiasi lavoro eseguito all'interno di **Invoke** sia thread-safe.</span><span class="sxs-lookup"><span data-stu-id="77016-144">Your application is responsible for ensuring that any work performed inside **Invoke** is thread-safe.</span></span>

<span data-ttu-id="77016-145">Per impostazione predefinita, il thread che chiama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) non fa presupposto del comportamento dell'oggetto callback.</span><span class="sxs-lookup"><span data-stu-id="77016-145">By default, the thread that calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) makes no assumptions about the behavior of your callback object.</span></span> <span data-ttu-id="77016-146">Facoltativamente, è possibile implementare il metodo [**IMFAsyncCallback:: GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) per restituire informazioni sull'implementazione del callback.</span><span class="sxs-lookup"><span data-stu-id="77016-146">Optionally, you can implement the [**IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) method to return information about your callback implementation.</span></span> <span data-ttu-id="77016-147">In caso contrario, questo metodo può restituire **E \_ NOTIMPL**:</span><span class="sxs-lookup"><span data-stu-id="77016-147">Otherwise, this method can return **E\_NOTIMPL**:</span></span>


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



<span data-ttu-id="77016-148">Se è stato specificato un oggetto stato nel metodo **Begin** , è possibile recuperarlo dall'interno del metodo di callback chiamando [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="77016-148">If you specified a state object in the **Begin** method, you can retrieve it from inside your callback method by calling [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77016-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77016-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77016-150">Metodi di callback asincroni</span><span class="sxs-lookup"><span data-stu-id="77016-150">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



