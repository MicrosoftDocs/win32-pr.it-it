---
description: Windows Sockets 2 introduce operazioni di I/O sovrapposte e richiede che tutti i provider di trasporto supportino questa funzionalità.
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: Input/output sovrapposto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d260cccd13bfb8e872e0ac7346c112efff2f77cf115e3fe2f8dd3d3fb94deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641791"
---
# <a name="overlapped-inputoutput"></a>Input/output sovrapposto

Windows Sockets 2 introduce operazioni di I/O sovrapposte e richiede che tutti i provider di trasporto supportino questa funzionalità. Le operazioni di I/O sovrapposte possono essere eseguite solo sui socket creati tramite la funzione [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) con il flag WSA FLAG OVERLAPPED impostato e seguono il modello stabilito \_ \_ in Windows.

Per la ricezione, un client usa [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) o [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) per fornire i buffer in cui devono essere ricevuti i dati. Se uno o più buffer vengono inviati prima del momento in cui i dati sono stati ricevuti dalla rete, è possibile che i dati verranno inseriti nei buffer dell'utente immediatamente non appena arrivano ed evitare quindi l'operazione di copia che altrimenti si verificherebbe. Se i dati arrivano quando i buffer di ricezione sono già stati inviati, vengono copiati immediatamente nei buffer dell'utente. Se i dati arrivano quando l'applicazione non ha inviato buffer di ricezione, il provider di servizi ricorre allo stile sincrono dell'operazione in cui i dati in ingresso vengono memorizzati nel buffer internamente fino a quando il client non esegue una chiamata di ricezione e quindi fornisce un buffer in cui i dati possono essere copiati. Un'eccezione potrebbe essere se l'applicazione [**usasse WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) per impostare le dimensioni del buffer di ricezione su zero. In questo caso, i protocolli affidabili consentono la ricezione dei dati solo quando sono stati inseriti buffer dell'applicazione e i dati su protocolli non affidabili andrebbero persi.

Sul lato di invio, i client usano [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) o [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) per fornire puntatori ai buffer riempiti e quindi accettano di non disturbare i buffer in alcun modo fino a quando la rete non ha utilizzato il contenuto del buffer.

Le chiamate di invio e ricezione sovrapposte vengono restituite immediatamente. Un valore restituito pari a zero indica che l'operazione di I/O è stata completata immediatamente e che l'indicazione di completamento corrispondente è già stata eseguita. In altre parole, l'oggetto evento associato è stato segnalato o la routine di completamento è stata accodata tramite [**WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) Il valore restituito SOCKET ERROR associato a un codice di errore WSA IO PENDING indica che l'operazione sovrapposta è stata avviata correttamente e che verrà fornita un'indicazione successiva quando i buffer di invio sono stati utilizzati o quando i buffer di ricezione vengono \_ \_ \_ riempiti. Qualsiasi altro codice di errore indica che l'operazione sovrapposta non è stata avviata correttamente e che non sarà disponibile alcuna indicazione di completamento.

Sia le operazioni di invio che di ricezione possono sovrapporsi. Le funzioni di ricezione possono essere richiamate più volte per inviare i buffer di ricezione in preparazione dei dati in ingresso e le funzioni di invio possono essere richiamate più volte per accodare più buffer da inviare. Si noti che mentre una serie di buffer di invio sovrapposti verrà inviata nell'ordine fornito, le corrispondenti indicazioni di completamento possono verificarsi in un ordine diverso. Analogamente, sul lato ricevente, i buffer verranno compilati nell'ordine in cui vengono forniti, ma le indicazioni di completamento possono verificarsi in un ordine diverso.

La funzionalità di completamento posticipato dell'I/O sovrapposto è disponibile anche per [**WSPIoctl.**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))

## <a name="delivering-completion-indications"></a>Recapito delle indicazioni di completamento

I provider di servizi possono indicare il completamento sovrapposto in due modi: impostando un oggetto evento specificato dal client o richiamando una routine di completamento specificata dal client. In entrambi i casi una struttura di dati, [**WSAOVERLAPPED,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped)è associata a ogni operazione sovrapposta. Questa struttura viene allocata dal client e utilizzata dal client per indicare quale oggetto evento (se presente) deve essere impostato quando si verifica il completamento. La struttura **WSAOVERLAPPED** può essere utilizzata dal provider di servizi come posizione in cui archiviare un handle per i risultati (ad esempio, il numero di byte trasferiti, i flag aggiornati, i codici di errore e così via) per una particolare operazione sovrapposta. Per ottenere questi risultati, i client devono [**richiamare WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult), passando un puntatore alla struttura sovrapposta corrispondente.

