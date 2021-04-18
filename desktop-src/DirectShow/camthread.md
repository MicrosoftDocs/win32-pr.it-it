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
# <a name="camthread-class"></a>Classe CAMThread

La `CAMThread` classe è una classe astratta per la gestione dei thread di lavoro.



| Variabili membro protette                                 | Descrizione                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**\_hThread m**](camthread-m-hthread.md)                  | Handle per il thread.                                                        |
| Variabili membro pubblico                                    | Descrizione                                                                  |
| [**\_AccessLock m**](camthread-m-accesslock.md)            | Sezione critica che blocca l'accesso al thread da parte di altri thread. |
| [**\_WorkerLock m**](camthread-m-workerlock.md)            | Sezione critica che blocca i dati condivisi tra i thread.                       |
| Metodi pubblici                                             | Descrizione                                                                  |
| [**CAMThread**](camthread-camthread.md)                   | Metodo del costruttore.                                                          |
| [**~ CAMThread**](camthread--camthread.md)                | Metodo del distruttore. Virtuale.                                                  |
| [**InitialThreadProc**](camthread-initialthreadproc.md)   | Chiama il metodo ThreadProc quando viene creato il thread.                      |
| [**Creare**](camthread-create.md)                         | Crea il thread.                                                          |
| [**CallWorker**](camthread-callworker.md)                 | Segnala al thread la richiesta.                                           |
| [**Chiudi**](camthread-close.md)                           | Attende la chiusura del thread, quindi rilascia le relative risorse.                   |
| [**ThreadExists**](camthread-threadexists.md)             | Esegue una query sull'esistenza del thread.                                           |
| [**GetRequest**](camthread-getrequest.md)                 | Attende la richiesta successiva.                                                  |
| [**CheckRequest**](camthread-checkrequest.md)             | Verifica se è presente una richiesta, senza blocco.                              |
| [**Rispondi**](camthread-reply.md)                           | Risponde a una richiesta.                                                        |
| [**GetRequestHandle**](camthread-getrequesthandle.md)     | Recupera un handle per l'evento segnalato dal metodo CallWorker.           |
| [**GetRequestParam**](camthread-getrequestparam.md)       | Recupera la richiesta più recente.                                                |
| [**CoInitializeHelper**](camthread-coinitializehelper.md) | Chiama CoInitializeEx all'inizio del thread.                             |
| Metodi virtuali puri                                       | Descrizione                                                                  |
| [**ThreadProc**](camthread-threadproc.md)                 | Routine thread.                                                            |



 

## <a name="remarks"></a>Commenti

Questa classe fornisce metodi per la creazione di un thread di lavoro, il passaggio delle richieste al thread e l'attesa della chiusura del thread. Per usare questa classe, eseguire le operazioni seguenti:

-   Derivare una classe da `CAMThread` ed eseguire l'override del metodo virtuale pure [**CAMThread:: ThreadProc**](camthread-threadproc.md). Questo metodo è la routine del thread che viene chiamata all'inizio del thread.
-   Nell'applicazione creare un'istanza della classe derivata. La creazione dell'oggetto non comporta la creazione del thread. Per creare il thread, chiamare il metodo [**CAMThread:: create**](camthread-create.md) .
-   Per inviare richieste al thread, chiamare il metodo [**CAMThread:: CallWorker**](camthread-callworker.md) . Questo metodo accetta un parametro DWORD, il cui significato è definito dalla classe. Il metodo si blocca fino a quando il thread non risponde (vedere di seguito).
-   Nella procedura del thread rispondere alle richieste chiamando [**CAMThread:: GetRequest**](camthread-getrequest.md) o [**CAMThread:: CheckRequest**](camthread-checkrequest.md). Il metodo GetRequest si blocca fino a quando un altro thread chiama CallWorker. Il metodo CheckRequest non è bloccante, che consente al thread di verificare la presenza di nuove richieste mentre funziona in modo asincrono.
-   Quando il thread riceve una richiesta, chiamare [**CAMThread:: Reply**](camthread-reply.md) per sbloccare il thread chiamante. Il metodo Reply accetta un parametro DWORD, che viene passato al thread chiamante come valore restituito per CallWorker.

Al termine del thread, chiamare il metodo [**CAMThread:: Close**](camthread-close.md) . Questo metodo attende la chiusura del thread, quindi chiude l'handle del thread. È necessario garantire la chiusura del messaggio ThreadProc, in modo autonomo o in risposta a una richiesta CallWorker. Il metodo del distruttore chiama anche Close.

Nell'esempio seguente vengono illustrati questi passaggi:


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



Nella classe derivata è inoltre possibile definire funzioni membro che convalidano i parametri per CallWorker. Nell'esempio seguente viene illustrato un modo tipico per eseguire questa operazione:


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



La `CAMThread` classe fornisce due sezioni critiche come variabili membro pubbliche. Usare `CAMThread::m_AccessLock` per bloccare l'accesso al thread da parte di altri thread. Ad esempio, i metodi create e CallWorker mantengono questo blocco per serializzare le operazioni sul thread. Usare [**CAMThread:: m \_ WorkerLock**](camthread-m-workerlock.md) per bloccare i dati condivisi tra i thread.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




