---
description: Sono disponibili diverse opzioni per ricevere le indicazioni di completamento, fornendo così applicazioni con livelli di flessibilità appropriati. Sono inclusi l'attesa (o il blocco) sugli oggetti evento, il polling degli oggetti evento e le routine di completamento I/O del socket.
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: Ricezione delle indicazioni di completamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd05d8297af17c26393b5db113fac283b39fcbb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317003"
---
# <a name="receiving-completion-indications"></a>Ricezione delle indicazioni di completamento

Sono disponibili diverse opzioni per ricevere le indicazioni di completamento, fornendo così applicazioni con livelli di flessibilità appropriati. Sono inclusi l'attesa (o il blocco) sugli oggetti evento, il polling degli oggetti evento e le routine di completamento I/O del socket.

## <a name="blocking-and-waiting-for-completion-indication"></a>Blocco e attesa dell'indicazione di completamento

Le applicazioni possono bloccarsi in attesa che uno o più oggetti evento vengano impostati utilizzando la funzione [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) . Nelle implementazioni di Windows, il processo o il thread si blocca effettivamente. Poiché gli oggetti evento Windows Sockets 2 sono implementati come eventi di Windows, per questo scopo è possibile utilizzare anche la funzione nativa di Windows, [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects) . Questa operazione è particolarmente utile se il thread deve attendere sia gli eventi socket che quelli non socket.

## <a name="polling-for-completion-indication"></a>Polling per l'indicazione di completamento

Le applicazioni che preferiscono non bloccare possono utilizzare la funzione [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) per eseguire il polling dello stato di completamento associato a un particolare oggetto evento. Questa funzione indica se l'operazione sovrapposta è stata completata e, se completata, dispone la funzione [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) per recuperare lo stato di errore dell'operazione sovrapposta.

## <a name="using-socket-io-completion-routines"></a>Uso delle routine di completamento I/O socket

Le funzioni utilizzate per avviare I/O sovrapposti ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) accettano tutti *il lpCompletionRoutine* come parametro di input facoltativo. Si tratta di un puntatore a una funzione specifica dell'applicazione che viene chiamata dopo che un'operazione di I/O sovrapposta avviata correttamente viene completata (correttamente o in caso contrario). La routine di completamento segue le stesse regole previste per le routine di completamento I/O dei file di Windows. Ovvero, la routine di completamento non viene richiamata finché il thread non è in uno stato di attesa di avviso, ad esempio quando viene richiamata la funzione [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) con il `fAlertable` flag impostato. Un'applicazione che usa l'opzione della routine di completamento per una particolare richiesta di I/O sovrapposta potrebbe non usare l'opzione wait di [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) per la stessa richiesta di i/o sovrapposta.

I trasporti consentono a un'applicazione di richiamare le operazioni di invio e ricezione dall'interno del contesto della routine di completamento I/O del socket e garantiscono che, per un determinato Socket, le routine di completamento I/O non saranno nidificate. In questo modo, le trasmissioni dei dati sensibili al tempo vengono eseguite interamente in un contesto preemptive.

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>Riepilogo dei meccanismi di indicazione di completamento sovrapposti

La particolare indicazione di completamento I/O sovrapposta da usare per una determinata operazione sovrapposta è determinata dal fatto che l'applicazione fornisca un puntatore a una funzione di completamento, se viene fatto riferimento a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped) e al valore del membro **hEvent** all'interno della struttura **WSAOVERLAPPED** (se fornito). La tabella seguente riepiloga la semantica di completamento per un socket sovrapposto e Mostra le varie combinazioni di *lpOverlapped*, **hEvent** e *il lpCompletionRoutine*:

| *lpOverlapped* | hEvent         | *Il lpCompletionRoutine* | Indicazione di completamento                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Non applicabile | Ignorato               | L'operazione viene completata in modo sincrono. Si comporta come se fosse un socket non sovrapposto.                                                                                                                                      |
| ! NULL          | NULL           | NULL                  | L'operazione è stata completata, ma non è disponibile alcun meccanismo di completamento supportato da Windows Sockets 2. In questo caso, è possibile usare il meccanismo della porta di completamento (se supportato). In caso contrario, non esiste alcuna notifica di completamento. |
| ! NULL          | ! NULL          | NULL                  | L'operazione è stata completata e viene eseguita la notifica tramite un oggetto evento di segnalazione.                                                                                                                                                  |
| ! NULL          | Ignorato        | ! NULL                 | Il completamento dell'operazione è sovrapposto, notifica pianificando la routine di completamento.                                                                                                                                           |



 

 

 
