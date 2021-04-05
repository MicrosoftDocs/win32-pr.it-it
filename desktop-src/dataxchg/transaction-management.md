---
title: Gestione delle transazioni (scambio di dati)
description: In questo argomento viene illustrato come un client può inviare transazioni per ottenere i dati e i servizi dal server.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), transazioni
- DDE (Dynamic Data Exchange), transazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Libreria di gestione Dynamic Data Exchange (DDEML), transazioni
- DDEML (libreria di gestione Dynamic Data Exchange), transazioni
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), transazioni di richiesta
- DDE (Dynamic Data Exchange), transazioni di richiesta
- Libreria di gestione Dynamic Data Exchange (DDEML), transazioni di richiesta
- DDEML (libreria di gestione Dynamic Data Exchange), transazioni di richiesta
- Dynamic Data Exchange (DDE), transazioni poke
- DDE (Dynamic Data Exchange), transazioni poke
- Libreria di gestione Dynamic Data Exchange (DDEML), transazioni poke
- DDEML (libreria di gestione Dynamic Data Exchange), transazioni poke
- Dynamic Data Exchange (DDE), transazioni di notifica
- DDE (Dynamic Data Exchange), transazioni di notifica
- Libreria di gestione Dynamic Data Exchange (DDEML), transazioni di notifica
- DDEML (libreria di gestione Dynamic Data Exchange), transazioni di notifica
- Dynamic Data Exchange (DDE), esecuzione di transazioni
- DDE (Dynamic Data Exchange), esecuzione di transazioni
- Libreria di gestione Dynamic Data Exchange (DDEML), esecuzione di transazioni
- DDEML (libreria di gestione Dynamic Data Exchange), esecuzione di transazioni
- Dynamic Data Exchange (DDE), transazioni sincrone
- DDE (Dynamic Data Exchange), transazioni sincrone
- Libreria di gestione Dynamic Data Exchange (DDEML), transazioni sincrone
- DDEML (libreria di gestione Dynamic Data Exchange), transazioni sincrone
- Dynamic Data Exchange (DDE), transazioni asincrone
- DDE (Dynamic Data Exchange), transazioni asincrone
- Libreria di gestione Dynamic Data Exchange (DDEML), transazioni asincrone
- DDEML (libreria di gestione Dynamic Data Exchange), transazioni asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570aa48b4dcdbb31855b3e1b15a091908feb2ba4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046885"
---
# <a name="transaction-management-data-exchange"></a>Gestione delle transazioni (scambio di dati)

Dopo aver stabilito una conversazione con un server, un client può inviare le transazioni per ottenere i dati e i servizi dal server.

Negli argomenti seguenti vengono descritti i tipi di transazioni che i client possono utilizzare per interagire con un server.

