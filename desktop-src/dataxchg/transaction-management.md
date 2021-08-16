---
title: Gestione delle transazioni (Exchange)
description: Questo argomento illustra come un client può inviare transazioni per ottenere dati e servizi dal server.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Windows Interfaccia utente,Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), transazioni
- DDE (Dynamic Data Exchange), transazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Windows Interfaccia utente,Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange Management Library (DDEML), transactions
- DDEML (Dynamic Data Exchange Management Library), transazioni
- scambio di dati, Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange (DDE), richiedere transazioni
- DDE (Dynamic Data Exchange), richiedere transazioni
- Dynamic Data Exchange Management Library (DDEML), richiedere transazioni
- DDEML (Dynamic Data Exchange Management Library), richiedere transazioni
- Dynamic Data Exchange (DDE), transazioni di poke
- transazioni DDE (Dynamic Data Exchange), poke
- Dynamic Data Exchange Management Library (DDEML), transazioni di poke
- DDEML (Dynamic Data Exchange Management Library), transazioni di poke
- Dynamic Data Exchange (DDE), consigliare le transazioni
- DDE (Dynamic Data Exchange), consigliare le transazioni
- Dynamic Data Exchange Management Library (DDEML), consigliare le transazioni
- DDEML (Dynamic Data Exchange Management Library), consigliare le transazioni
- Dynamic Data Exchange (DDE), eseguire transazioni
- DDE (Dynamic Data Exchange), eseguire transazioni
- Dynamic Data Exchange Management Library (DDEML), eseguire transazioni
- DDEML (Dynamic Data Exchange Management Library), eseguire transazioni
- Dynamic Data Exchange (DDE), transazioni sincrone
- DDE (Dynamic Data Exchange), transazioni sincrone
- Dynamic Data Exchange Management Library (DDEML), transazioni sincrone
- DDEML (Dynamic Data Exchange Management Library), transazioni sincrone
- Dynamic Data Exchange (DDE), transazioni asincrone
- DDE (Dynamic Data Exchange), transazioni asincrone
- Dynamic Data Exchange Management Library (DDEML), transazioni asincrone
- DDEML (Dynamic Data Exchange Management Library), transazioni asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5065c9e909a4589cd7d2d157fc1151c2efd42a4ddfc3c29d84fd26f0ea184dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128574"
---
# <a name="transaction-management-data-exchange"></a>Gestione delle transazioni (Exchange)

Dopo aver stabilito una conversazione con un server, un client può inviare transazioni per ottenere dati e servizi dal server.

Negli argomenti seguenti vengono descritti i tipi di transazioni che i client possono usare per interagire con un server.

