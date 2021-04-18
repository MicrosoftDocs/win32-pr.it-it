---
description: Windows Sockets 2 supporta l'I/O sovrapposto e tutti i provider di trasporto supportano questa funzionalità.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Oggetti I/O sovrapposti e oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed034f06243959d94a1ada7eaa71e33c84cd35ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306914"
---
# <a name="overlapped-io-and-event-objects"></a>Oggetti I/O sovrapposti e oggetti evento

Windows Sockets 2 supporta l'I/O sovrapposto e tutti i provider di trasporto supportano questa funzionalità. L'I/O sovrapposto segue il modello stabilito in Windows e può essere eseguito su socket creati con la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o i socket creati con la funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con il flag **WSA \_ \_ sovrapposto** impostato nel parametro *dwFlags* .

> [!Note]  
> La creazione di un socket con l'attributo Overlapped non ha alcun effetto sul fatto che un socket sia attualmente in modalità di blocco o non blocco. I socket creati con l'attributo Overlapped possono essere utilizzati per eseguire operazioni di I/O sovrapposte, in modo da non modificare la modalità di blocco di un socket. Poiché le operazioni di I/O sovrapposte non vengono bloccate, la modalità di blocco di un socket è irrilevante per queste operazioni.

 

Per la ricezione, le applicazioni usano le funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) per fornire i buffer in cui devono essere ricevuti i dati. Se uno o più buffer vengono inviati prima del momento in cui i dati sono stati ricevuti dalla rete, i dati potrebbero essere inseriti nei buffer dell'utente immediatamente dopo l'arrivo. In questo modo, è possibile evitare l'operazione di copia che altrimenti si verificherebbe nel momento in cui viene richiamata la funzione [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) o [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) . Se i dati sono già presenti quando si inviano buffer di ricezione, vengono copiati immediatamente nei buffer dell'utente.

Se i dati arrivano quando l'applicazione non dispone di buffer di ricezione, la rete ricorre al consueto stile sincrono dell'operazione. Ovvero, i dati in ingresso vengono memorizzati nel buffer internamente fino a quando l'applicazione non emette una chiamata di ricezione e pertanto fornisce un buffer in cui i dati possono essere copiati. Un'eccezione è rappresentata dal caso in cui l'applicazione utilizza [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per impostare la dimensione del buffer di ricezione su zero. In questo caso, i protocolli affidabili consentono di ricevere solo i dati quando i buffer dell'applicazione sono stati inviati e i dati su protocolli non affidabili andranno perduti.

Sul lato di invio, le applicazioni usano [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) o [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) per fornire i puntatori ai buffer pieni e quindi accettano di non disturbare i buffer in alcun modo finché la rete non ha utilizzato il contenuto del buffer.

Le chiamate di invio e ricezione sovrapposte vengono restituite immediatamente. Un valore restituito pari a zero indica che l'operazione di I/O è stata completata immediatamente e che l'indicazione di completamento corrispondente è già stata eseguita. Ovvero l'oggetto evento associato è stato segnalato oppure una routine di completamento è stata accodata e verrà eseguita quando il thread chiamante entra nello stato di attesa di avviso.

Un valore restituito dell'errore del SOCKET \_ associato a un codice di errore di i/o di [WSA \_ \_ in sospeso](windows-sockets-error-codes-2.md) indica che l'operazione sovrapposta è stata avviata correttamente e che verrà fornita un'indicazione successiva quando vengono utilizzati i buffer di invio o quando un'operazione di ricezione è stata completata. Tuttavia, per i socket con stile di flusso di byte, l'indicazione di completamento viene eseguita ogni volta che i dati in ingresso vengono esauriti, indipendentemente dal fatto che i buffer siano pieni. Qualsiasi altro codice di errore indica che l'operazione sovrapposta non è stata avviata correttamente e che l'indicazione di completamento non sarà imminente.

È possibile sovrapporre le operazioni di invio e ricezione. Le funzioni receive possono essere richiamate più volte per inserire i buffer di ricezione in preparazione ai dati in ingresso e le funzioni di invio possono essere richiamate più volte per accodare più buffer da inviare. Mentre l'applicazione può basarsi su una serie di buffer di invio sovrapposti inviati nell'ordine specificato, le indicazioni di completamento corrispondenti possono verificarsi in un ordine diverso. Analogamente, sul lato ricevente, i buffer possono essere compilati nell'ordine in cui vengono forniti, ma le indicazioni di completamento possono verificarsi in un ordine diverso.

In molti casi, le operazioni Winsock sovrapposte che usano [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)e funzioni simili sono annullabili. Tuttavia, il comportamento non è definito per l'uso continuativo di un socket che ha annullato le operazioni in sospeso. La funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) deve essere chiamata dopo l'annullamento di un'operazione sovrapposta. Pertanto, per ottenere risultati ottimali, anziché annullare direttamente l'i/O, è necessario chiamare la funzione **chiamata closesocket** per chiudere il socket che interrompe infine tutte le operazioni in sospeso.

La funzionalità di completamento posticipato dell'I/O sovrapposto è disponibile anche per [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl), che è una versione migliorata di [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket).

 

 
