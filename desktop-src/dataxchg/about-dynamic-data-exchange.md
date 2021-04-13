---
title: Informazioni su Dynamic Data Exchange
description: In questo argomento viene illustrato il trasferimento dei dati tra le applicazioni.
ms.assetid: 0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb
keywords:
- Dynamic Data Exchange (DDE), informazioni
- DDE (Dynamic Data Exchange), informazioni
- scambio di dati, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), collegamento ai dati in tempo reale
- DDE (Dynamic Data Exchange), collegamento ai dati in tempo reale
- Dynamic Data Exchange (DDE), creazione di documenti composti
- DDE (Dynamic Data Exchange), creazione di documenti composti
- Dynamic Data Exchange (DDE), query di dati
- DDE (Dynamic Data Exchange), query di dati
- Dynamic Data Exchange (DDE), esempi
- DDE (Dynamic Data Exchange), esempi
- Dynamic Data Exchange (DDE), rappresentazione
- DDE (Dynamic Data Exchange), rappresentazione
- Dynamic Data Exchange (DDE), messaggi
- DDE (Dynamic Data Exchange), messaggi
- Dynamic Data Exchange (DDE), atomi
- DDE (Dynamic Data Exchange), atomi
- Dynamic Data Exchange (DDE), oggetti Shared Memory
- DDE (Dynamic Data Exchange), oggetti Shared Memory
- Dynamic Data Exchange (DDE), funzioni di compressione di parametri
- DDE (Dynamic Data Exchange), funzioni di compressione di parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d38574e9182255e8f6761520aea60575d8affbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399524"
---
# <a name="about-dynamic-data-exchange"></a>Informazioni su Dynamic Data Exchange

In Windows sono disponibili diversi metodi per il trasferimento dei dati tra le applicazioni. Un metodo consiste nell'utilizzare il protocollo Dynamic Data Exchange (DDE). Il protocollo DDE è un set di messaggi e linee guida. Invia messaggi tra applicazioni che condividono dati e utilizza la memoria condivisa per scambiare dati tra le applicazioni. Le applicazioni possono utilizzare il protocollo DDE per i trasferimenti di dati monouso e per gli scambi continui in cui le applicazioni inviano gli aggiornamenti l'uno all'altro man volta che i nuovi dati diventano disponibili.

Windows supporta inoltre la libreria di gestione Dynamic Data Exchange (DDEML). DDEML è una libreria di collegamento dinamico (DLL) che può essere utilizzata dalle applicazioni per condividere i dati. DDEML fornisce funzioni e messaggi che semplificano l'attività di aggiunta della funzionalità DDE a un'applicazione. Anziché inviare, inviare ed elaborare direttamente i messaggi DDE, un'applicazione utilizza le funzioni DDEML per gestire le conversazioni DDE. Una conversazione DDE è l'interazione tra applicazioni client e server.

DDEML fornisce inoltre una funzionalità per la gestione delle stringhe e dei dati condivisi dalle applicazioni DDE. Anziché utilizzare gli atomi e i puntatori agli oggetti Shared Memory, le applicazioni DDE creano e scambiano handle di stringa, che identificano le stringhe e gli handle di dati, che identificano gli oggetti di memoria. Il DDEML consente anche a un'applicazione server di registrare i nomi di servizio supportati. I nomi vengono trasmessi ad altre applicazioni nel sistema, che possono usare i nomi per connettersi al server. Inoltre, il DDEML garantisce la compatibilità tra applicazioni DDE forzando l'implementazione del protocollo DDE in modo coerente.