-   [Transazione di richiesta](#request-transaction)
-   [Transazione poke](#poke-transaction)
-   [Notifica transazione](#advise-transaction)
-   [Esegui transazione](#execute-transaction)
-   [Transazioni sincrone e asincrone](#synchronous-and-asynchronous-transactions)
-   [Controllo transazione](#transaction-control)
-   [Classi di transazione](#transaction-classes)
-   [Tipi di transazione](#transaction-types)

## <a name="request-transaction"></a>Transazione di richiesta

Un'applicazione client può utilizzare la transazione di [**\_ richiesta XTYP**](xtyp-request.md) per richiedere un elemento dati da un'applicazione server. Il client chiama la funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , specificando la **\_ richiesta XTYP** come tipo di transazione e specificando l'elemento dati necessario per l'applicazione.

La libreria di gestione Dynamic Data Exchange (DDEML) passa la transazione della [**\_ richiesta XTYP**](xtyp-request.md) al server, specificando il nome dell'argomento, il nome dell'elemento e il formato dati richiesti dal client. Se il server supporta l'argomento, l'elemento e il formato richiesti, il server deve restituire un handle di dati che identifichi il valore corrente dell'elemento. Il DDEML passa questo handle al client come valore restituito da [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Il server deve restituire **null** se non supporta l'argomento, l'elemento o il formato richiesto.

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) usa il parametro *lpdwResult* per restituire un flag di stato della transazione al client. Se il server non elabora la transazione [**di \_ richiesta XTYP**](xtyp-request.md) , **DdeClientTransaction** restituisce **null** e *LPDWRESULT* punta al \_ flag DDE FNOTPROCESSED o FBUSY DDE \_ . Se \_ viene restituito il flag DDE FNOTPROCESSED, il client non è in grado di determinare il motivo per cui il server non ha elaborato la transazione.

Se un server non supporta la transazione [**di \_ richiesta XTYP**](xtyp-request.md) , è necessario specificare il \_ \_ flag di filtro richieste non riuscite CBF nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Questo flag impedisce al DDEML di inviare la transazione al server.

## <a name="poke-transaction"></a>Transazione poke

Un client può inviare dati non richiesti a un server usando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) per inviare una transazione [**\_ poke XTYP**](xtyp-poke.md) alla funzione di callback di un server.

L'applicazione client crea innanzitutto un buffer che contiene i dati da inviare al server e quindi passa un puntatore al buffer come parametro a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). In alternativa, il client può usare la funzione [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) per ottenere un handle di dati che identifichi i dati e quindi passa l'handle a **DdeClientTransaction**. In entrambi i casi, il client specifica anche il nome dell'argomento, il nome dell'elemento e il formato dati quando chiama **DdeClientTransaction**.

Il DDEML passa la [**transazione \_ poke XTYP**](xtyp-poke.md) al server, specificando il nome dell'argomento, il nome dell'elemento e il formato dati richiesti dal client. Per accettare l'elemento dati e il formato, il server deve restituire \_ fack DDE. Per rifiutare i dati, il server deve restituire \_ FNOTPROCESSED DDE. Se il server è troppo occupato per accettare i dati, il server deve restituire il \_ FBUSY DDE.

Quando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) restituisce, il client può usare il parametro *lpdwResult* per accedere al flag di stato della transazione. Se il flag è \_ FBUSY DDE, il client deve inviare nuovamente la transazione in un secondo momento.

Se un server non supporta la transazione [**\_ poke XTYP**](xtyp-poke.md) , è necessario specificare il \_ \_ flag di filtro CBF Fail pokes in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Questo flag impedisce al DDEML di inviare questa transazione al server.

## <a name="advise-transaction"></a>Notifica transazione

Un'applicazione client può usare DDEML per stabilire uno o più collegamenti agli elementi in un'applicazione server. Quando viene stabilito un collegamento di questo tipo, il server invia aggiornamenti periodici sull'elemento collegato al client (in genere, ogni volta che viene modificato il valore dell'elemento associato all'applicazione server). Il collegamento stabilisce un ciclo di notifica tra le due applicazioni rimanenti fino a quando il client non la termina.

Esistono due tipi di cicli di notifica: "Hot" e "warm". In un ciclo Hot Advise, il server invia immediatamente un handle di dati che identifica il valore modificato. In un ciclo di avviso caldo, il server informa il client che il valore dell'elemento è stato modificato, ma non invia l'handle di dati fino a quando non viene richiesto dal client.

Un client può richiedere un ciclo Hot Advise con un server specificando il tipo di transazione [**XTYP \_ ADVSTART**](xtyp-advstart.md) in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Per richiedere un ciclo warm Advise, il client deve combinare il \_ flag NODATA XTYPF con il tipo di transazione **XTYP \_ ADVSTART** . In entrambi i casi, DDEML passa la **transazione \_ ADVSTART XTYP** alla funzione di callback di Dynamic Data Exchange (DDE) del server. La funzione di callback DDE del server deve esaminare i parametri che accompagnano la transazione **XTYP \_ ADVSTART** (inclusi il formato richiesto, il nome dell'argomento e il nome dell'elemento), quindi restituire **true** per consentire il ciclo Advise o **false** per negarlo.

Dopo la creazione di un ciclo di notifica, l'applicazione server deve chiamare la funzione [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) ogni volta che viene modificato il valore dell'elemento associato al nome dell'elemento richiesto. Questa chiamata comporta l'invio di una transazione [**\_ ADVREQ XTYP**](xtyp-advreq.md) alla funzione di callback DDE del server. La funzione di callback DDE del server deve restituire un handle di dati che identifichi il nuovo valore dell'elemento di dati. DDEML notifica quindi al client che l'elemento specificato è stato modificato inviando la transazione [**\_ ADVDATA XTYP**](xtyp-advdata.md) alla funzione di callback DDE del client.

Se il client ha richiesto un ciclo Hot Advise, DDEML passa l'handle di dati all'elemento modificato al client durante la transazione [**\_ ADVDATA XTYP**](xtyp-advdata.md) . In caso contrario, il client può inviare una transazione di [**\_ richiesta XTYP**](xtyp-request.md) per ottenere l'handle di dati.

È possibile che un server invii gli aggiornamenti più velocemente di quanto un client possa elaborare i nuovi dati. La velocità degli aggiornamenti può costituire un problema per un client che deve eseguire operazioni di elaborazione lunghe sui dati. In questo caso, il client deve specificare il \_ flag XTYPF ACKREQ quando richiede un ciclo di notifica. Questo flag fa in modo che il server attenda che il client riconosca la ricezione e l'elaborazione di un elemento di dati prima che il server invii l'elemento dati successivo. I cicli di notifica stabiliti con il \_ flag XTYPF ACKREQ sono più affidabili con i server veloci, ma possono occasionalmente mancare aggiornamenti. I cicli di notifica stabiliti senza il \_ flag ACKREQ di XTYPF sono garantiti per evitare la mancata disponibilità di aggiornamenti purché il client continui a usare il server.

Un client può terminare un ciclo di notifica specificando il tipo di transazione [**XTYP \_ ADVSTOP**](xtyp-advstop.md) in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).

Se un server non supporta i cicli di notifica, è necessario specificare il \_ \_ flag di filtro CBF Fail advises nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Questo flag impedisce al DDEML di inviare le transazioni [**XTYP \_ ADVSTART**](xtyp-advstart.md) e [**XTYP \_ ADVSTOP**](xtyp-advstop.md) al server.

## <a name="execute-transaction"></a>Esegui transazione

Un client può utilizzare [**XTYP \_ Execute**](xtyp-execute.md) Transaction per fare in modo che un server esegua un comando o una serie di comandi.

Per eseguire un comando server, il client crea innanzitutto un buffer che contiene una stringa di comando per il server da eseguire e quindi passa un puntatore al buffer o un handle di dati che identifica il buffer quando chiama [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Gli altri parametri obbligatori includono l'handle di conversazione, l'handle di stringa del nome dell'elemento, la specifica del formato e il tipo di transazione [**XTYP \_ Execute**](xtyp-execute.md) . Un'applicazione che crea un handle di dati per passare i dati di esecuzione deve specificare **null** per il parametro *HszItem* della funzione [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) e zero per il parametro *uFmt* .

DDEML passa [**XTYP \_ Execute**](xtyp-execute.md) Transaction alla funzione di callback DDE del server e specifica il nome del formato, l'handle di conversazione, il nome dell'argomento e l'handle di dati che identificano la stringa di comando. Se il server supporta il comando, deve usare la funzione [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) per ottenere un puntatore alla stringa di comando, eseguire il comando e quindi restituire \_ fack DDE. Se il server non supporta il comando o non è in grado di completare la transazione, deve restituire \_ FNOTPROCESSED DDE. Il server deve restituire \_ FBUSY DDE se è troppo occupato per completare la transazione.

In generale, la funzione di callback di un server deve elaborare [**XTYP \_ Execute**](xtyp-execute.md) Transaction prima di restituire con le eccezioni seguenti:

1.  Quando il comando passato con [**XTYP \_ Execute**](xtyp-execute.md) Transaction richiede che il server termini, il server non deve terminare fino a quando la funzione di callback non viene restituita dall'elaborazione **XTYP \_ Execute**.
2.  Se il server deve eseguire un'operazione, ad esempio l'elaborazione di una finestra di dialogo o di una transazione DDE che può causare problemi di ricorsione DDEML, il server deve restituire il \_ codice di blocco CBR per bloccare la transazione di esecuzione, eseguire l'operazione e quindi riprendere l'elaborazione dell'esecuzione della transazione.

Quando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) restituisce, il client può usare il parametro *lpdwResult* per accedere al flag di stato della transazione. Se il flag è \_ FBUSY DDE, il client deve inviare nuovamente la transazione in un secondo momento.

Se un server non supporta [**XTYP \_ Execute**](xtyp-execute.md) Transaction, deve specificare il \_ \_ flag di filtro CBF Fail executes nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . In questo modo si impedisce al DDEML di inviare la transazione al server.

## <a name="synchronous-and-asynchronous-transactions"></a>Transazioni sincrone e asincrone

Un client può inviare transazioni sincrone o asincrone. In una transazione sincrona, il client specifica un valore di timeout che indica il tempo massimo di attesa del server per l'elaborazione della transazione. [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) non restituisce alcun risultato finché il server non elabora la transazione, la transazione ha esito negativo o il valore di timeout scade. Il client specifica il valore di timeout quando chiama **DdeClientTransaction**.

Durante una transazione sincrona, il client immette un ciclo modale mentre è in attesa dell'elaborazione della transazione. Il client può comunque elaborare l'input dell'utente, ma non può inviare un'altra transazione sincrona finché non viene restituito [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .

Un client invia una transazione asincrona specificando il \_ flag async di timeout in [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). La funzione restituisce una volta iniziata la transazione, passando un identificatore di transazione al client. Al termine dell'elaborazione della transazione asincrona da parte del server, DDEML invia una transazione [**XTYP \_ XACT \_ complete**](xtyp-xact-complete.md) al client. Uno dei parametri che il DDEML passa al client durante la transazione **XTYP \_ XACT \_ complete** è l'identificatore della transazione. Confrontando questo identificatore di transazione con l'identificatore restituito da **DdeClientTransaction**, il client identifica la transazione asincrona completata dall'elaborazione del server.

Un client può utilizzare la funzione [**DdeSetUserHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) come supporto nell'elaborazione di una transazione asincrona. Questa funzione consente a un client di associare un valore definito dall'applicazione a un handle di conversazione e a un identificatore di transazione. Il client può utilizzare la funzione [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante la transazione [**XTYP \_ XACT \_ complete**](xtyp-xact-complete.md) per ottenere il valore definito dall'applicazione. A causa di questa funzione, un'applicazione non deve gestire un elenco di identificatori di transazioni attivi.

Quando un client completa correttamente una richiesta di dati tramite una transazione sincrona, DDEML non è in grado di stabilire quando il client ha terminato l'utilizzo dei dati ricevuti. L'applicazione client deve passare l'handle di dati ricevuto alla funzione [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) , notificando al DDEML che l'handle non verrà più usato. Gli handle di dati restituiti dalle transazioni sincrone sono di proprietà del client.

Se un server non elabora una transazione asincrona in modo tempestivo, il client può abbandonare la transazione chiamando la funzione [**DdeAbandonTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) . DDEML rilascia tutte le risorse associate alla transazione ed Elimina i risultati della transazione al termine dell'elaborazione da parte del server. Un timeout durante una transazione sincrona annulla efficacemente la transazione.

Il metodo di transazione asincrono viene fornito per le applicazioni che devono inviare un volume elevato di transazioni DDE, eseguendo contemporaneamente una notevole quantità di elaborazione, ad esempio l'esecuzione di calcoli. Il metodo asincrono è inoltre utile nelle applicazioni che devono arrestare temporaneamente l'elaborazione delle transazioni DDE, in modo da poter completare altre attività senza interruzioni. Nella maggior parte delle situazioni, un'applicazione deve usare il metodo sincrono.

Le transazioni sincrone sono più semplici da gestire e più veloci rispetto alle transazioni asincrone. Tuttavia, è possibile eseguire una sola transazione sincrona alla volta, mentre molte transazioni asincrone possono essere eseguite contemporaneamente. Con le transazioni sincrone, un server lento può causare che un client rimanga inattivo mentre è in attesa di una risposta. Inoltre, le transazioni sincrone fanno sì che il client entri in un ciclo modale che può ignorare il filtro dei messaggi nel ciclo di messaggi dell'applicazione.

Se il client ha installato una procedura di hook per filtrare i messaggi (ovvero se è stato specificato il \_ tipo di hook msgfilter di WH in una chiamata alla funzione [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) ), una transazione sincrona non comporterà il bypass della routine hook da parte del sistema. Quando si verifica un evento di input mentre il client è in attesa del termine di una transazione sincrona, la routine hook riceve un \_ codice hook DDEMGR di MSGF. Il pericolo principale dell'utilizzo di un ciclo modale di transazione sincrona è che un ciclo modale creato da una finestra di dialogo può interferire con l'operazione. Le transazioni asincrone devono essere sempre utilizzate quando DDEML viene utilizzato da una DLL.

## <a name="transaction-control"></a>Controllo transazione

Un'applicazione può sospendere le transazioni alla relativa funzione di callback DDE, ovvero le transazioni associate a un handle di conversazione specifico o a tutte le transazioni indipendentemente dall'handle di conversazione. Questa funzionalità è utile quando un'applicazione riceve una transazione che richiede una lunga elaborazione. In tal caso, l'applicazione può restituire il \_ codice restituito del blocco CBR per sospendere le transazioni future associate all'handle di conversazione della transazione, in modo che l'applicazione sia disponibile per l'elaborazione di altre conversazioni.

Al termine dell'elaborazione, l'applicazione chiama la funzione [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) per riprendere le transazioni associate alla conversazione sospesa. La chiamata di **DdeEnableCallback** fa sì che DDEML riinvii la transazione che ha causato la sospensione della conversazione da parte dell'applicazione. Pertanto, l'applicazione deve archiviare il risultato della transazione in modo tale che possa ottenere e restituire il risultato senza rielaborare la transazione.

Un'applicazione può sospendere tutte le transazioni associate a un handle di conversazione specifico specificando l'handle e il \_ flag di disabilitazione EC in una chiamata a [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Specificando un handle **null** , un'applicazione può sospendere tutte le transazioni per tutte le conversazioni.

Quando una conversazione è stata sospesa, DDEML Salva le transazioni per la conversazione in una coda di transazioni. Quando l'applicazione riabilita la conversazione, DDEML rimuove le transazioni salvate dalla coda e passa ogni transazione alla funzione di callback appropriata. La capacità della coda delle transazioni è di grandi dimensioni, ma un'applicazione deve riabilitare una conversazione sospesa il prima possibile per evitare la perdita di transazioni.

Un'applicazione può riprendere la normale elaborazione delle transazioni specificando il \_ flag EC ENABLEALL in [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Per una ripresa più controllata dell'elaborazione delle transazioni, l'applicazione può specificare il \_ flag EC ENABLEONE. Questo flag rimuove una transazione dalla coda delle transazioni e la passa alla funzione di callback appropriata; dopo che la transazione è stata elaborata, le conversazioni vengono nuovamente disabilitate.

Se \_ nella chiamata a [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)sono specificati il flag EC ENABLEONE e un handle di conversazione, solo la conversazione viene bloccata dopo l'elaborazione della transazione. Se viene specificato un handle di conversazione **null** , tutte le conversazioni vengono bloccate dopo l'elaborazione di una transazione in qualsiasi conversazione.

## <a name="transaction-classes"></a>Classi di transazione

DDEML dispone di quattro classi di transazioni. Ogni classe è identificata da una costante che inizia con il \_ prefisso XCLASS. Le classi sono definite nel file di intestazione DDEML. Il valore della classe viene combinato con il valore del tipo di transazione e viene passato alla funzione di callback DDE dell'applicazione ricevente.

Una classe di transazione determina il valore restituito che una funzione di callback dovrebbe restituire se elabora la transazione. I valori restituiti e i tipi di transazioni seguenti sono associati a ognuna delle quattro classi di transazione.



| Classe                | Valore restituito                                                     | Transazione                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_bool XCLASS         | **True** o **false**                                            | [**\_ADVSTART XTYP**](xtyp-advstart.md)<br/> [**\_connessione XTYP**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| \_dati XCLASS         | Un handle di dati, il \_ codice restituito del blocco CBR **o null**           | [**\_ADVREQ XTYP**](xtyp-advreq.md)<br/> [**\_richiesta XTYP**](xtyp-request.md)<br/> [**\_WILDCONNECT XTYP**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| \_flag XCLASS        | Flag di transazione: DDE \_ fack, DDE \_ FBUSY o DDE \_ FNOTPROCESSED | [**\_ADVDATA XTYP**](xtyp-advdata.md)<br/> [**esecuzione di XTYP \_**](xtyp-execute.md)<br/> [**\_poke XTYP**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| \_notifica XCLASS | nessuno                                                             | [**\_ADVSTOP XTYP**](xtyp-advstop.md)<br/> [**\_Conferma connessione \_ XTYP**](xtyp-connect-confirm.md)<br/> [**disconnessione XTYP \_**](xtyp-disconnect.md)<br/> [**\_errore XTYP**](xtyp-error.md)<br/> [**\_Registro XTYP**](xtyp-register.md)<br/> [**annullare la registrazione di XTYP \_**](xtyp-unregister.md)<br/> [**XTYP \_ XACT \_ completato**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>Tipi di transazione

Ogni tipo di transazione DDE dispone di un ricevitore e di un'attività associata che determina la generazione di ogni tipo da parte del DDEML.



| Tipo di transazione                                       | Ricevitore                   | Causa                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ADVDATA XTYP**](xtyp-advdata.md)                  | Client                     | Un server ha risposto a una transazione [**XTYP \_ ADVREQ**](xtyp-advreq.md) restituendo un handle di dati.                                                                          |
| [**\_ADVREQ XTYP**](xtyp-advreq.md)                    | Server                     | Server denominato funzione [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) , che indica che il valore di un elemento di dati in un ciclo di notifica è stato modificato.                                  |
| [**\_ADVSTART XTYP**](xtyp-advstart.md)                | Server                     | Un client ha specificato il tipo di transazione [**\_ ADVSTART XTYP**](xtyp-advstart.md) in una chiamata alla funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .               |
| [**\_ADVSTOP XTYP**](xtyp-advstop.md)                  | Server                     | Un client ha specificato il tipo di transazione [**\_ ADVSTOP di XTYP**](xtyp-advstop.md) in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**\_connessione XTYP**](xtyp-connect.md)                  | Server                     | Un client ha chiamato la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e ha specificato un nome di servizio e un nome di argomento supportati dal server.                                            |
| [**\_Conferma connessione \_ XTYP**](xtyp-connect-confirm.md) | Server                     | Il server ha restituito **true** in risposta a una transazione [**XTYP \_ Connect**](xtyp-connect.md) o [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) .                            |
| [**disconnessione XTYP \_**](xtyp-disconnect.md)            | Client/Server              | Partner in una conversazione chiamata funzione [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) , che causa la ricezione della transazione da parte di entrambi i partner.                                    |
| [**\_errore XTYP**](xtyp-error.md)                      | Client/Server              | Si è verificato un errore critico. È possibile che il DDEML non disponga di risorse sufficienti per continuare.                                                                                       |
| [**esecuzione di XTYP \_**](xtyp-execute.md)                  | Server                     | Un client ha specificato il tipo di transazione [**XTYP \_ Execute**](xtyp-execute.md) in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**\_monitoraggio XTYP**](xtyp-monitor.md)                  | Applicazione di monitoraggio DDE | Si è verificato un evento DDE nel sistema. Per ulteriori informazioni sulle applicazioni di monitoraggio DDE, vedere [monitoraggio delle applicazioni](monitoring-applications.md).                       |
| [**\_poke XTYP**](xtyp-poke.md)                        | Server                     | Un client ha specificato il tipo di transazione [**\_ poke XTYP**](xtyp-poke.md) in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                                    |
| [**\_Registro XTYP**](xtyp-register.md)                | Client/Server              | Un'applicazione server utilizza la funzione [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per registrare un nome di servizio.                                                                   |
| [**\_richiesta XTYP**](xtyp-request.md)                  | Server                     | Un client ha specificato il tipo di transazione di [**\_ richiesta XTYP**](xtyp-request.md) in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**annullare la registrazione di XTYP \_**](xtyp-unregister.md)            | Client/Server              | Un'applicazione server utilizza [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per annullare la registrazione di un nome di servizio.                                                                              |
| [**\_WILDCONNECT XTYP**](xtyp-wildconnect.md)          | Server                     | Un client ha chiamato la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) o [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) , specificando **null** per il nome del servizio, il nome dell'argomento o entrambi. |
| [**XTYP \_ XACT \_ completato**](xtyp-xact-complete.md)     | Client                     | Una transazione asincrona, inviata quando il client ha specificato il \_ flag di timeout asincrono in una chiamata a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction), è stata conclusa.         |



 

 

