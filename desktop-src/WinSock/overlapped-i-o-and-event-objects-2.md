---
description: Windows Sockets 2 supporta l'I/O sovrapposto e tutti i provider di trasporto supportano questa funzionalità.
ms.assetid: b36ab606-df1a-4254-b048-6d47eb366275
title: Oggetti di I/O e eventi sovrapposti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6ae2ee17036275183518bfd444b9317bcdc05145a9fcb327ad48388618a66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741054"
---
# <a name="overlapped-io-and-event-objects"></a>Oggetti di I/O e eventi sovrapposti

Windows Sockets 2 supporta l'I/O sovrapposto e tutti i provider di trasporto supportano questa funzionalità. L'I/O sovrapposto segue il modello stabilito nel Windows e può essere eseguito sui socket creati con la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o i socket creati con la funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con il flag **\_ \_ OVERLAPPED FLAG WSA** impostato nel parametro *dwFlags.*

> [!Note]  
> La creazione di un socket con l'attributo sovrapposto non influisce sul fatto che un socket sia attualmente in modalità di blocco o non blocco. I socket creati con l'attributo sovrapposto possono essere usati per eseguire operazioni di I/O sovrapposte, in modo da non modificare la modalità di blocco di un socket. Poiché le operazioni di I/O sovrapposte non si bloccano, la modalità di blocco di un socket è irrilevante per queste operazioni.

 

Per la ricezione, le applicazioni usano le funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) per fornire buffer in cui devono essere ricevuti i dati. Se uno o più buffer vengono pubblicati prima del momento in cui i dati sono stati ricevuti dalla rete, i dati potrebbero essere inseriti nei buffer dell'utente immediatamente all'arrivo. Di conseguenza, può evitare l'operazione di copia che altrimenti si verificherebbe nel momento in cui viene richiamata la funzione [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) o [**recvfrom.**](/windows/desktop/api/winsock/nf-winsock-recvfrom) Se i dati sono già presenti quando vengono inviati buffer di ricezione, vengono copiati immediatamente nei buffer dell'utente.

Se i dati arrivano quando l'applicazione non ha inviato buffer di ricezione, la rete ricorre allo stile di funzionamento sincrono familiare. Ovvero, i dati in ingresso vengono memorizzati nel buffer internamente fino a quando l'applicazione non evade una chiamata di ricezione e quindi fornisce un buffer in cui i dati possono essere copiati. Un'eccezione a questo problema si verifica quando l'applicazione usa [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per impostare le dimensioni del buffer di ricezione su zero. In questo caso, i protocolli reliable consentivano la ricezione dei dati solo quando i buffer dell'applicazione erano stati pubblicati e i dati su protocolli non affidabili andrebbero persi.

Sul lato di invio, le applicazioni usano [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) o [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) per fornire puntatori ai buffer riempiti e quindi accettano di non disturbare i buffer in alcun modo fino a quando la rete non ha utilizzato il contenuto del buffer.

Le chiamate di invio e ricezione sovrapposte vengono restituite immediatamente. Un valore restituito pari a zero indica che l'operazione di I/O è stata completata immediatamente e che l'indicazione di completamento corrispondente è già stata eseguita. In altre parole, l'oggetto evento associato è stato segnalato o una routine di completamento è stata accodata e verrà eseguita quando il thread chiamante entra nello stato di attesa avvisabile.

Il valore restituito SOCKET ERROR associato a un codice di errore \_ [WSA \_ IO \_ PENDING](windows-sockets-error-codes-2.md) indica che l'operazione sovrapposta è stata avviata correttamente e che verrà fornita un'indicazione successiva quando i buffer di invio sono stati utilizzati o quando un'operazione di ricezione è stata completata. Tuttavia, per i socket in stile flusso di byte, l'indicazione di completamento si verifica ogni volta che i dati in ingresso sono esauriti, indipendentemente dal fatto che i buffer siano completi. Qualsiasi altro codice di errore indica che l'operazione sovrapposta non è stata avviata correttamente e che non sarà disponibile alcuna indicazione di completamento.

Sia le operazioni di invio che di ricezione possono essere sovrapposte. Le funzioni di ricezione possono essere richiamate più volte per pubblicare buffer di ricezione in preparazione dei dati in ingresso e le funzioni di invio possono essere richiamate più volte per accodare più buffer da inviare. Anche se l'applicazione può basarsi su una serie di buffer di trasmissione sovrapposti inviati nell'ordine fornito, le indicazioni di completamento corrispondenti potrebbero verificarsi in un ordine diverso. Analogamente, sul lato ricevente, i buffer possono essere compilati nell'ordine in cui vengono forniti, ma le indicazioni di completamento potrebbero verificarsi in un ordine diverso.

In molti casi, le operazioni di Winsock sovrapposte usando [**AcceptEx,**](/windows/win32/api/mswsock/nf-mswsock-acceptex) [**ConnectEx,**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) [**WSASend,**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) [**WSARecv,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)e funzioni simili sono annullabili. Tuttavia, il comportamento non è definito per l'uso continuo di un socket che ha annullato le operazioni in sospeso. La [**funzione closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) deve essere chiamata dopo l'annullamento di un'operazione sovrapposta. Pertanto, per ottenere risultati ottimali, anziché annullare direttamente l'I/O, è necessario chiamare la **funzione closesocket** per chiudere il socket che alla fine interromperà tutte le operazioni in sospeso.

La funzionalità di completamento posticipato dell'I/O sovrapposto è disponibile anche per [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl), che è una versione avanzata di [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket).

 

 
