---
description: La classe CAMThread è una classe astratta per la gestione dei thread di lavoro.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Classe CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327228"
---
# <a name="camthread-class"></a><span data-ttu-id="2afd9-103">Classe CAMThread</span><span class="sxs-lookup"><span data-stu-id="2afd9-103">CAMThread class</span></span>

<span data-ttu-id="2afd9-104">La `CAMThread` classe è una classe astratta per la gestione dei thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2afd9-104">The `CAMThread` class is an abstract class for managing worker threads.</span></span>



| <span data-ttu-id="2afd9-105">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="2afd9-105">Protected Member Variables</span></span>                                 | <span data-ttu-id="2afd9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2afd9-106">Description</span></span>                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="2afd9-107">**\_hThread m**</span><span class="sxs-lookup"><span data-stu-id="2afd9-107">**m\_hThread**</span></span>](camthread-m-hthread.md)                  | <span data-ttu-id="2afd9-108">Handle per il thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-108">Handle to the thread.</span></span>                                                        |
| <span data-ttu-id="2afd9-109">Variabili membro pubblico</span><span class="sxs-lookup"><span data-stu-id="2afd9-109">Public Member Variables</span></span>                                    | <span data-ttu-id="2afd9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2afd9-110">Description</span></span>                                                                  |
| [<span data-ttu-id="2afd9-111">**\_AccessLock m**</span><span class="sxs-lookup"><span data-stu-id="2afd9-111">**m\_AccessLock**</span></span>](camthread-m-accesslock.md)            | <span data-ttu-id="2afd9-112">Sezione critica che blocca l'accesso al thread da parte di altri thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-112">Critical section that locks the thread from being accessed by other threads.</span></span> |
| [<span data-ttu-id="2afd9-113">**\_WorkerLock m**</span><span class="sxs-lookup"><span data-stu-id="2afd9-113">**m\_WorkerLock**</span></span>](camthread-m-workerlock.md)            | <span data-ttu-id="2afd9-114">Sezione critica che blocca i dati condivisi tra i thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-114">Critical section that locks data shared among threads.</span></span>                       |
| <span data-ttu-id="2afd9-115">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="2afd9-115">Public Methods</span></span>                                             | <span data-ttu-id="2afd9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2afd9-116">Description</span></span>                                                                  |
| [<span data-ttu-id="2afd9-117">**CAMThread**</span><span class="sxs-lookup"><span data-stu-id="2afd9-117">**CAMThread**</span></span>](camthread-camthread.md)                   | <span data-ttu-id="2afd9-118">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="2afd9-118">Constructor method.</span></span>                                                          |
| [<span data-ttu-id="2afd9-119">**~ CAMThread**</span><span class="sxs-lookup"><span data-stu-id="2afd9-119">**~ CAMThread**</span></span>](camthread--camthread.md)                | <span data-ttu-id="2afd9-120">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="2afd9-120">Destructor method.</span></span> <span data-ttu-id="2afd9-121">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="2afd9-121">Virtual.</span></span>                                                  |
| [<span data-ttu-id="2afd9-122">**InitialThreadProc**</span><span class="sxs-lookup"><span data-stu-id="2afd9-122">**InitialThreadProc**</span></span>](camthread-initialthreadproc.md)   | <span data-ttu-id="2afd9-123">Chiama il metodo ThreadProc quando viene creato il thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-123">Calls the ThreadProc method when the thread is created.</span></span>                      |
| [<span data-ttu-id="2afd9-124">**Creare**</span><span class="sxs-lookup"><span data-stu-id="2afd9-124">**Create**</span></span>](camthread-create.md)                         | <span data-ttu-id="2afd9-125">Crea il thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-125">Creates the thread.</span></span>                                                          |
| [<span data-ttu-id="2afd9-126">**CallWorker**</span><span class="sxs-lookup"><span data-stu-id="2afd9-126">**CallWorker**</span></span>](camthread-callworker.md)                 | <span data-ttu-id="2afd9-127">Segnala al thread la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2afd9-127">Signals the thread with a request.</span></span>                                           |
| [<span data-ttu-id="2afd9-128">**Chiudi**</span><span class="sxs-lookup"><span data-stu-id="2afd9-128">**Close**</span></span>](camthread-close.md)                           | <span data-ttu-id="2afd9-129">Attende la chiusura del thread, quindi rilascia le relative risorse.</span><span class="sxs-lookup"><span data-stu-id="2afd9-129">Waits for the thread to exit, then releases its resources.</span></span>                   |
| [<span data-ttu-id="2afd9-130">**ThreadExists**</span><span class="sxs-lookup"><span data-stu-id="2afd9-130">**ThreadExists**</span></span>](camthread-threadexists.md)             | <span data-ttu-id="2afd9-131">Esegue una query sull'esistenza del thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-131">Queries whether the thread exists.</span></span>                                           |
| [<span data-ttu-id="2afd9-132">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="2afd9-132">**GetRequest**</span></span>](camthread-getrequest.md)                 | <span data-ttu-id="2afd9-133">Attende la richiesta successiva.</span><span class="sxs-lookup"><span data-stu-id="2afd9-133">Waits for the next request.</span></span>                                                  |
| [<span data-ttu-id="2afd9-134">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="2afd9-134">**CheckRequest**</span></span>](camthread-checkrequest.md)             | <span data-ttu-id="2afd9-135">Verifica se è presente una richiesta, senza blocco.</span><span class="sxs-lookup"><span data-stu-id="2afd9-135">Checks if there is a request, without blocking.</span></span>                              |
| [<span data-ttu-id="2afd9-136">**Rispondi**</span><span class="sxs-lookup"><span data-stu-id="2afd9-136">**Reply**</span></span>](camthread-reply.md)                           | <span data-ttu-id="2afd9-137">Risponde a una richiesta.</span><span class="sxs-lookup"><span data-stu-id="2afd9-137">Replies to a request.</span></span>                                                        |
| [<span data-ttu-id="2afd9-138">**GetRequestHandle**</span><span class="sxs-lookup"><span data-stu-id="2afd9-138">**GetRequestHandle**</span></span>](camthread-getrequesthandle.md)     | <span data-ttu-id="2afd9-139">Recupera un handle per l'evento segnalato dal metodo CallWorker.</span><span class="sxs-lookup"><span data-stu-id="2afd9-139">Retrieves a handle to the event signaled by the CallWorker method.</span></span>           |
| [<span data-ttu-id="2afd9-140">**GetRequestParam**</span><span class="sxs-lookup"><span data-stu-id="2afd9-140">**GetRequestParam**</span></span>](camthread-getrequestparam.md)       | <span data-ttu-id="2afd9-141">Recupera la richiesta più recente.</span><span class="sxs-lookup"><span data-stu-id="2afd9-141">Retrieves the latest request.</span></span>                                                |
| [<span data-ttu-id="2afd9-142">**CoInitializeHelper**</span><span class="sxs-lookup"><span data-stu-id="2afd9-142">**CoInitializeHelper**</span></span>](camthread-coinitializehelper.md) | <span data-ttu-id="2afd9-143">Chiama CoInitializeEx all'inizio del thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-143">Calls CoInitializeEx at the start of the thread.</span></span>                             |
| <span data-ttu-id="2afd9-144">Metodi virtuali puri</span><span class="sxs-lookup"><span data-stu-id="2afd9-144">Pure Virtual Methods</span></span>                                       | <span data-ttu-id="2afd9-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2afd9-145">Description</span></span>                                                                  |
| [<span data-ttu-id="2afd9-146">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="2afd9-146">**ThreadProc**</span></span>](camthread-threadproc.md)                 | <span data-ttu-id="2afd9-147">Routine thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-147">Thread procedure.</span></span>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="2afd9-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="2afd9-148">Remarks</span></span>