-   [Richiedi transazione](#request-transaction)
-   [Transazione poke](#poke-transaction)
-   [Avvisa transazione](#advise-transaction)
-   [Esegui transazione](#execute-transaction)
-   [Transazioni sincrone e asincrone](#synchronous-and-asynchronous-transactions)
-   [Controllo delle transazioni](#transaction-control)
-   [Classi di transazione](#transaction-classes)
-   [Tipi di transazione](#transaction-types)

## <a name="request-transaction"></a>Richiedi transazione

Un'applicazione client può usare la [**transazione XTYP \_ REQUEST**](xtyp-request.md) per richiedere un elemento di dati a un'applicazione server. Il client chiama la [**funzione DdeClientTransaction,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) specificando **XTYP \_ REQUEST** come tipo di transazione e specificando l'elemento di dati necessario per l'applicazione.

La Dynamic Data Exchange Management Library (DDEML) passa la transazione [**XTYP \_ REQUEST**](xtyp-request.md) al server, specificando il nome dell'argomento, il nome dell'elemento e il formato dei dati richiesti dal client. Se il server supporta l'argomento, l'elemento e il formato richiesti, il server deve restituire un handle di dati che identifica il valore corrente dell'elemento. DDEML passa questo handle al client come valore restituito da [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) Il server deve restituire **NULL** se non supporta l'argomento, l'elemento o il formato richiesto.

[**DdeClientTransaction usa**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) il *parametro lpdwResult* per restituire un flag di stato della transazione al client. Se il server non elabora la transazione [**XTYP \_ REQUEST,**](xtyp-request.md) **DdeClientTransaction** restituisce **NULL** e *lpdwResult* punta al flag DDE \_ FNOTPROCESSED o DDE \_ FBUSY. Se viene restituito il flag DDE FNOTPROCESSED, il client non è in grado di determinare il motivo per cui il server non \_ ha elaborato la transazione.

Se un server non supporta la [**transazione XTYP \_ REQUEST,**](xtyp-request.md) deve specificare il flag di filtro CBF \_ FAIL REQUESTS nella funzione \_ [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Questo flag impedisce a DDEML di inviare la transazione al server.

## <a name="poke-transaction"></a>Transazione poke

Un client può inviare dati non richiesta a un server usando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) per inviare una transazione [**\_ POKE XTYP**](xtyp-poke.md) alla funzione di callback di un server.

L'applicazione client crea innanzitutto un buffer contenente i dati da inviare al server e quindi passa un puntatore al buffer come parametro a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). In alternativa, il client può usare la [**funzione DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) per ottenere un handle di dati che identifica i dati e quindi passare l'handle **a DdeClientTransaction.** In entrambi i casi, il client specifica anche il nome dell'argomento, il nome dell'elemento e il formato dei dati quando chiama **DdeClientTransaction.**

DDEML passa la transazione [**\_ POKE XTYP**](xtyp-poke.md) al server, specificando il nome dell'argomento, il nome dell'elemento e il formato dei dati richiesti dal client. Per accettare l'elemento di dati e il formato, il server deve restituire DDE \_ FACK. Per rifiutare i dati, il server deve restituire DDE \_ FNOTPROCESSED. Se il server è troppo occupato per accettare i dati, il server deve restituire DDE \_ FBUSY.

Quando [**viene restituito DdeClientTransaction,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) il client può usare il *parametro lpdwResult* per accedere al flag di stato della transazione. Se il flag è DDE \_ FBUSY, il client deve inviare nuovamente la transazione in un secondo momento.

Se un server non supporta la transazione [**\_ POKE XTYP,**](xtyp-poke.md) deve specificare il flag di filtro CBF \_ FAIL \_ POKES in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Questo flag impedisce a DDEML di inviare la transazione al server.

## <a name="advise-transaction"></a>Avvisa transazione

Un'applicazione client può usare DDEML per stabilire uno o più collegamenti agli elementi in un'applicazione server. Quando viene stabilito un collegamento di questo tipo, il server invia aggiornamenti periodici sull'elemento collegato al client (in genere, ogni volta che il valore dell'elemento associato all'applicazione server cambia). Il collegamento stabilisce un ciclo di consulenza tra le due applicazioni che rimane attivo fino a quando il client non lo termina.

Esistono due tipi di cicli di consulenza: "hot" e "warm". In un ciclo hot advise, il server invia immediatamente un handle di dati che identifica il valore modificato. In un ciclo warm advise, il server notifica al client che il valore dell'elemento è stato modificato ma non invia l'handle di dati fino a quando il client non lo richiede.

Un client può richiedere un ciclo hot advise con un server specificando il tipo di transazione [**\_ ADVSTART XTYP**](xtyp-advstart.md) in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Per richiedere un ciclo warm advise, il client deve combinare il flag NODATA XTYPF con il tipo di \_ **\_ transazione XTYP ADVSTART.** In entrambi gli eventi, DDEML passa la transazione **\_ ADVSTART XTYP** alla funzione di callback Dynamic Data Exchange (DDE) del server. La funzione di callback DDE del server deve esaminare i parametri che accompagnano la transazione **\_ ADVSTART XTYP** (inclusi il formato richiesto, il nome dell'argomento e il nome dell'elemento) e quindi restituire **TRUE** per consentire al ciclo advise o **FALSE** di negarla.

Dopo aver stabilito un ciclo di consulenza, l'applicazione server deve chiamare la [**funzione DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) ogni volta che cambia il valore dell'elemento associato al nome dell'elemento richiesto. Questa chiamata comporta l'invio di una transazione [**\_ ADVREQ XTYP**](xtyp-advreq.md) alla funzione di callback DDE del server. La funzione di callback DDE del server deve restituire un handle di dati che identifica il nuovo valore dell'elemento di dati. DDEML notifica quindi al client che l'elemento specificato è stato modificato inviando la transazione [**\_ ADVDATA XTYP**](xtyp-advdata.md) alla funzione di callback DDE del client.

Se il client ha richiesto un ciclo hot advise, DDEML passa l'handle di dati all'elemento modificato al client durante la [**transazione \_ ADVDATA XTYP.**](xtyp-advdata.md) In caso contrario, il client può inviare una [**\_ transazione XTYP REQUEST**](xtyp-request.md) per ottenere l'handle di dati.

È possibile che un server invii gli aggiornamenti più velocemente di quanto un client possa elaborare i nuovi dati. La velocità degli aggiornamenti può essere un problema per un client che deve eseguire lunghe operazioni di elaborazione sui dati. In questo caso, il client deve specificare il flag ACKREQ XTYPF \_ quando richiede un ciclo di consulenza. Questo flag fa sì che il server attenda che il client riconosca che ha ricevuto ed elaborato un elemento di dati prima che il server invii l'elemento di dati successivo. I cicli di consulenza stabiliti con il flag ACKREQ XTYPF sono più affidabili con server veloci, ma possono \_ occasionalmente perdere gli aggiornamenti. È garantito che i cicli di consulenza stabiliti senza il flag ACKREQ XTYPF non mancheranno di perdere gli aggiornamenti purché il client si acconti \_ al server.

Un client può terminare un ciclo advise specificando il tipo di transazione [**\_ ADVSTOP XTYP**](xtyp-advstop.md) in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).

Se un server non supporta i cicli advise, deve specificare il flag di filtro CBF \_ FAIL \_ ADVISES nella [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Questo flag impedisce a DDEML di inviare le transazioni [**\_ XTYP ADVSTART**](xtyp-advstart.md) e [**XTYP \_ ADVSTOP**](xtyp-advstop.md) al server.

## <a name="execute-transaction"></a>Esegui transazione

Un client può usare la [**transazione EXECUTE \_ XTYP**](xtyp-execute.md) per fare in modo che un server esere un comando o una serie di comandi.

Per eseguire un comando server, il client crea innanzitutto un buffer contenente una stringa di comando per l'esecuzione del server e quindi passa un puntatore al buffer o un handle di dati che identifica il buffer quando chiama [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Altri parametri obbligatori includono l'handle di conversazione, l'handle della stringa del nome dell'elemento, la specifica del formato e il [**tipo di transazione \_ EXECUTE XTYP.**](xtyp-execute.md) Un'applicazione che crea un handle di dati per passare i dati di esecuzione deve specificare **NULL** per il parametro *hszItem* della [**funzione DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) e zero per il *parametro uFmt.*

DDEML passa la transazione [**\_ EXECUTE XTYP**](xtyp-execute.md) alla funzione di callback DDE del server e specifica il nome del formato, l'handle di conversazione, il nome dell'argomento e l'handle di dati che identificano la stringa di comando. Se il server supporta il comando, deve usare la funzione [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) per ottenere un puntatore alla stringa di comando, eseguire il comando e quindi restituire DDE \_ FACK. Se il server non supporta il comando o non è in grado di completare la transazione, deve restituire DDE \_ FNOTPROCESSED. Il server deve restituire DDE \_ FBUSY se è troppo occupato per completare la transazione.

In generale, la funzione di callback di un server deve elaborare la [**transazione \_ EXECUTE XTYP**](xtyp-execute.md) prima di restituire con le eccezioni seguenti:

1.  Quando il comando passato con la transazione [**\_ EXECUTE XTYP**](xtyp-execute.md) richiede al server di terminare, il server non deve terminare fino a quando la relativa funzione di callback non viene restituita dall'elaborazione **di XTYP \_ EXECUTE.**
2.  Se il server deve eseguire un'operazione, ad esempio l'elaborazione di una finestra di dialogo o di una transazione DDE che potrebbe causare problemi di ricorsione DDEML, il server deve restituire il codice restituito CBR BLOCK per bloccare la transazione di esecuzione, eseguire l'operazione e quindi riprendere l'elaborazione della transazione \_ di esecuzione.

Quando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) restituisce un risultato, il client può usare il parametro *lpdwResult* per accedere al flag di stato della transazione. Se il flag è DDE \_ FBUSY, il client deve inviare nuovamente la transazione in un secondo momento.

Se un server non supporta la transazione [**\_ EXECUTE XTYP,**](xtyp-execute.md) deve specificare il flag di filtro CBF \_ FAIL \_ EXECUTES nella [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) In questo modo si impedisce a DDEML di inviare la transazione al server.

## <a name="synchronous-and-asynchronous-transactions"></a>Transazioni sincrone e asincrone

Un client può inviare transazioni sincrone o asincrone. In una transazione sincrona, il client specifica un valore di timeout che indica la quantità massima di tempo di attesa per l'elaborazione della transazione da parte del server. [**DdeClientTransaction non**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) restituisce valori finché il server non elabora la transazione, la transazione ha esito negativo o il valore di timeout scade. Il client specifica il valore di timeout quando chiama **DdeClientTransaction.**

Durante una transazione sincrona, il client entra in un ciclo modale in attesa dell'elaborazione della transazione. Il client può comunque elaborare l'input dell'utente, ma non può inviare un'altra transazione sincrona fino al completamento [**di DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)

Un client invia una transazione asincrona specificando il \_ flag TIMEOUT ASYNC in [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) La funzione restituisce un risultato dopo l'inizio della transazione, passando un identificatore di transazione al client. Quando il server termina l'elaborazione della transazione asincrona, DDEML invia una [**transazione \_ XTYP XACT \_ COMPLETE**](xtyp-xact-complete.md) al client. Uno dei parametri che DDEML passa al client durante la transazione **\_ XTYP XACT \_ COMPLETE** è l'identificatore della transazione. Confrontando questo identificatore di transazione con l'identificatore restituito da **DdeClientTransaction**, il client identifica la transazione asincrona che il server ha completato l'elaborazione.

Un client può usare la [**funzione DdeSetUserHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) come supporto per l'elaborazione di una transazione asincrona. Questa funzione consente a un client di associare un valore definito dall'applicazione a un handle di conversazione e a un identificatore di transazione. Il client può usare [**la funzione DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante la [**transazione \_ XTYP XACT \_ COMPLETE**](xtyp-xact-complete.md) per ottenere il valore definito dall'applicazione. A causa di questa funzione, un'applicazione non deve gestire un elenco di identificatori di transazioni attive.

Quando un client completa correttamente una richiesta di dati usando una transazione sincrona, DDEML non è in grado di indicare quando il client ha terminato di usare i dati ricevuti. L'applicazione client deve passare l'handle di dati ricevuto alla funzione [**DdeFreeDataHandle,**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) notificando a DDEML che l'handle non verrà più usato. Gli handle di dati restituiti dalle transazioni sincrone sono effettivamente di proprietà del client.

Se un server non elabora una transazione asincrona in modo appropriato, il client può abbandonare la transazione chiamando la [**funzione DdeAbandonTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) DDEML rilascia tutte le risorse associate alla transazione ed elimina i risultati della transazione al termine dell'elaborazione da parte del server. Un timeout durante una transazione sincrona annulla in modo efficace la transazione.

Il metodo di transazione asincrona viene fornito per le applicazioni che devono inviare un volume elevato di transazioni DDE eseguendo contemporaneamente una notevole quantità di elaborazione, ad esempio l'esecuzione di calcoli. Il metodo asincrono è utile anche nelle applicazioni che devono interrompere temporaneamente l'elaborazione delle transazioni DDE in modo che possano completare altre attività senza interruzioni. Nella maggior parte delle altre situazioni, un'applicazione deve usare il metodo sincrono.

Le transazioni sincrone sono più semplici da gestire e sono più veloci delle transazioni asincrone. Tuttavia, è possibile eseguire una sola transazione sincrona alla volta, mentre molte transazioni asincrone possono essere eseguite contemporaneamente. Con le transazioni sincrone, un server lento può fare in modo che un client rimanga inattivo mentre è in attesa di una risposta. Inoltre, le transazioni sincrone determinano l'immissione da parte del client di un ciclo modale che potrebbe ignorare il filtro messaggi nel ciclo di messaggi dell'applicazione.

Se il client ha installato una procedura hook per filtrare i messaggi, ovvero è stato specificato il tipo hook WH MSGFILTER in una chiamata alla funzione \_ [**SetWindowsHookEx,**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) una transazione sincrona non causerà il bypass della procedura hook da parte del sistema. Quando si verifica un evento di input mentre il client è in attesa del termine di una transazione sincrona, la procedura hook riceve un codice \_ hook MSGF DDEMGR. Il rischio principale di usare un ciclo modale di transazione sincrono è che un ciclo modale creato da una finestra di dialogo può interferire con il relativo funzionamento. Le transazioni asincrone devono essere sempre utilizzate quando DDEML viene usato da una DLL.

## <a name="transaction-control"></a>Controllo delle transazioni

Un'applicazione può sospendere le transazioni alla relativa funzione di callback DDE, sia quelle associate a un handle di conversazione specifico che tutte le transazioni indipendentemente dall'handle di conversazione. Questa funzionalità è utile quando un'applicazione riceve una transazione che richiede una lunga elaborazione. In tal caso, l'applicazione può restituire il codice restituito CBR BLOCK per sospendere le future transazioni associate all'handle di conversazione della transazione, in modo che l'applicazione sia libera di elaborare \_ altre conversazioni.

Al termine dell'elaborazione, l'applicazione chiama [**la funzione DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) per riprendere le transazioni associate alla conversazione sospesa. La **chiamata di DdeEnableCallback** fa sì che DDEML invii nuovamente la transazione che ha comportato la sospensione della conversazione da parte dell'applicazione. Pertanto, l'applicazione deve archiviare il risultato della transazione in modo che possa ottenere e restituire il risultato senza rielaborare la transazione.

Un'applicazione può sospendere tutte le transazioni associate a un handle di conversazione specifico specificando l'handle e il flag EC DISABLE in una chiamata \_ a [**DdeEnableCallback.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) Specificando un handle **NULL,** un'applicazione può sospendere tutte le transazioni per tutte le conversazioni.

Quando una conversazione è stata sospesa, DDEML salva le transazioni per la conversazione in una coda di transazioni. Quando l'applicazione riabilita la conversazione, DDEML rimuove le transazioni salvate dalla coda e passa ogni transazione alla funzione di callback appropriata. La capacità della coda delle transazioni è elevata, ma un'applicazione deve riabilitare una conversazione sospesa il prima possibile per evitare la perdita di transazioni.

Un'applicazione può riprendere la normale elaborazione delle transazioni specificando il flag EC \_ ENABLEALL in [**DdeEnableCallback.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) Per una ripresa più controllata dell'elaborazione delle transazioni, l'applicazione può specificare il flag EC \_ ENABLEONE. Questo flag rimuove una transazione dalla coda delle transazioni e la passa alla funzione di callback appropriata. Dopo l'elaborazione della transazione, tutte le conversazioni vengono nuovamente disabilitate.

Se nella chiamata \_ a [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)vengono specificati il flag EC ENABLEONE e un handle di conversazione, solo tale conversazione viene bloccata dopo l'elaborazione della transazione. Se viene specificato un handle di conversazione **NULL,** tutte le conversazioni vengono bloccate dopo l'elaborazione di una transazione in qualsiasi conversazione.

## <a name="transaction-classes"></a>Classi di transazioni

DDEML include quattro classi di transazioni. Ogni classe è identificata da una costante che inizia con il prefisso \_ XCLASS. Le classi sono definite nel file di intestazione DDEML. Il valore della classe viene combinato con il valore del tipo di transazione e viene passato alla funzione di callback DDE dell'applicazione ricevente.

La classe di una transazione determina il valore restituito che una funzione di callback deve restituire se elabora la transazione. I valori restituiti e i tipi di transazione seguenti sono associati a ognuna delle quattro classi di transazione.



| Classe                | Valore restituito                                                     | Transazione                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XCLASS \_ BOOL         | **TRUE** o **FALSE**                                            | [**XTYP \_ ADVSTART**](xtyp-advstart.md)<br/> [**XTYP \_ CONNECT**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| XCLASS \_ DATA         | Handle di dati, codice restituito BLOCK CBR \_ o **NULL**           | [**XTYP \_ ADVREQ**](xtyp-advreq.md)<br/> [**RICHIESTA \_ XTYP**](xtyp-request.md)<br/> [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| FLAG \_ XCLASS        | Un flag di transazione: DDE \_ FACK, DDE \_ FBUSY o DDE \_ FNOTPROCESSED | [**XTYP \_ ADVDATA**](xtyp-advdata.md)<br/> [**XTYP \_ EXECUTE**](xtyp-execute.md)<br/> [**XTYP \_ POKE**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| NOTIFICA \_ XCLASS | Nessuno                                                             | [**XTYP \_ ADVSTOP**](xtyp-advstop.md)<br/> [**CONFERMA DI XTYP \_ \_ CONNECT**](xtyp-connect-confirm.md)<br/> [**DISCONNESSIONE \_ XTYP**](xtyp-disconnect.md)<br/> [**ERRORE \_ XTYP**](xtyp-error.md)<br/> [**REGISTRO \_ XTYP**](xtyp-register.md)<br/> [**XTYP \_ UNREGISTER**](xtyp-unregister.md)<br/> [**XTYP \_ XACT \_ COMPLETE**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>Tipi di transazione

Ogni tipo di transazione DDE dispone di un ricevitore e di un'attività associata che determina la generazione di ogni tipo da parte di DDEML.



| Tipo di transazione                                       | Ricevitore                   | Causa                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XTYP \_ ADVDATA**](xtyp-advdata.md)                  | Client                     | Un server ha risposto a una [**transazione \_ ADVREQ XTYP**](xtyp-advreq.md) tramite la restituzione di un handle di dati.                                                                          |
| [**XTYP \_ ADVREQ**](xtyp-advreq.md)                    | Server                     | Un server denominato [**funzione DdePostAdvise,**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) che indica che il valore di un elemento di dati in un ciclo di consulenza è stato modificato.                                  |
| [**XTYP \_ ADVSTART**](xtyp-advstart.md)                | Server                     | Un client ha specificato [**il tipo di \_ transazione ADVSTART XTYP**](xtyp-advstart.md) in una chiamata alla [**funzione DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)               |
| [**XTYP \_ ADVSTOP**](xtyp-advstop.md)                  | Server                     | Un client ha specificato il [**tipo di \_ transazione ADVSTOP XTYP**](xtyp-advstop.md) in una chiamata a [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)                              |
| [**XTYP \_ CONNECT**](xtyp-connect.md)                  | Server                     | Un client ha chiamato [**la funzione DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e ha specificato un nome di servizio e un nome di argomento supportati dal server.                                            |
| [**CONFERMA DI XTYP \_ \_ CONNECT**](xtyp-connect-confirm.md) | Server                     | Il server ha **restituito TRUE** in risposta a [**una \_ transazione XTYP CONNECT**](xtyp-connect.md) o [**XTYP \_ WILDCONNECT.**](xtyp-wildconnect.md)                            |
| [**DISCONNESSIONE \_ XTYP**](xtyp-disconnect.md)            | Client/Server              | Partner in una conversazione denominata [**funzione DdeDisconnect,**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) che fa sì che entrambi i partner ricevano questa transazione.                                    |
| [**ERRORE \_ XTYP**](xtyp-error.md)                      | Client/Server              | Si è verificato un errore critico. DDEML potrebbe non avere risorse sufficienti per continuare.                                                                                       |
| [**XTYP \_ EXECUTE**](xtyp-execute.md)                  | Server                     | Un client ha specificato il [**tipo di \_ transazione EXECUTE XTYP**](xtyp-execute.md) in una chiamata a [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)                              |
| [**MONITORAGGIO \_ XTYP**](xtyp-monitor.md)                  | Applicazione di monitoraggio DDE | Si è verificato un evento DDE nel sistema. Per altre informazioni sulle applicazioni di monitoraggio DDE, vedere [Monitoraggio delle applicazioni](monitoring-applications.md).                       |
| [**XTYP \_ POKE**](xtyp-poke.md)                        | Server                     | Un client ha specificato il [**tipo di \_ transazione POKE XTYP**](xtyp-poke.md) in una chiamata a [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)                                    |
| [**REGISTRO \_ XTYP**](xtyp-register.md)                | Client/Server              | Un'applicazione server ha usato [**la funzione DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per registrare un nome di servizio.                                                                   |
| [**RICHIESTA \_ XTYP**](xtyp-request.md)                  | Server                     | Un client ha specificato il [**tipo di \_ transazione XTYP REQUEST**](xtyp-request.md) in una chiamata a [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)                              |
| [**XTYP \_ UNREGISTER**](xtyp-unregister.md)            | Client/Server              | Un'applicazione server ha [**usato DdeNameService per**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) annullare la registrazione di un nome di servizio.                                                                              |
| [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)          | Server                     | Un client denominato [**funzione DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) o [**DdeConnectList,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) che specifica **NULL** per il nome del servizio, il nome dell'argomento o entrambi. |
| [**XTYP \_ XACT \_ COMPLETE**](xtyp-xact-complete.md)     | Client                     | Una transazione asincrona, inviata quando il client ha specificato il flag TIMEOUT ASYNC in una chiamata \_ a [**DdeClientTransaction,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)si è conclusa.         |



 

 