Se si seleziona l'indicazione di completamento basata su eventi per una particolare richiesta di I/O sovrapposta, la routine [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) può essere usata dai client per eseguire il polling o attendere il completamento dell'operazione sovrapposta. Se viene selezionata l'indicazione di completamento basata su routine di completamento per una particolare richiesta di I/O sovrapposta, è disponibile solo l'opzione di polling **di WSPGetOverlappedResult.** Un client può anche usare altri mezzi per attendere (ad esempio usando [**WSAWaitForMultipleEvents)**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)fino a quando l'oggetto evento corrispondente non viene segnalato o la routine di completamento specificata non viene richiamata dal provider di servizi. Una volta indicato il completamento, il client può richiamare **WSPGetOverlappedResult**, con l'aspettativa che la chiamata venga completata immediatamente.

## <a name="invoking-socket-io-completion-routines"></a>Chiamata di routine di completamento I/O socket

Se il parametro *lpCompletionRoutine* per un'operazione sovrapposta non è **NULL,** è responsabilità del provider di servizi disporre della chiamata della routine di completamento specificata dal client al termine dell'operazione sovrapposta. Poiché la routine di completamento deve essere eseguita nel contesto dello stesso thread che ha avviato l'operazione sovrapposta, non può essere richiamata direttamente dal provider di servizi. L'32.DLL Ws2 offre un meccanismo APC (Asynchronous Procedure Call) per facilitare la \_ chiamata delle routine di completamento.

Un provider di servizi organizza l'esecuzione di una funzione nel thread appropriato chiamando [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Questa funzione può essere chiamata da qualsiasi contesto di processo e thread, anche da un contesto diverso dal thread e dal processo usati per avviare l'operazione sovrapposta.

[**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) accetta come parametri di input un puntatore a una struttura [**WSATHREADID,**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) un puntatore a una funzione APC da richiamare e un valore di contesto a 32 bit che viene successivamente passato alla funzione APC. I provider di servizi vengono sempre forniti con un puntatore alla struttura **WSATHREADID** appropriata tramite il *parametro lpThreadId* alla funzione sovrapposta. Il provider deve archiviare la struttura **WSATHREADID** in locale e fornire un puntatore a questa copia della struttura **WSATHREADID** come parametro di input per **WPUQueueApc.** Una volta restituita la funzione **WPUQueueApc,** il provider può eliminare la copia di **WSATHREADID**.

La procedura [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) accoda semplicemente informazioni sufficienti per chiamare la funzione APC indicata con i parametri specificati, ma non la chiama. Quando il thread di destinazione entra in uno stato di attesa avvisabile, queste informazioni vengono rimovite dalla coda e viene effettuata una chiamata alla funzione APC nel thread di destinazione e nel contesto del processo. Poiché il meccanismo APC supporta solo un singolo valore di contesto a 32 bit, la funzione APC non può essere la routine di completamento specificata dal client, che include più parametri. Il provider di servizi deve invece fornire un puntatore alla propria funzione APC che usa il valore di contesto fornito per accedere alle informazioni sui risultati necessarie per l'operazione sovrapposta e quindi richiama la routine di completamento specificata dal client.

Per i provider di servizi in cui un componente in modalità utente implementa operazioni di I/O sovrapposte, l'utilizzo tipico del meccanismo APC è il seguente:

-   Al termine dell'operazione di I/O, il provider alloca un buffer di piccole dimensioni e lo contiene con un puntatore alla procedura di completamento fornita dal client e i valori dei parametri da passare alla procedura.
-   Accoda un APC, specificando il puntatore al buffer come valore di contesto e la propria procedura intermedia come procedura di destinazione.
-   Quando il thread di destinazione entra nello stato di attesa avvisabile, la procedura intermedia del provider di servizi viene chiamata nel contesto del thread appropriato.
-   La procedura intermedia decomprime semplicemente i parametri, dealloca il buffer e chiama la procedura di completamento fornita dal client.
-   Per i provider di servizi in cui un componente in modalità kernel implementa operazioni di I/O sovrapposte, un'implementazione tipica è simile, ad eccezione del fatto che l'implementazione userebbe interfacce kernel standard per accodare il modulo APC.

La descrizione delle interfacce kernel pertinenti non rientra nell'ambito della specifica Windows Sockets 2.

> [!Note]  
> I provider di servizi devono consentire ai client Windows Sockets 2 di richiamare le operazioni di invio e ricezione dall'interno del contesto della routine di completamento I/O del socket e garantire che per un determinato socket le routine di completamento I/O non saranno annidate.

 

In alcuni casi, un provider di servizi su più livelli potrebbe dover avviare e completare operazioni sovrapposte dall'interno di un thread di lavoro interno. In questo caso, [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) non sarebbe disponibile da una chiamata di funzione in ingresso. L'interfaccia del provider di servizi fornisce una chiamata, [**WPUOpenCurrentThread,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread)per ottenere **un WSATHREADID** per il thread corrente. Quando questo **WSATHREADID** non è più necessario, le relative risorse devono essere restituite chiamando [**WPUCloseThread.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread)

 

 
