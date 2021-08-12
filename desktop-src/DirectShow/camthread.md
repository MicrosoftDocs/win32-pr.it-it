---
description: La classe CAMThread è una classe astratta per la gestione dei thread di lavoro.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Classe CAMThread (Wxutil.h)
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
ms.openlocfilehash: ca7182ecc16cd873732b2d39d2659f42017f9e01c1308642af4b8cac7ff2a682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662115"
---
# <a name="camthread-class"></a>Classe CAMThread

La `CAMThread` classe è una classe astratta per la gestione dei thread di lavoro.



| Variabili membro protette                                 | Descrizione                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**m \_ hThread**](camthread-m-hthread.md)                  | Handle per il thread.                                                        |
| Variabili membro pubbliche                                    | Descrizione                                                                  |
| [**m \_ AccessLock**](camthread-m-accesslock.md)            | Sezione critica che blocca l'accesso al thread da parte di altri thread. |
| [**m \_ WorkerLock**](camthread-m-workerlock.md)            | Sezione critica che blocca i dati condivisi tra thread.                       |
| Metodi pubblici                                             | Descrizione                                                                  |
| [**CAMThread**](camthread-camthread.md)                   | Metodo del costruttore.                                                          |
| [**~ CAMThread**](camthread--camthread.md)                | Metodo del distruttore. Virtuale.                                                  |
| [**InitialThreadProc**](camthread-initialthreadproc.md)   | Chiama il metodo ThreadProc quando viene creato il thread.                      |
| [**Crea**](camthread-create.md)                         | Crea il thread.                                                          |
| [**CallWorker**](camthread-callworker.md)                 | Segnala al thread una richiesta.                                           |
| [**Chiudi**](camthread-close.md)                           | Attende la chiusura del thread, quindi rilascia le relative risorse.                   |
| [**ThreadExists**](camthread-threadexists.md)             | Esegue una query per determinare se il thread esiste.                                           |
| [**Getrequest**](camthread-getrequest.md)                 | Attende la richiesta successiva.                                                  |
| [**CheckRequest**](camthread-checkrequest.md)             | Verifica se è presente una richiesta, senza blocco.                              |
| [**Rispondi**](camthread-reply.md)                           | Risponde a una richiesta.                                                        |
| [**GetRequestHandle**](camthread-getrequesthandle.md)     | Recupera un handle per l'evento segnalato dal metodo CallWorker.           |
| [**GetRequestParam**](camthread-getrequestparam.md)       | Recupera la richiesta più recente.                                                |
| [**CoInitializeHelper**](camthread-coinitializehelper.md) | Chiama CoInitializeEx all'inizio del thread.                             |
| Metodi virtuali puri                                       | Descrizione                                                                  |
| [**Threadproc**](camthread-threadproc.md)                 | Routine del thread.                                                            |



 

## <a name="remarks"></a>Commenti

Questa classe fornisce metodi per la creazione di un thread di lavoro, il passaggio di richieste al thread e l'attesa della chiusura del thread. Per usare questa classe, eseguire le operazioni seguenti:

-   Derivare una classe da `CAMThread` ed eseguire l'override del metodo virtuale [**puro CAMThread::ThreadProc**](camthread-threadproc.md). Questo metodo è la routine del thread che viene chiamata all'inizio del thread.
-   Nell'applicazione creare un'istanza della classe derivata. La creazione dell'oggetto non crea il thread. Per creare il thread, chiamare il [**metodo CAMThread::Create.**](camthread-create.md)
-   Per inviare richieste al thread, chiamare il [**metodo CAMThread::CallWorker.**](camthread-callworker.md) Questo metodo accetta un parametro DWORD, il cui significato è definito dalla classe . Il metodo si blocca fino a quando il thread non risponde (vedere di seguito).
-   Nella routine del thread rispondere alle richieste chiamando [**CAMThread::GetRequest**](camthread-getrequest.md) o [**CAMThread::CheckRequest**](camthread-checkrequest.md). Il metodo GetRequest si blocca fino a quando un altro thread non chiama CallWorker. Il metodo CheckRequest non è bloccante, che consente al thread di verificare la presenza di nuove richieste mentre funziona in modo asincrono.
-   Quando il thread riceve una richiesta, chiamare [**CAMThread::Reply**](camthread-reply.md) per sbloccare il thread chiamante. Il metodo Reply accetta un parametro DWORD, che viene passato al thread chiamante come valore restituito per CallWorker.

Al termine dell'esecuzione del thread, chiamare il [**metodo CAMThread::Close.**](camthread-close.md) Questo metodo attende la chiusura del thread e quindi chiude l'handle del thread. È necessario garantire l'uscita del messaggio ThreadProc, da solo o in risposta a una richiesta CallWorker. Il metodo del distruttore chiama anche Close.

L'esempio seguente illustra questi passaggi:


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



Nella classe derivata è anche possibile definire funzioni membro che convalidano i parametri in CallWorker. L'esempio seguente illustra un modo tipico per eseguire questa operazione:


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



La `CAMThread` classe fornisce due sezioni critiche come variabili membro pubbliche. Usare `CAMThread::m_AccessLock` per bloccare l'accesso al thread da parte di altri thread. Ad esempio, i metodi Create e CallWorker mantendono questo blocco per serializzare le operazioni sul thread. Usare [**CAMThread::m \_ WorkerLock**](camthread-m-workerlock.md) per bloccare i dati condivisi tra thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




