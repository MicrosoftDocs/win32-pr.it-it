---
description: Windows Sockets 2 introduce I/O sovrapposti e richiede che tutti i provider di trasporto supportino questa funzionalità.
ms.assetid: 90d49171-e211-4426-aa56-88aaeac7c578
title: Input/output sovrapposto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8caa13dd3d50e4f0fdaa1b92fa8e99afd8e2e1
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "103886038"
---
# <a name="overlapped-inputoutput"></a>Input/output sovrapposto

Windows Sockets 2 introduce I/O sovrapposti e richiede che tutti i provider di trasporto supportino questa funzionalità. Le operazioni di I/O sovrapposte possono essere eseguite solo su socket creati tramite la funzione [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) con il flag WSA \_ \_ sovrapposto impostato e seguono il modello stabilito in Windows.

Per la ricezione, un client utilizza [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) o [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) per fornire i buffer in cui devono essere ricevuti i dati. Se uno o più buffer vengono inviati prima del momento in cui i dati sono stati ricevuti dalla rete, è possibile che i dati vengano inseriti nei buffer dell'utente immediatamente dopo l'arrivo, evitando in questo modo l'operazione di copia che altrimenti verrebbe eseguita. Se i dati arrivano quando i buffer di ricezione sono già stati pubblicati, vengono copiati immediatamente nei buffer dell'utente. Se i dati arrivano quando l'applicazione non dispone di buffer di ricezione, il provider di servizi ricorre allo stile sincrono dell'operazione in cui i dati in arrivo vengono memorizzati nel buffer internamente fino al momento in cui il client invia una chiamata di ricezione e quindi fornisce un buffer in cui i dati possono essere copiati. Un'eccezione è costituita dal caso in cui l'applicazione utilizza [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) per impostare la dimensione del buffer di ricezione su zero. In questo caso, i protocolli affidabili consentono di ricevere solo i dati quando i buffer dell'applicazione sono stati inviati e i dati su protocolli non affidabili andranno perduti.

Sul lato di invio, i client usano [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) o [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) per fornire i puntatori ai buffer pieni e quindi accettano di non disturbare i buffer in alcun modo finché la rete non ha utilizzato il contenuto del buffer.

Le chiamate di invio e ricezione sovrapposte vengono restituite immediatamente. Un valore restituito pari a zero indica che l'operazione di I/O è stata completata immediatamente e che l'indicazione di completamento corrispondente è già stata eseguita. Ovvero l'oggetto evento associato è stato segnalato o la routine di completamento è stata accodata tramite [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Un valore restituito dell'errore del SOCKET \_ associato a un codice di errore di i/o WSA \_ \_ in sospeso indica che l'operazione sovrapposta è stata avviata correttamente e che verrà fornita un'indicazione successiva quando vengono utilizzati i buffer di invio o quando vengono riempiti i buffer di ricezione. Qualsiasi altro codice di errore indica che l'operazione sovrapposta non è stata avviata correttamente e che l'indicazione di completamento non sarà imminente.

È possibile sovrapporre le operazioni di invio e ricezione. Le funzioni receive possono essere richiamate più volte per inserire i buffer di ricezione in preparazione ai dati in ingresso e le funzioni di invio possono essere richiamate più volte per accodare più buffer da inviare. Si noti che, mentre una serie di buffer di invio sovrapposti viene inviata nell'ordine specificato, le indicazioni di completamento corrispondenti possono verificarsi in un ordine diverso. Analogamente, sul lato ricevente, i buffer verranno compilati nell'ordine in cui vengono forniti, ma le indicazioni di completamento possono verificarsi in un ordine diverso.

Per [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))è disponibile anche la funzionalità di completamento posticipato dell'I/O sovrapposto.

## <a name="delivering-completion-indications"></a>Recapito delle indicazioni di completamento

I provider di servizi hanno due modi per indicare il completamento sovrapposto: l'impostazione di un oggetto evento specificato dal client o la chiamata di una routine di completamento specificata dal client. In entrambi i casi, una struttura di dati, [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped), è associata a ogni operazione sovrapposta. Questa struttura viene allocata dal client e utilizzata per indicare quale oggetto evento (se presente) deve essere impostato quando si verifica il completamento. La struttura **WSAOVERLAPPED** può essere usata dal provider di servizi come posizione in cui archiviare un handle per i risultati (ad esempio, il numero di byte trasferiti, i flag aggiornati, i codici di errore e così via) per una particolare operazione sovrapposta. Per ottenere questi risultati i client devono richiamare [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult), passando un puntatore alla struttura sovrapposta corrispondente.

