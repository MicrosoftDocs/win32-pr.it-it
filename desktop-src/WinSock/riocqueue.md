---
description: Specifica un descrittore della coda di completamento utilizzato per la notifica di completamento I/O tramite le richieste di invio e ricezione con le estensioni I/O registrate di Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310442"
---
# <a name="rio_cq"></a>\_CQ Rio

Il typedef di **Rio \_ CQ** specifica un descrittore della coda di completamento utilizzato per la notifica di completamento i/o tramite le richieste di invio e ricezione con le estensioni i/o registrate di Winsock.


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

**\_CQ Rio**
</dt> <dd>

Tipo di dati che specifica un descrittore della coda di completamento utilizzato per la notifica di completamento I/O dalle richieste di invio e ricezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'oggetto **Rio \_ CQ** viene utilizzato per la notifica di completamento i/o delle richieste di invio e ricezione della rete da parte delle estensioni i/o registrate di Winsock.

Un'applicazione può usare la funzione [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) per richiedere una notifica quando una coda di completamento di **Rio \_ CQ** non è vuota. Un'applicazione può anche eseguire il polling dello stato in qualsiasi momento di una coda di completamento di **Rio \_ CQ** in modo non bloccante usando la funzione [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .

L'oggetto **Rio \_ CQ** viene creato usando la funzione [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) . Al momento della creazione, l'applicazione deve specificare le dimensioni della coda, che determina il numero di voci di completamento che è possibile memorizzare. Quando un'applicazione chiama la funzione [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) per ottenere un handle di [**Rio \_ RQ**](riorqueue.md) , l'applicazione deve specificare un handle di **Rio \_ CQ** per i completamenti di invio e un handle di **Rio \_ CQ** per i completamenti della ricezione. Questi handle possono essere identici quando è necessario utilizzare la stessa coda per il completamento dell'invio e della ricezione. La funzione **RIOCreateRequestQueue** richiede anche un numero massimo di operazioni di invio e ricezione in attesa, che vengono addebitate in base alla capacità della coda o delle code di completamento associate. Se la capacità rimanente per le code non è sufficiente, la chiamata di **RIOCreateRequestQueue** avrà esito negativo con [WSAENOBUFS](windows-sockets-error-codes-2.md).

Il comportamento delle notifiche per una coda di completamento viene impostato al momento della creazione del **\_ CQ di Rio** .

Per una coda di completamento che usa un evento, il membro del **tipo** della struttura di [**\_ \_ completamento delle notifiche Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) viene impostato sul **\_ \_ completamento dell'evento Rio**. Il membro **Event. EventHandle** deve contenere l'handle per un evento creato dalla funzione [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) o [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) . Per ricevere il completamento del [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , l'applicazione deve attendere l'handle di evento specificato usando [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o una routine di attesa simile. Se l'applicazione prevede di reimpostare e riutilizzare l'evento, l'applicazione può ridurre il sovraccarico impostando il membro **Event. NotifyReset** su un valore diverso da zero. In questo modo l'evento viene reimpostato automaticamente dalla funzione **RIONotify** quando si verifica la notifica. In questo modo è possibile ridurre la necessità di chiamare la funzione [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) per reimpostare l'evento tra le chiamate alla funzione **RIONotify** .

Per una coda di completamento che usa una porta di completamento di I/O, il membro del **tipo** della struttura di [**\_ \_ completamento delle notifiche Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) è impostato sul **\_ \_ completamento IOCP di Rio**. Il membro **IOCP. IocpHandle** deve contenere l'handle per una porta di completamento i/O creata dalla funzione [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) . Per ricevere il completamento del [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , l'applicazione deve chiamare la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) o [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) . L'applicazione deve fornire un oggetto [**sovrapposto**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dedicato per la coda di completamento e può anche usare il membro **IOCP. CompletionKey** per distinguere le richieste **RIONotify** nella coda di completamento da altri completamenti di i/O, inclusi i completamenti **RIONotify** per altre code di completamento.

> [!Note]  
> Ai fini dell'efficienza, l'accesso alle code di completamento (**struct \_ CQ** ) e le code di richiesta (struct di [**Rio \_ RQ**](riorqueue.md) ) non sono protette dalle primitive di sincronizzazione. Se è necessario accedere a una coda di completamento o di richiesta da più thread, l'accesso deve essere coordinato da una sezione critica, da un blocco Write reader sottile o da un meccanismo simile. Questo blocco non è necessario per l'accesso da un singolo thread. Thread diversi possono accedere a code di completamento/richieste separate senza blocchi. La necessità di sincronizzazione avviene solo quando più thread tentano di accedere alla stessa coda. La sincronizzazione è necessaria anche se più thread inviano e ricevono lo stesso socket perché le operazioni di invio e ricezione utilizzano la coda di richieste del socket.

 

Se più thread tentano di accedere allo stesso valore di **Rio \_ CQ** usando [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), l'accesso deve essere coordinato da una sezione critica, da un blocco writer reader sottile o da un meccanismo di esclusione reciproca simile. Se le code di completamento non sono condivise, l'esclusione reciproca non è obbligatoria.

Quando una coda di completamento non è più necessaria, un'applicazione può chiuderla usando la funzione [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .

Il typedef di **Rio \_ CQ** è definito nel file di intestazione *Mswsockdef. h* , che viene incluso automaticamente nel file di intestazione *mswsock. h* . Il file di intestazione *Mswsockdef. h* non deve mai essere utilizzato direttamente.

## <a name="thread-safety"></a>Thread safety

Se più thread tentano di accedere allo stesso valore di **Rio \_ CQ** usando [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), l'accesso deve essere coordinato da una sezione critica, da un blocco writer reader sottile o da un meccanismo di esclusione reciproca simile. Se le code di completamento non sono condivise, l'esclusione reciproca non è obbligatoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Mswsockdef. h (include mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[**\_completamento notifiche \_ Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[**\_tipo di \_ completamento \_ notifica Rio**](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[**RIO \_ RQ**](riorqueue.md)
</dt> <dt>

[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))
</dt> <dt>

[**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