<span data-ttu-id="2afd9-149">Questa classe fornisce metodi per la creazione di un thread di lavoro, il passaggio delle richieste al thread e l'attesa della chiusura del thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-149">This class provides methods for creating a worker thread, passing requests to the thread, and waiting for the thread to exit.</span></span> <span data-ttu-id="2afd9-150">Per usare questa classe, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2afd9-150">To use this class, do the following:</span></span>

-   <span data-ttu-id="2afd9-151">Derivare una classe da `CAMThread` ed eseguire l'override del metodo virtuale pure [**CAMThread:: ThreadProc**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="2afd9-151">Derive a class from `CAMThread` and override the pure virtual method [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="2afd9-152">Questo metodo è la routine del thread che viene chiamata all'inizio del thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-152">This method is the thread procedure that gets called at the start of the thread.</span></span>
-   <span data-ttu-id="2afd9-153">Nell'applicazione creare un'istanza della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="2afd9-153">In your application, create an instance of your derived class.</span></span> <span data-ttu-id="2afd9-154">La creazione dell'oggetto non comporta la creazione del thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-154">Creating the object does not create the thread.</span></span> <span data-ttu-id="2afd9-155">Per creare il thread, chiamare il metodo [**CAMThread:: create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="2afd9-155">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>
-   <span data-ttu-id="2afd9-156">Per inviare richieste al thread, chiamare il metodo [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="2afd9-156">To send requests to the thread, call the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="2afd9-157">Questo metodo accetta un parametro DWORD, il cui significato è definito dalla classe.</span><span class="sxs-lookup"><span data-stu-id="2afd9-157">This method takes a DWORD parameter, whose meaning is defined by your class.</span></span> <span data-ttu-id="2afd9-158">Il metodo si blocca fino a quando il thread non risponde (vedere di seguito).</span><span class="sxs-lookup"><span data-stu-id="2afd9-158">The method blocks until the thread responds (see below).</span></span>
-   <span data-ttu-id="2afd9-159">Nella procedura del thread rispondere alle richieste chiamando [**CAMThread:: GetRequest**](camthread-getrequest.md) o [**CAMThread:: CheckRequest**](camthread-checkrequest.md).</span><span class="sxs-lookup"><span data-stu-id="2afd9-159">In your thread procedure, respond to requests by calling either [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md).</span></span> <span data-ttu-id="2afd9-160">Il metodo GetRequest si blocca fino a quando un altro thread chiama CallWorker.</span><span class="sxs-lookup"><span data-stu-id="2afd9-160">The GetRequest method blocks until another thread calls CallWorker.</span></span> <span data-ttu-id="2afd9-161">Il metodo CheckRequest non è bloccante, che consente al thread di verificare la presenza di nuove richieste mentre funziona in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="2afd9-161">The CheckRequest method is non-blocking, which enables the thread to check for new requests while working asynchronously.</span></span>
-   <span data-ttu-id="2afd9-162">Quando il thread riceve una richiesta, chiamare [**CAMThread:: Reply**](camthread-reply.md) per sbloccare il thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="2afd9-162">When the thread receives a request, call [**CAMThread::Reply**](camthread-reply.md) to unblock the calling thread.</span></span> <span data-ttu-id="2afd9-163">Il metodo Reply accetta un parametro DWORD, che viene passato al thread chiamante come valore restituito per CallWorker.</span><span class="sxs-lookup"><span data-stu-id="2afd9-163">The Reply method takes a DWORD parameter, which is passed to the calling thread as the return value for CallWorker.</span></span>

<span data-ttu-id="2afd9-164">Al termine del thread, chiamare il metodo [**CAMThread:: Close**](camthread-close.md) .</span><span class="sxs-lookup"><span data-stu-id="2afd9-164">When you are done with the thread, call the [**CAMThread::Close**](camthread-close.md) method.</span></span> <span data-ttu-id="2afd9-165">Questo metodo attende la chiusura del thread, quindi chiude l'handle del thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-165">This method waits for the thread to exit, and then closes the thread handle.</span></span> <span data-ttu-id="2afd9-166">È necessario garantire la chiusura del messaggio ThreadProc, in modo autonomo o in risposta a una richiesta CallWorker.</span><span class="sxs-lookup"><span data-stu-id="2afd9-166">Your ThreadProc message must be guaranteed to exit, either on its own or in response to a CallWorker request.</span></span> <span data-ttu-id="2afd9-167">Il metodo del distruttore chiama anche Close.</span><span class="sxs-lookup"><span data-stu-id="2afd9-167">The destructor method also calls Close.</span></span>

<span data-ttu-id="2afd9-168">Nell'esempio seguente vengono illustrati questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="2afd9-168">The following example illustrates these steps:</span></span>


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



<span data-ttu-id="2afd9-169">Nella classe derivata è inoltre possibile definire funzioni membro che convalidano i parametri per CallWorker.</span><span class="sxs-lookup"><span data-stu-id="2afd9-169">In your derived class, you can also define member functions that validate the parameters to CallWorker.</span></span> <span data-ttu-id="2afd9-170">Nell'esempio seguente viene illustrato un modo tipico per eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="2afd9-170">The following example shows a typical way to do this:</span></span>


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



<span data-ttu-id="2afd9-171">La `CAMThread` classe fornisce due sezioni critiche come variabili membro pubbliche.</span><span class="sxs-lookup"><span data-stu-id="2afd9-171">The `CAMThread` class provides two critical sections as public member variables.</span></span> <span data-ttu-id="2afd9-172">Usare `CAMThread::m_AccessLock` per bloccare l'accesso al thread da parte di altri thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-172">Use `CAMThread::m_AccessLock` to lock the thread from being accessed by other threads.</span></span> <span data-ttu-id="2afd9-173">Ad esempio, i metodi create e CallWorker mantengono questo blocco per serializzare le operazioni sul thread. Usare [**CAMThread:: m \_ WorkerLock**](camthread-m-workerlock.md) per bloccare i dati condivisi tra i thread.</span><span class="sxs-lookup"><span data-stu-id="2afd9-173">(For example, the Create and CallWorker methods hold this lock, to serialize operations on the thread.) Use [**CAMThread::m\_WorkerLock**](camthread-m-workerlock.md) to lock data that is shared among threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="2afd9-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2afd9-174">Requirements</span></span>



| <span data-ttu-id="2afd9-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="2afd9-175">Requirement</span></span> | <span data-ttu-id="2afd9-176">Valore</span><span class="sxs-lookup"><span data-stu-id="2afd9-176">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2afd9-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2afd9-177">Header</span></span><br/>  | <dl> <span data-ttu-id="2afd9-178"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2afd9-178"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2afd9-179">Libreria</span><span class="sxs-lookup"><span data-stu-id="2afd9-179">Library</span></span><br/> | <dl> <span data-ttu-id="2afd9-180"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2afd9-180"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