Le applicazioni esistenti che usano il protocollo DDE basato su messaggi sono completamente compatibili con quelle che usano DDEML. Ovvero, un'applicazione che utilizza un DDE basato su messaggi può stabilire conversazioni ed eseguire transazioni con applicazioni che utilizzano DDEML. A causa dei numerosi vantaggi di DDEML, le nuove applicazioni devono utilizzarlo invece dei messaggi DDE. Per usare gli elementi API del DDEML, è necessario includere il file di intestazione DDEML nei file di origine, collegare con la libreria DDEML e verificare che la libreria a collegamento dinamico DDEML si trovi nel percorso di ricerca del sistema.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Protocollo Dynamic Data Exchange](#dynamic-data-exchange-protocol)
-   [Usi per Windows Dynamic Data Exchange](#uses-for-windows-dynamic-data-exchange)
-   [Dynamic Data Exchange dal punto di vista dell'utente](#dynamic-data-exchange-from-the-users-point-of-view)
-   [Concetti di Dynamic Data Exchange](#dynamic-data-exchange-concepts)
    -   [Client, server e conversazione](#client-server-and-conversation)
    -   [Nomi di applicazione, argomento e elemento](#application-topic-and-item-names)
    -   [Argomento di sistema](#the-system-topic)
    -   [Collegamenti dati permanenti](#permanent-data-links)
    -   [Atomi e oggetti Shared Memory](#atoms-and-shared-memory-objects)
-   [Panoramica dei messaggi di Dynamic Data Exchange](#dynamic-data-exchange-messages-overview)
-   [Flusso di messaggi Dynamic Data Exchange](#dynamic-data-exchange-message-flow)
-   [Funzioni di compressione di parametri](#parameter-packing-functions)
-   [Dynamic Data Exchange e rappresentazione](#dynamic-data-exchange-and-impersonation)

## <a name="dynamic-data-exchange-protocol"></a>Protocollo Dynamic Data Exchange

Poiché Windows dispone di un'architettura basata su messaggi, il passaggio dei messaggi è il metodo più appropriato per il trasferimento automatico delle informazioni tra le applicazioni. Tuttavia, i messaggi contengono solo due parametri (*wParam* e *lParam*) per il passaggio di dati. Di conseguenza, questi parametri devono riferirsi indirettamente ad altre parti di dati quando più di poche parole di informazioni passano tra le applicazioni. Il protocollo DDE definisce esattamente il modo in cui le applicazioni devono usare i parametri *wParam* e *lParam* per passare dati di grandi dimensioni per mezzo di atomi globali e handle di memoria condivisa. Il protocollo DDE prevede regole specifiche per l'allocazione e l'eliminazione di atomi globali e oggetti di memoria condivisa.

Un Atom globale è un riferimento a una stringa di caratteri. Nel protocollo DDE gli atomi identificano le applicazioni che scambiano dati, la natura dei dati scambiati e gli stessi elementi di dati. Per altre informazioni sugli atomi, vedere [informazioni sugli atomi](about-atom-tables.md).

## <a name="uses-for-windows-dynamic-data-exchange"></a>Usi per Windows Dynamic Data Exchange

Il DDE è più adatto per gli scambi di dati che non richiedono l'interazione dell'utente continua. In genere, un'applicazione fornisce un metodo per consentire all'utente di stabilire il collegamento tra le applicazioni che scambiano dati. Una volta stabilito il collegamento, le applicazioni scambiano i dati senza ulteriore intervento dell'utente.

È possibile utilizzare DDE per implementare un'ampia gamma di funzionalità dell'applicazione, ad esempio:

-   Collegamento a dati in tempo reale, ad esempio aggiornamenti del mercato azionario, strumenti scientifici o controllo dei processi.
-   Creazione di documenti composti, ad esempio un documento di elaborazione di testo che include un grafico prodotto da un'applicazione grafica. Utilizzando DDE, il grafico verrà modificato quando i dati di origine vengono modificati, mentre il resto del documento rimane lo stesso.
-   Esecuzione di query sui dati tra applicazioni, ad esempio un foglio di calcolo che esegue query su un database per gli account precedenti.

## <a name="dynamic-data-exchange-from-the-users-point-of-view"></a>Dynamic Data Exchange dal punto di vista dell'utente

Nell'esempio seguente viene illustrato il modo in cui due applicazioni DDE possono collaborare, come illustrato dal punto di vista dell'utente.

Un utente del foglio di calcolo desidera utilizzare Microsoft Excel per tenere traccia del prezzo di una determinata azione in borsa di New York. L'utente dispone di un'applicazione denominata virgolette che a sua volta ha accesso ai dati NYSE. La conversazione DDE tra Excel e le virgolette viene eseguita come indicato di seguito:

-   L'utente avvia la conversazione fornendo il nome dell'applicazione (virgoletta) che fornirà i dati e il particolare argomento di interesse (NYSE). La conversazione DDE risultante viene utilizzata per richiedere virgolette in base a scorte specifiche.
-   Excel trasmette i nomi dell'applicazione e dell'argomento a tutte le applicazioni DDE attualmente in esecuzione nel sistema. Il preventivo risponde, che stabilisce una conversazione con Excel sull'argomento NYSE.
-   L'utente può quindi creare una formula del foglio di calcolo in una cella che richiede che il foglio di calcolo venga aggiornato automaticamente ogni volta che vengono apportate modifiche alle virgolette. Ad esempio, l'utente potrebbe richiedere un aggiornamento automatico ogni volta che viene apportata una modifica al prezzo di vendita di ZAXX Stock specificando la formula di Excel seguente: =' quote ' \| ' NYSE '! ZAXX
-   L'utente può terminare l'aggiornamento automatico delle quotazioni azionarie di ZAXX in qualsiasi momento. Altri collegamenti dati che sono stati stabiliti separatamente, ad esempio per le quote per altre scorte, rimarranno attivi nella stessa conversazione NYSE.
-   L'utente può anche terminare l'intera conversazione tra Excel e le virgolette nell'argomento NYSE, in modo che non sia possibile stabilire collegamenti dati specifici su tale argomento senza avviare una nuova conversazione.

## <a name="dynamic-data-exchange-concepts"></a>Concetti di Dynamic Data Exchange

Le sezioni seguenti illustrano i concetti e la terminologia principali per comprendere lo scambio di dati dinamici.

-   [Client, server e conversazione](#client-server-and-conversation)
-   [Nomi di applicazione, argomento e elemento](#application-topic-and-item-names)
-   [Argomento di sistema](#the-system-topic)
-   [Collegamenti dati permanenti](#permanent-data-links)
-   [Atomi e oggetti Shared Memory](#atoms-and-shared-memory-objects)

### <a name="client-server-and-conversation"></a>Client, server e conversazione

Due applicazioni che partecipano a DDE sono definite in una conversazione DDE. L'applicazione che avvia la conversazione è l'applicazione client DDE. l'applicazione che risponde al client è l'applicazione server DDE. Un'applicazione può coinvolgere più conversazioni contemporaneamente, agendo come client in alcuni e come server in altri.

Una conversazione DDE si verifica tra due finestre, una per ogni applicazione partecipante. Una finestra può essere la finestra principale dell'applicazione. una finestra associata a un documento specifico, come in un'applicazione con interfaccia a documenti multipli (MDI); o una finestra nascosta (invisibile) il cui unico scopo è elaborare i messaggi DDE.

Poiché una conversazione DDE viene identificata dalla coppia di handle per le finestre coinvolte nella conversazione, nessuna finestra deve essere inserita in più di una conversazione con un'altra finestra. L'applicazione client o l'applicazione server deve fornire una finestra diversa per ognuna delle conversazioni con un server o un'applicazione client specifica.

Un'applicazione può garantire che una coppia di Windows client e server non venga mai interessata in più di una conversazione creando una finestra nascosta per ogni conversazione. L'unico scopo di questa finestra è elaborare i messaggi DDE.

### <a name="application-topic-and-item-names"></a>Nomi di applicazione, argomento e elemento

Il protocollo DDE identifica le unità di dati passate tra il client e il server con una gerarchia a tre livelli dei nomi di applicazione, argomento e elemento.

Ogni conversazione DDE viene definita in modo univoco dal nome dell'applicazione e dall'argomento. All'inizio di una conversazione DDE, il client e il server determinano il nome dell'applicazione e l'argomento. Il nome dell'applicazione è in genere il nome dell'applicazione server. Ad esempio, quando Excel funge da server in una conversazione, il nome dell'applicazione è Excel.

L'argomento DDE è una classificazione generale dei dati in cui è possibile che vengano discussi più elementi di dati (scambiati) durante la conversazione. Per le applicazioni che operano su documenti basati su file, l'argomento è in genere un nome di file. Per altre applicazioni, l'argomento è un nome specifico dell'applicazione.

Poiché la finestra client e server gestisce insieme l'identificazione di una conversazione DDE, il nome dell'applicazione e l'argomento che definiscono una conversazione non possono essere modificati nel corso della conversazione.

Un elemento di dati DDE è informazioni correlate all'argomento di conversazione scambiato tra le applicazioni. I valori per l'elemento di dati possono essere passati dal server al client o dal client al server. I dati possono essere passati con uno dei formati degli Appunti standard o con un formato degli Appunti registrato. Un formato speciale registrato denominato link identifica un elemento in una conversazione DDE. Per ulteriori informazioni sui formati degli Appunti, vedere [Appunti](clipboard.md).

### <a name="the-system-topic"></a>Argomento di sistema

Le applicazioni devono supportare l'argomento di sistema in qualsiasi momento. In questo argomento viene fornito un contesto per informazioni che possono essere di interesse generale per un'altra applicazione.

È necessario eseguire il rendering dei valori degli elementi di dati nel formato degli Appunti di [**\_ testo CF**](standard-clipboard-formats.md) . I singoli elementi dei valori degli elementi per un argomento di sistema devono essere delimitati da caratteri di tabulazione. La tabella seguente suggerisce alcuni elementi per l'argomento di sistema.



| Elemento          | Descrizione                                                                                                                                                                                                                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Formati       | Elenco delimitato da tabulazioni di formati degli Appunti di cui l'applicazione può eseguire il rendering. In genere, i formati **CF \_** sono elencati con la parte "**CF \_**" dei nomi rimossi (ad esempio, il **\_ testo CF** viene elencato come "**testo**").                                                                                        |
| Help          | Testo che spiega brevemente come utilizzare il server DDE.                                                                                                                                                                                                                                                   |
| ReturnMessage | Dettagli di supporto per il messaggio [**\_ \_ ACK DDE WM**](wm-dde-ack.md) usato più di recente. Questo elemento è utile quando sono necessari più di otto bit di dati restituiti specifici dell'applicazione.                                                                                                                |
| Stato        | Indica lo stato corrente dell'applicazione. Quando un server riceve un messaggio di [**\_ \_ richiesta DDE di WM**](wm-dde-request.md) per questo elemento dell'argomento di sistema, deve rispondere inserendo un messaggio di [**\_ \_ dati DDE WM**](wm-dde-data.md) con una stringa che contiene occupato o pronto, a seconda dei casi. |
| SysItems      | Elenco di elementi dell'argomento di sistema supportati dall'applicazione.                                                                                                                                                                                                                                                    |
| TopicItemList | Simile all'elemento SysItems, ad eccezione del fatto che TopicItemList deve essere supportato per ogni argomento diverso dall'argomento di sistema. In questo modo è possibile esplorare gli elementi supportati in qualsiasi argomento. Se non è possibile enumerare gli elementi, l'elemento deve contenere solo "TopicItemList".                                  |
| Argomenti        | Elenco di argomenti supportati dall'applicazione nell'ora corrente; Questo elenco può variare a seconda del momento.                                                                                                                                                                                                  |



 

### <a name="permanent-data-links"></a>Collegamenti dati permanenti

Una volta iniziata una conversazione DDE, il client può stabilire uno o più collegamenti di dati permanenti con il server. Un collegamento dati è un meccanismo di comunicazione mediante il quale il server invia una notifica al client ogni volta che viene modificato il valore di un elemento di dati specificato. Il collegamento dati è permanente nel senso che questo processo di notifica continua fino a quando non viene terminato il collegamento dati o la conversazione DDE.

Sono disponibili due tipi di collegamenti permanenti ai dati DDE: caldo e frequente. In un collegamento dati caldo, il server notifica al client che il valore dell'elemento di dati è stato modificato, ma il server non invia il valore dei dati al client fino a quando non viene richiesto dal client. In un collegamento dati attivo, il server invia immediatamente il valore dei dati modificati al client.

Le applicazioni che supportano collegamenti dati caldi o a caldo forniscono in genere un comando **copia** o **Incolla collegamento** nel menu **modifica** per consentire all'utente di stabilire collegamenti tra le applicazioni.

### <a name="atoms-and-shared-memory-objects"></a>Atomi e oggetti Shared Memory

Alcuni argomenti dei messaggi DDE sono atomi globali o oggetti Shared Memory. Le applicazioni che usano questi argomenti devono seguire regole esplicite su quando allocarle ed eliminarle. In tutti i casi, il mittente del messaggio deve eliminare tutti gli oggetti Atom o Shared Memory che non vengono ricevuti dal ricevitore previsto a causa di una condizione di errore, ad esempio un errore della funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .

Il DDE utilizza gli oggetti Shared Memory per tre scopi:

-   Per portare un valore dell'elemento di dati da scambiare. Si tratta di un elemento a cui fa  riferimento il parametro hData [**nei \_ \_ dati DDE di WM**](wm-dde-data.md) e nei messaggi [**\_ \_ poke DDE di WM**](wm-dde-poke.md) .
-   Per includere le opzioni in un messaggio. Si tratta di un elemento a cui fa riferimento il parametro *hOptions* in un messaggio di [**\_ \_ avviso DDE di WM**](wm-dde-advise.md) .
-   Per includere una stringa di esecuzione del comando. Si tratta di un elemento a cui fa riferimento il parametro *hCommands* nel messaggio [**\_ \_ Execute DDE di WM**](wm-dde-execute.md) e il corrispondente messaggio [**\_ \_ ACK DDE**](wm-dde-ack.md) .

Un'applicazione che riceve un oggetto memoria condivisa DDE deve considerarla di sola lettura. L'applicazione non deve usare l'oggetto come area di lettura/scrittura reciproca per lo scambio di dati libero.

Come avviene con un Atom DDE, un'applicazione deve liberare un oggetto Shared Memory per gestire la memoria in modo efficace. L'applicazione deve inoltre bloccare e sbloccare gli oggetti di memoria.

## <a name="dynamic-data-exchange-messages-overview"></a>Panoramica dei messaggi di Dynamic Data Exchange

Poiché DDE è un protocollo basato su messaggi, non utilizza funzioni o librerie. Tutte le transazioni DDE vengono eseguite passando determinati messaggi DDE definiti tra le finestre client e server.

Sono presenti nove messaggi DDE. le costanti simboliche per questi messaggi sono definite nel file di intestazione DDE. In questo file di intestazione sono definite anche alcune strutture per i vari messaggi DDE.

Nella tabella seguente vengono riepilogati i messaggi DDE.



| Message                                        | Descrizione                                                                                                                                      |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACK DDE \_ WM**](wm-dde-ack.md)             | Conferma la ricezione o la mancata ricezione di un messaggio.                                                                                               |
| [**\_avviso DDE di WM \_**](wm-dde-advise.md)       | Richiede all'applicazione server di fornire un aggiornamento o una notifica per un elemento di dati ogni volta che viene modificato. Viene stabilito un collegamento dati permanente. |
| [**\_dati DDE di WM \_**](wm-dde-data.md)           | Invia un valore dell'elemento di dati all'applicazione client.                                                                                               |
| [**esecuzione di WM \_ DDE \_**](wm-dde-execute.md)     | Invia una stringa all'applicazione server, che dovrebbe elaborare la stringa come una serie di comandi.                                       |
| [**\_avvio DDE \_ WM**](wm-dde-initiate.md)   | Avvia una conversazione tra le applicazioni client e server.                                                                             |
| [**\_poke DDE \_ WM**](wm-dde-poke.md)           | Invia un valore dell'elemento di dati all'applicazione server.                                                                                               |
| [**\_richiesta DDE \_ WM**](wm-dde-request.md)     | Richiede all'applicazione server di fornire il valore di un elemento di dati.                                                                             |
| [**\_ \_ terminazione DDE WM**](wm-dde-terminate.md) | Termina una conversazione.                                                                                                                       |
| [**\_Unadvise DDE WM \_**](wm-dde-unadvise.md)   | Termina un collegamento dati permanente.                                                                                                                |



 

Un'applicazione chiama [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per emettere il messaggio di [**\_ \_ avvio DDE di WM**](wm-dde-initiate.md) o un messaggio [**\_ \_ ACK DDE WM**](wm-dde-ack.md) inviato in risposta **all' \_ \_ avvio di WM DDE**. Tutti gli altri messaggi vengono inviati da [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea). Il primo parametro di queste chiamate è un handle per la finestra di ricezione. il secondo parametro contiene il messaggio da inviare. il terzo parametro identifica la finestra di invio; il quarto parametro contiene quindi gli argomenti specifici del messaggio.

## <a name="dynamic-data-exchange-message-flow"></a>Flusso di messaggi Dynamic Data Exchange

Una tipica conversazione DDE è costituita dagli eventi seguenti:

1.  L'applicazione client avvia la conversazione e l'applicazione server risponde.
2.  Le applicazioni scambiano i dati in base a uno o tutti i metodi seguenti:
    -   -   L'applicazione server invia i dati al client in corrispondenza della richiesta del client.
        -   L'applicazione client invia dati non richiesti all'applicazione server.
        -   L'applicazione client richiede all'applicazione server di notificare al client ogni volta che un elemento di dati viene modificato (collegamento dati caldo).
        -   L'applicazione client richiede che l'applicazione server invii i dati ogni volta che i dati cambiano (collegamento a dati sensibili).
        -   L'applicazione server esegue un comando in corrispondenza della richiesta del client.

3.  Il client o l'applicazione server termina la conversazione.

Una finestra dell'applicazione che elabora le richieste da un client o da un server deve elaborarle rigorosamente nell'ordine in cui vengono ricevute.

Un client può stabilire conversazioni con più di un server. un server può avere conversazioni con più di un client. Quando si gestiscono messaggi da più origini, un client o un server deve elaborare i messaggi di una conversazione in modo sincrono, ma non è necessario elaborare tutti i messaggi in modo sincrono. In altre parole, è possibile passare da una conversazione all'altra in base alle esigenze.

Se un'applicazione non è in grado di elaborare una richiesta in ingresso perché è in attesa di una risposta DDE, deve impedire il deadlock inviando un messaggio di [**\_ \_ ACK DDE WM**](wm-dde-ack.md) con il membro **fBusy** della struttura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) impostata su 1. Un'applicazione può anche inviare un messaggio **di \_ \_ ACK DDE WM** occupato se, per qualsiasi motivo, non è in grado di elaborare una richiesta in ingresso entro un periodo di tempo ragionevole.

Un'applicazione deve essere in grado di gestire l'errore di un client o di un server per rispondere a un messaggio entro un determinato periodo di tempo. Poiché l'intervallo di timeout può variare a seconda della natura dell'applicazione e della configurazione del sistema dell'utente (ad esempio se è connessa a una rete), l'applicazione deve fornire un modo per specificare l'intervallo per l'utente.

## <a name="parameter-packing-functions"></a>Funzioni di compressione di parametri

Il parametro *lParam* di molti messaggi DDE contiene due tipi di dati. Il valore *lParam* del messaggio di [**\_ \_ dati DDE WM**](wm-dde-data.md) , ad esempio, contiene un handle di dati e un Atom. Le applicazioni devono utilizzare la funzione [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) per comprimere l'handle e il formato Atom in un parametro *lParam* e la funzione [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) per rimuovere i valori. Le applicazioni DDE devono usare **PackDDElParam** e **UnpackDDElParam** per tutti i messaggi inviati durante una conversazione DDE.

Le applicazioni possono inoltre utilizzare le funzioni [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) e [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) . **ReuseDDElParam** consente a un'applicazione DDE di riutilizzare un parametro *lParam* compresso, contribuendo a ridurre il numero di riallocazioni di memoria che l'applicazione deve eseguire durante una conversazione. Un'applicazione può utilizzare **FreeDDElParam** per liberare la memoria associata a un handle di dati ricevuto durante una conversazione DDE.

## <a name="dynamic-data-exchange-and-impersonation"></a>Dynamic Data Exchange e rappresentazione

Per consentire a un server di rappresentare un client, il client chiama la funzione [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) . La struttura del [**\_ \_ livello di rappresentazione di sicurezza**](/windows/win32/api/winnt/ne-winnt-security_impersonation_level) viene utilizzata per controllare il livello di rappresentazione che il server può eseguire.

Un server DDE può rappresentare un client DDE chiamando la funzione [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) . Un server DDEML deve usare la funzione [**DdeImpersonateClient**](/windows/desktop/api/Ddeml/nf-ddeml-ddeimpersonateclient) .

 

 