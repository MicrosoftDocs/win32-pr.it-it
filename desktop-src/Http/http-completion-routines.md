---
title: Routine di completamento HTTP
description: Le applicazioni offrono diverse opzioni per ricevere le indicazioni di completamento e offrire una certa flessibilità agli sviluppatori.
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd80259d806d81153a649ad606e40c10986090442e3cab5e04bd864367441871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981671"
---
# <a name="http-completion-routines"></a>Routine di completamento HTTP

Le applicazioni offrono diverse opzioni per ricevere le indicazioni di completamento e offrire una certa flessibilità agli sviluppatori. Le opzioni sono il blocco durante l'attesa del completamento di una chiamata API o l'uso delle routine di completamento per le operazioni asincrone. Il vantaggio dell'uso delle operazioni asincrone è un aumento della velocità di risposta dell'applicazione.

## <a name="blocked-io"></a>I/O bloccato

Le applicazioni possono bloccarsi durante l'attesa del completamento della chiamata API impostando la [**struttura OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) su **NULL.** In questo modo si bloccano effettivamente tutte le operazioni sul thread. Ad esempio, nelle chiamate a [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)la chiamata si blocca fino a quando la connessione non viene interrotta.

## <a name="asynchronous-io"></a>I/O asincrono

Le applicazioni che preferiscono non bloccare possono usare la [**struttura OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) per ottenere i risultati del completamento. L'applicazione fornisce un puntatore a una **struttura OVERLAPPED,** usata con un oggetto evento o una porta di completamento. Con una porta di completamento I/O, un handle HTTP viene usato come handle di file in un'operazione di I/O di file asincrona. Nella tabella seguente vengono riepilogate le opzioni di completamento disponibili per le applicazioni.



| Struttura sovrapposta | Oggetto event   | Porta di completamento | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | Non applicabile | Ignorato         | L'operazione viene completata in modo sincrono.                                                                           |
| Non **NULL**         | Non **NULL**   | **NULL**        | L'operazione viene completata in modo asincrono. La notifica sovrapposta viene eseguita segnalando un oggetto evento.       |
| Non **NULL**         | Ignorato        | Non **NULL**    | L'operazione viene completata in modo asincrono. La notifica sovrapposta viene eseguita pianificando una routine di completamento. |



 

## <a name="returning-the-number-of-bytes-read"></a>Restituzione del numero di byte letti

Alcune delle funzioni che usano la struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) per il completamento asincrono restituiscono un parametro *pBytesReceived* (o *pBytesSent* o *pBytesRead)* che indica il numero di byte trasferiti in modo sincrono. Per le chiamate asincrone, questo parametro deve essere impostato su **NULL.** Per le chiamate sincrone, il *parametro pBytesReceived* è facoltativo e può essere **NULL** o non **NULL.**

Se l'oggetto evento viene usato per il completamento asincrono, viene chiamata la [**funzione GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare il numero di byte letti. Se viene usata la porta di completamento (il *parametro hFile* è associato a una porta di completamento I/O), l'applicazione chiama la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per determinare il numero di byte letti. Se le operazioni asincrone non sono state completate, le applicazioni possono chiamare [**la funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere informazioni estese sugli errori.

La tabella seguente riepiloga il comportamento di completamento per il completamento sincrono e asincrono in funzioni come [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) che usano il *parametro pBytesReceived.*



| pBytesReceived\* | pOverlapped  | Descrizione                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | L'applicazione non riceve informazioni sul numero di byte restituiti.           |
| **NULL**         | Non **NULL** | Operazione asincrona, *pBytesReceived* non ha significato.                                |
| Non **NULL**     | **NULL**     | Operazione sincrona, numero di byte restituiti in *pBytesReceived.*                    |
| Non **NULL**     | Non **NULL** | Operazione asincrona, *pBytesReceived* viene ignorata anche se non è **NULL.**\*\* |



 

> [!Note]  
> \*Questo parametro può anche *essere pBytesSent* o *pBytesRead.*

 

> [!Note]  
> \*\*È consigliabile che le applicazioni passino un valore **NULL** in *pBytesReceived* per le operazioni asincrone e occorsi il numero di byte ricevuti da [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

 

## <a name="return-codes"></a>Codici restituiti

L'API del server HTTP restituisce tre classi di codici per le chiamate di funzione asincrone.

-   NESSUN \_ ERRORE
-   ERRORE \_ I/O \_ IN SOSPESO
-   Qualsiasi altro codice [di errore di sistema](/windows/desktop/Debug/system-error-codes).

Quando viene restituito ERROR IO PENDING o NO ERROR dalla chiamata di funzione asincrona, gli utenti devono aspettarsi che l'evento o la routine di \_ \_ completamento sia \_ segnalato. La chiamata [**alla funzione GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per l'evento o [**alla funzione GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per la porta di completamento restituisce lo stato di completamento. Inoltre, se viene restituito NO ERROR, le applicazioni possono eseguire \_ la post-elaborazione nello stesso thread che ha effettuato la chiamata API.

Se l'API del server HTTP restituisce un valore diverso da ERROR IO PENDING o NO ERROR, dalla chiamata di funzione asincrona la routine di completamento non viene segnalata e l'errore viene restituito direttamente \_ \_ \_ dall'API.

 

 