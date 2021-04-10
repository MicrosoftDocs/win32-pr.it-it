---
title: Routine di completamento HTTP
description: Per le applicazioni sono disponibili diverse opzioni per la ricezione di indicazioni di completamento e una certa flessibilità per gli sviluppatori.
ms.assetid: c48a64d2-b6c8-4694-8600-f84751954bad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee05efc8284cb29130efae4bcaefb4834a3fb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963067"
---
# <a name="http-completion-routines"></a>Routine di completamento HTTP

Per le applicazioni sono disponibili diverse opzioni per la ricezione di indicazioni di completamento e una certa flessibilità per gli sviluppatori. Le opzioni sono bloccate in attesa del completamento di una chiamata API o per l'uso di routine di completamento per le operazioni asincrone. Il vantaggio dell'uso di operazioni asincrone è un aumento della velocità di risposta dell'applicazione.

## <a name="blocked-io"></a>I/O bloccato

Le applicazioni possono bloccarsi in attesa del completamento della chiamata API impostando la struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) su **null**. Questo blocca tutte le operazioni sul thread. Nelle chiamate a [**HttpWaitForDisconnect**](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect), ad esempio, la chiamata si blocca fino a quando la connessione non viene interruppe.

## <a name="asynchronous-io"></a>I/O asincrono

Le applicazioni che preferiscono non bloccare possono utilizzare la struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) per ottenere i risultati del completamento. L'applicazione fornisce un puntatore a una struttura **sovrapposta** , che viene utilizzata con un oggetto evento o una porta di completamento. Con una porta di completamento di I/O, un handle HTTP viene usato come handle di file in un'operazione di I/O di file asincrona. Nella tabella seguente sono riepilogate le opzioni di completamento disponibili per le applicazioni.



| Struttura sovrapposta | Oggetto Event   | Porta di completamento | Completion                                                                                                   |
|----------------------|----------------|-----------------|--------------------------------------------------------------------------------------------------------------|
| **NULL**             | Non applicabile | Ignorato         | L'operazione viene completata in modo sincrono.                                                                           |
| Non **null**         | Non **null**   | **NULL**        | L'operazione viene completata in modo asincrono. La notifica sovrapposta viene eseguita segnalando un oggetto evento.       |
| Non **null**         | Ignorato        | Non **null**    | L'operazione viene completata in modo asincrono. La notifica sovrapposta viene eseguita pianificando una routine di completamento. |



 

## <a name="returning-the-number-of-bytes-read"></a>Restituzione del numero di byte letti

Alcune delle funzioni che usano la struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) per il completamento asincrono restituiscono un parametro *PBytesReceived* (o *pBytesSent* o *pBytesRead*) che indica il numero di byte trasferiti in modo sincrono. Per le chiamate asincrone, questo parametro deve essere impostato su **null**. Per le chiamate sincrone, il parametro *pBytesReceived* è facoltativo e può essere **null** o non **null**.

Se l'oggetto evento viene utilizzato per il completamento asincrono, viene chiamata la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare il numero di byte letti. Se viene usata la porta di completamento (il parametro *hFile* è associato a una porta di completamento di I/O), l'applicazione chiama la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per determinare il numero di byte letti. Se le operazioni asincrone non sono state completate, le applicazioni possono chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere informazioni estese sull'errore.

La tabella seguente riepiloga il comportamento di completamento per il completamento sincrono e asincrono in funzioni come [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) che usano il parametro *pBytesReceived* .



| pBytesReceived\* | pOverlapped  | Descrizione                                                                             |
|------------------|--------------|-----------------------------------------------------------------------------------------|
| **NULL**         | **NULL**     | L'applicazione non riceve informazioni sul numero di byte restituiti.           |
| **NULL**         | Non **null** | L'operazione asincrona *pBytesReceived* è priva di significato.                                |
| Non **null**     | **NULL**     | Operazione sincrona, numero di byte restituiti in *pBytesReceived*.                    |
| Non **null**     | Non **null** | L'operazione asincrona *pBytesReceived* viene ignorata anche se non è **null**.\*\* |



 

> [!Note]  
> \*Questo parametro può essere anche *pBytesSent* o *pBytesRead*.

 

> [!Note]  
> \*\*È consigliabile che le applicazioni passino un **valore null** in *pBytesReceived* per le operazioni asincrone e ottengano il numero di byte ricevuti da [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

 

## <a name="return-codes"></a>Codici restituiti

L'API server HTTP restituisce tre classi di codici per le chiamate di funzione asincrone.

-   Nessun \_ errore
-   ERRORE i/o \_ \_ in sospeso
-   Qualsiasi altro [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).

Quando si verificano errori \_ \_ di i/o in sospeso o non \_ vengono restituiti errori dalla chiamata di funzione asincrona, è necessario che gli utenti attendano la segnalazione dell'evento o della routine di completamento. La chiamata della funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per l'evento o la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per la porta di completamento restituisce lo stato di completamento. Inoltre, se non \_ viene restituito alcun errore, le applicazioni possono eseguire la post-elaborazione sullo stesso thread che ha effettuato la chiamata all'API.

Se l'API del server HTTP restituisce un valore diverso da errore \_ io \_ in sospeso o nessun \_ errore, dalla chiamata di funzione asincrona, la routine di completamento non viene segnalata e l'errore viene restituito direttamente dall'API.

 

 