Se per una determinata richiesta di I/O sovrapposta è selezionata l'indicazione di completamento basato su eventi, la routine [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) può essere utilizzata dai client per eseguire il polling o attendere il completamento dell'operazione sovrapposta. Se per una particolare richiesta di I/O sovrapposta è selezionata l'indicazione di completamento basato su routine, è disponibile solo l'opzione di polling di **WSPGetOverlappedResult** . Un client può inoltre utilizzare altri mezzi per attendere (ad esempio, l'utilizzo di [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)) fino a quando l'oggetto evento corrispondente non è stato segnalato o la routine di completamento specificata è stata richiamata dal provider di servizi. Una volta indicato il completamento, il client può richiamare **WSPGetOverlappedResult**, con la previsione che la chiamata venga completata immediatamente.

## <a name="invoking-socket-io-completion-routines"></a>Richiamo di routine di completamento I/O socket

Se il parametro *il lpCompletionRoutine* di un'operazione sovrapposta non è **null**, è responsabilità del provider di servizi disporre la chiamata della routine di completamento specificata dal client al termine dell'operazione sovrapposta. Poiché la routine di completamento deve essere eseguita nel contesto dello stesso thread che ha avviato l'operazione sovrapposta, non può essere richiamata direttamente dal provider di servizi. Il \_32.DLL WS2 offre un meccanismo APC (Asynchronous Procedure Call) per facilitare la chiamata delle routine di completamento.

Un provider di servizi dispone che una funzione venga eseguita nel thread appropriato chiamando [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc). Questa funzione può essere chiamata da qualsiasi contesto di processo e thread, anche da un contesto diverso dal thread e dal processo utilizzati per avviare l'operazione sovrapposta.

[**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) accetta come parametri di input un puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) , un puntatore a una funzione APC da richiamare e un valore di contesto a 32 bit che viene successivamente passato alla funzione APC. I provider di servizi vengono sempre forniti con un puntatore alla struttura **WSATHREADID** corretta tramite il parametro *lpThreadId* alla funzione Overlapped. Il provider deve archiviare la struttura **WSATHREADID** localmente e fornire un puntatore a questa copia della struttura **WSATHREADID** come parametro di input per **WPUQueueApc**. Una volta che la funzione **WPUQueueApc** restituisce, il provider può eliminare la propria copia di **WSATHREADID**.

La procedura [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) Accoda semplicemente informazioni sufficienti per chiamare la funzione APC indicata con i parametri specificati, ma non la chiama. Quando il thread di destinazione entra in uno stato di attesa di avviso, queste informazioni vengono rimossi dalla coda e viene eseguita una chiamata alla funzione APC nel contesto del thread e del processo di destinazione. Poiché il meccanismo APC supporta solo un singolo valore di contesto a 32 bit, la funzione APC non può essere la routine di completamento specificata dal client, che prevede più parametri. Il provider di servizi deve invece fornire un puntatore alla propria funzione APC che usa il valore di contesto fornito per accedere alle informazioni sui risultati necessarie per l'operazione sovrapposta, quindi richiama la routine di completamento specificata dal client.

Per i provider di servizi in cui un componente in modalità utente implementa I/O sovrapposti, un utilizzo tipico del meccanismo APC è il seguente:

-   Quando l'operazione di I/O viene completata, il provider alloca un buffer di piccole dimensioni e lo comprime con un puntatore alla procedura di completamento fornita dal client e ai valori dei parametri da passare alla procedura.
-   Accoda un APC, specificando il puntatore al buffer come valore di contesto e la relativa procedura intermedia come procedura di destinazione.
-   Quando il thread di destinazione immette lo stato di attesa di avviso, la procedura intermedia del provider di servizi viene chiamata nel contesto del thread appropriato.
-   Con la procedura intermedia è sufficiente decomprimere i parametri, deallocare il buffer e chiamare la procedura di completamento fornita dal client.
-   Per i provider di servizi in cui un componente in modalità kernel implementa l'I/O sovrapposto, un'implementazione tipica è simile, ad eccezione del fatto che l'implementazione userà interfacce kernel standard per accodare l'APC.

La descrizione delle interfacce kernel pertinenti esula dall'ambito della specifica di Windows Sockets 2.

> [!Note]  
> I provider di servizi devono consentire ai client di Windows Sockets 2 di richiamare le operazioni di invio e ricezione dall'interno del contesto della routine di completamento I/O del socket e garantiscono che per un socket specifico, le routine di completamento I/O non saranno nidificate.

 

In alcuni casi, un provider di servizi su più livelli potrebbe dover avviare e completare le operazioni sovrapposte dall'interno di un thread di lavoro interno. In questo caso, un [**WSATHREADID**](/windows/desktop/api/Ws2spi/ns-ws2spi-wsathreadid) non sarebbe disponibile da una chiamata di funzione in entrata. L'interfaccia del provider di servizi fornisce una chiamata [**WPUOpenCurrentThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuopencurrentthread)per ottenere un **WSATHREADID** per il thread corrente. Quando questo **WSATHREADID** non è più necessario, le relative risorse devono essere restituite chiamando [**WPUCloseThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread).

 

 
