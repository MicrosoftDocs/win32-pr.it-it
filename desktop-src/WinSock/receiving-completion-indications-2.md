---
description: Sono disponibili diverse opzioni per ricevere le indicazioni di completamento, offrendo alle applicazioni livelli di flessibilità appropriati. tra cui l'attesa (o il blocco) di oggetti evento, il polling degli oggetti evento e le routine di completamento dell'I/O del socket.
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Ricezione delle indicazioni di completamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0ea3d46707eb31d803362f327c309d3c9d948812c0eb3a810e31b896e895e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569251"
---
# <a name="receiving-completion-indications"></a>Ricezione delle indicazioni di completamento

Sono disponibili diverse opzioni per ricevere le indicazioni di completamento, offrendo alle applicazioni livelli di flessibilità appropriati. tra cui l'attesa (o il blocco) di oggetti evento, il polling degli oggetti evento e le routine di completamento dell'I/O del socket.

## <a name="blocking-and-waiting-for-completion-indication"></a>Indicazione di blocco e attesa del completamento

Le applicazioni possono bloccarsi durante l'attesa dell'impostazione di uno o più oggetti evento tramite la [**funzione WSAWaitForMultipleEvents.**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) Nelle Windows, il processo o il thread si blocca effettivamente. Poiché Windows oggetti evento Windows Sockets 2 vengono implementati come eventi Windows, a questo scopo è possibile usare anche la funzione Windows nativa [**WaitForMultipleObjects.**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) Ciò è particolarmente utile se il thread deve attendere eventi socket e nonsocket.

## <a name="polling-for-completion-indication"></a>Polling per l'indicazione di completamento

Le applicazioni che preferiscono non bloccare possono usare la funzione [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) per eseguire il polling dello stato di completamento associato a qualsiasi oggetto evento specifico. Questa funzione indica se l'operazione sovrapposta è stata completata e, se completata, consente alla funzione [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) di recuperare lo stato di errore dell'operazione sovrapposta.

## <a name="using-socket-io-completion-routines"></a>Uso delle routine di completamento di I/O socket

Le funzioni usate per avviare operazioni di I/O sovrapposte ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) accettano *tutte lpCompletionRoutine* come parametro di input facoltativo. Si tratta di un puntatore a una funzione specifica dell'applicazione che viene chiamata dopo il completamento di un'operazione di I/O sovrapposta avviata correttamente (o in caso contrario). La routine di completamento segue le stesse regole stabilite per Windows di completamento di I/O di file. In altre parole, la routine di completamento non viene richiamata fino a quando il thread non si trova in uno stato di attesa avvisabile, ad esempio quando la funzione [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) viene richiamata con il `fAlertable` flag impostato. Un'applicazione che usa l'opzione della routine di completamento per una particolare richiesta di I/O sovrapposta potrebbe non usare l'opzione wait di [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) per la stessa richiesta di I/O sovrapposta.

I trasporti consentono a un'applicazione di richiamare operazioni di invio e ricezione dall'interno del contesto della routine di completamento I/O del socket e garantiscono che, per un determinato socket, le routine di completamento di I/O non saranno annidate. In questo modo, le trasmissioni di dati sensibili al tempo possono essere eseguite interamente all'interno di un contesto preemptive.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Riepilogo dei meccanismi di indicazione del completamento sovrapposti

L'indicazione specifica di completamento di I/O sovrapposto da usare per una determinata operazione sovrapposta è determinata dal fatto che l'applicazione fornisce un puntatore a una funzione di completamento, se viene fatto riferimento a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) e dal valore del membro **hEvent** all'interno della struttura **WSAOVERLAPPED** (se specificato). La tabella seguente riepiloga la semantica di completamento per un socket sovrapposto e illustra le varie combinazioni di *lpOverlapped*, **hEvent** e *lpCompletionRoutine*:

| *lpOverlapped* | hEvent         | *lpCompletionRoutine* | Indicazione di completamento                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Non applicabile | Ignorato               | L'operazione viene completata in modo sincrono. Si comporta come se fosse un socket non sovrapposto.                                                                                                                                      |
| ! Null          | NULL           | NULL                  | L'operazione viene completata sovrapposta, ma non Windows di completamento supportato da Sockets 2. In questo caso, è possibile usare il meccanismo della porta di completamento( se supportato). In caso contrario, non è presente alcuna notifica di completamento. |
| ! Null          | ! Null          | NULL                  | L'operazione viene completata sovrapposta, notifica segnalando l'oggetto evento.                                                                                                                                                  |
| ! Null          | Ignorato        | ! Null                 | L'operazione viene completata sovrapposta, notifica pianificando la routine di completamento.                                                                                                                                           |



 

 

 
