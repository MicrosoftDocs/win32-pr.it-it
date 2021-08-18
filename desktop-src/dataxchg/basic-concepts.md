---
title: Concetti di base
description: In questo argomento vengono illustrati i concetti chiave relativi a Dynamic Data Exchange.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Windows Interfaccia utente,Dynamic Data Exchange (DDE)
- Windows Interfaccia utente,Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange (DDE), interazione del server client
- DDE (Dynamic Data Exchange),interazione del server client
- scambio di dati, Dynamic Data Exchange (DDE)
- scambio di dati, Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange (DDE), applicazioni client
- DDE (Dynamic Data Exchange),applicazioni client
- Dynamic Data Exchange (DDE), applicazioni server
- DDE (Dynamic Data Exchange),applicazioni server
- Dynamic Data Exchange (DDE), funzioni di callback
- DDE (Dynamic Data Exchange),funzioni di callback
- Dynamic Data Exchange (DDE), transazioni
- DDE (Dynamic Data Exchange),transazioni
- Dynamic Data Exchange (DDE), nomi dei servizi
- DDE (Dynamic Data Exchange),nomi dei servizi
- Dynamic Data Exchange (DDE), nomi degli elementi
- DDE (Dynamic Data Exchange),nomi degli elementi
- Dynamic Data Exchange (DDE), nomi degli argomenti
- DDE (Dynamic Data Exchange),nomi degli argomenti
- Dynamic Data Exchange (DDE),Argomento System
- DDE (Dynamic Data Exchange),Argomento System
- Dynamic Data Exchange Management Library (DDEML), inizializzazione
- DDEML (Dynamic Data Exchange Management Library),inizializzazione
- Dynamic Data Exchange Management Library (DDEML), funzioni di callback
- DDEML (Dynamic Data Exchange Management Library), funzioni di callback
- Dynamic Data Exchange Management Library (DDEML), gestione delle stringhe
- DDEML (Dynamic Data Exchange Management Library),gestione delle stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae271c359afd571cf6c51fb3387a15f1496416e5eb54b055ef518fd213f30fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128623"
---
# <a name="basic-concepts-dde"></a>Concetti di base (DDE)

Questi concetti sono fondamentali per comprendere Dynamic Data Exchange (DDE) e Dynamic Data Exchange Management Library (DDEML).

-   [Interazione tra client e server](#client-and-server-interaction)
-   [Transazioni e funzione di callback DDE](#transactions-and-the-dde-callback-function)
-   [Nomi di servizi, nomi di argomenti e nomi di elementi](#service-names-topic-names-and-item-names)
-   [Argomento di sistema](#system-topic)
-   [Inizializzazione](#initialization)
-   [Funzione di callback](#callback-function)
-   [Gestione delle stringhe](#string-management)
-   [DDEML e thread](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>Interazione tra client e server

DDE si verifica sempre tra un'applicazione client e un'applicazione server. *L'applicazione client DDE* avvia lo scambio stabilendo una conversazione con il server per inviare le transazioni al server. Una transazione è una richiesta di dati o servizi. *L'applicazione server DDE* risponde alle transazioni fornendo dati o servizi al client. Ad esempio, un'applicazione grafica potrebbe contenere un grafico a barre che rappresenta i profitti trimestrali di un'azienda, ma i dati per il grafico a barre potrebbero essere contenuti in un'applicazione foglio di calcolo. Per ottenere i profitti più recenti, l'applicazione grafica (il client) può stabilire una conversazione con l'applicazione foglio di calcolo (il server). L'applicazione grafica può quindi inviare una transazione all'applicazione foglio di calcolo, richiedendo le cifre di profitto più recenti.

Un server può avere più client contemporaneamente e un client può richiedere dati da più server. Un'applicazione può anche essere sia un client che un server. Il client o il server può terminare la conversazione in qualsiasi momento.

## <a name="transactions-and-the-dde-callback-function"></a>Transazioni e funzione di callback DDE

DDEML notifica a un'applicazione l'attività DDE che influisce sull'applicazione inviando transazioni alla funzione di callback DDE dell'applicazione. Una *transazione DDE* è simile a un messaggio. Si tratta di una costante denominata accompagnata da altri parametri che contengono informazioni aggiuntive sulla transazione.

DDEML passa una transazione a una funzione di callback DDE definita dall'applicazione che esegue un'azione appropriata al tipo di transazione. Ad esempio, quando un'applicazione client tenta di stabilire una conversazione con un'applicazione server, il client chiama [**la funzione DdeConnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) Questa funzione fa in modo che DDEML invii una [**transazione XTYP \_ CONNECT**](xtyp-connect.md) alla funzione di callback DDE del server. La funzione di callback può consentire la conversazione restituisce **TRUE** a DDEML oppure può negare la conversazione restituisce **FALSE.** Per una descrizione dettagliata delle transazioni, vedere [Gestione delle transazioni.](transaction-management.md)

## <a name="service-names-topic-names-and-item-names"></a>Nomi di servizi, nomi di argomenti e nomi di elementi

Un server DDE usa un nome di servizio gerarchia a tre livelli (denominato "nome applicazione" nella documentazione DDE precedente), il nome dell'argomento e il nome dell'elemento per identificare in modo univoco un'unità di dati che il server può scambiare durante una conversazione.

Un *nome di servizio* è una stringa a cui risponde un'applicazione server quando un client tenta di stabilire una conversazione con il server. Un client deve specificare il nome del servizio per stabilire una conversazione con il server. Anche se un server può rispondere a molti nomi di servizio, la maggior parte dei server risponde a un solo nome.

Un *nome di argomento* è una stringa che identifica un contesto dati logico. Per i server che operano su documenti basati su file, i nomi degli argomenti sono in genere nomi file. per gli altri server, sono altre stringhe specifiche dell'applicazione. Un client deve specificare un nome di argomento insieme al nome del servizio di un server quando tenta di stabilire una conversazione con un server.

Un *nome di elemento* è una stringa che identifica un'unità di dati che un server può passare a un client durante una transazione. Ad esempio, un nome di elemento potrebbe identificare un numero intero, una stringa, diversi paragrafi di testo o una bitmap.

I nomi di servizio, argomento ed elemento consentono al client di stabilire una conversazione con un server e di ricevere dati dal server.

## <a name="system-topic"></a>Argomento di sistema

L'argomento System fornisce un contesto per informazioni di interesse generale per qualsiasi client DDE. È consigliabile che le applicazioni server supportino l'argomento Sistema in qualsiasi momento. L'argomento System è definito in DDEML. File di intestazione H come ARGOMENTO SZDDESYS. \_

Per determinare quali server sono presenti e i tipi di informazioni che possono fornire, un'applicazione client può richiedere una conversazione sull'argomento System all'avvio, impostando il nome del dispositivo su **NULL.** Queste conversazioni con caratteri jolly sono costose in termini di prestazioni del sistema, pertanto devono essere mantenute al minimo. Per altre informazioni sull'avvio di conversazioni DDE, vedere [Gestione delle conversazioni.](conversation-management.md)

Un server deve supportare i seguenti nomi di elemento all'interno dell'argomento System e qualsiasi altro nome di elemento utile per un client.



| Elemento                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SZDDE \_ ITEM \_ ITEMLIST    | Elenco degli elementi supportati in un argomento non di sistema. Questo elenco può variare da un momento all'altro e da un argomento all'altro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| FORMATI DEGLI ELEMENTI SZDDESYS \_ \_  | Elenco delimitato da tabulazioni di stringhe che rappresentano tutti i formati degli Appunti potenzialmente supportati dall'applicazione di servizio. Le stringhe che rappresentano formati di Appunti predefiniti sono equivalenti ai valori CF \_ con il prefisso \_ "CF" rimosso. Ad esempio, il formato CF \_ TEXT è rappresentato dalla stringa "TEXT". Queste stringhe devono essere maiuscole per identificarle ulteriormente come formati predefiniti. L'elenco dei formati deve essere visualizzato nell'ordine del contenuto più completo al meno completo. Per altre informazioni sui formati degli Appunti e sul rendering dei dati, vedere [Appunti.](clipboard.md)<br/> |
| GUIDA DELL'ELEMENTO SZDDESYS \_ \_     | Informazioni leggibili dall'utente di interesse generale. Questo elemento deve contenere almeno informazioni su come usare le funzionalità DDE dell'applicazione server. Queste informazioni possono includere, ma non solo, come specificare gli elementi all'interno di argomenti, quali stringhe di esecuzione possono essere eseguite dal server, quali transazioni di poke sono consentite e come trovare informazioni su altri elementi dell'argomento system.                                                                                                                                                                                                                           |
| ELEMENTO SZDDESYS \_ \_ RTNMSG   | Dettagli di supporto per il messaggio [**WM \_ DDE \_ ACK**](wm-dde-ack.md) usato più di recente. Questo elemento è utile quando sono necessari più di 8 bit di dati restituiti specifici dell'applicazione.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| STATO DELL'ELEMENTO SZDDESYS \_ \_   | Indicazione dello stato corrente del server. In genere, questo elemento supporta solo il formato CF \_ TEXT e contiene la stringa Ready o Busy.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SZDDESYS \_ ITEM \_ SYSITEMS | Elenco degli elementi supportati nell'argomento System da questo server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ARGOMENTI RELATIVI AGLI ELEMENTI SZDDESYS \_ \_   | Elenco degli argomenti supportati dal server all'ora corrente. Questo elenco può variare da un momento all'altro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Questi nomi di elemento sono valori definiti in DDEML. File di intestazione H. Per ottenere handle di stringa per queste stringhe, un'applicazione deve usare le funzioni di gestione delle stringhe DDEML, esattamente come per qualsiasi altra stringa in un'applicazione DDEML. Per altre informazioni sulla gestione delle stringhe, vedere [Gestione delle stringhe.](#string-management)

## <a name="initialization"></a>Inizializzazione

Prima di chiamare qualsiasi altra funzione DDEML, un'applicazione deve chiamare la [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) **DdeInitialize** ottiene un identificatore di istanza per l'applicazione, registra la funzione di callback DDE dell'applicazione con DDE e specifica i flag di filtro delle transazioni per la funzione di callback.

Ogni istanza di un'applicazione o di una DLL deve passare il relativo identificatore di istanza come *parametro idInst* a qualsiasi altra funzione DDEML che lo richiede. Lo scopo di più istanze DDEML è supportare le DLL che devono usare DDEML contemporaneamente a un'applicazione. Un'applicazione non deve usare più di un'istanza di DDEML.

*I filtri delle* transazioni ottimizzano le prestazioni del sistema impedendo a DDEML di passare transazioni indesiderate alla funzione di callback DDE dell'applicazione. Un'applicazione imposta i filtri delle transazioni nel parametro *ufCmd* [**di DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Un'applicazione deve specificare un flag di filtro delle transazioni per ogni tipo di transazione che non elabora nella funzione di callback. Un'applicazione può modificare i filtri delle transazioni con una chiamata successiva a **DdeInitialize.** Per altre informazioni sulle transazioni, vedere [Gestione delle transazioni.](transaction-management.md)

Nell'esempio seguente viene illustrato come inizializzare un'applicazione per l'uso di DDEML.


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



Un'applicazione deve [**chiamare la funzione DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) quando non userà più DDEML. Questa funzione termina tutte le conversazioni attualmente aperte per l'applicazione e libera le risorse DDEML allocate dal sistema per l'applicazione.

## <a name="callback-function"></a>Funzione di callback

Un'applicazione che usa DDEML deve fornire una funzione di callback che elabora gli eventi DDE che interessano l'applicazione. DDEML invia una notifica a un'applicazione di tali eventi inviando transazioni alla funzione di callback DDE dell'applicazione. Le transazioni ricevute da una funzione di callback dipendono dal filtro di callback che contrassegna l'applicazione specificata in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) e dal fatto che l'applicazione sia un client, un server o entrambi. Per altre informazioni, vedere [**DdeCallback.**](/windows/win32/api/ddeml/nc-ddeml-pfncallback)

Nell'esempio seguente viene illustrata la struttura generale di una funzione di callback per un'applicazione client tipica.


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



Il *parametro uType* specifica il tipo di transazione inviato alla funzione di callback da DDEML. I valori dei parametri rimanenti dipendono dal tipo di transazione. I tipi di transazione e gli eventi che li generano sono descritti negli argomenti seguenti. Per informazioni dettagliate su ogni tipo di transazione, vedere [Gestione delle transazioni.](transaction-management.md)

## <a name="string-management"></a>Gestione delle stringhe

Per eseguire un'attività DDE, molte funzioni DDEML richiedono l'accesso alle stringhe. Ad esempio, un client deve specificare un nome di servizio e un nome di argomento quando chiama la [**funzione DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) per richiedere una conversazione con un server. Un'applicazione specifica una stringa passando un handle di stringa (HSZ) anziché un puntatore in una funzione DDEML. Un *handle di* stringa è un valore **DWORD,** assegnato dal sistema, che identifica una stringa.

Un'applicazione può ottenere un handle di stringa per una determinata stringa chiamando la [**funzione DdeCreateStringHandle.**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) Questa funzione registra la stringa con il sistema e restituisce un handle di stringa all'applicazione. L'applicazione può passare l'handle alle funzioni DDEML che devono accedere alla stringa. Nell'esempio seguente si ottengono handle di stringa per la stringa dell'argomento System e la stringa del nome del servizio.


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



Il *parametro idInst* nell'esempio precedente specifica l'identificatore di istanza ottenuto dalla [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

La funzione di callback DDE di un'applicazione riceve uno o più handle di stringa durante la maggior parte delle transazioni DDE. Ad esempio, un server riceve due handle di stringa durante la transazione [**XTYP \_ REQUEST:**](xtyp-request.md) uno identifica una stringa che specifica il nome di un argomento e l'altro identifica una stringa che specifica un nome di elemento. Un'applicazione può ottenere la lunghezza della stringa che corrisponde a un handle di stringa e copiare la stringa in un buffer definito dall'applicazione chiamando la funzione [**DdeQueryString,**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) come illustrato nell'esempio seguente.


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



Non è possibile eseguire il mapping di un handle di stringa specifico dell'istanza dall'handle di stringa alla stringa e di nuovo all'handle di stringa. Ad esempio, anche se [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) crea una stringa da un handle di stringa e quindi [**DdeCreateStringHandle crea**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) un handle di stringa da tale stringa, i due handle non sono uguali, come illustrato nell'esempio seguente.


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



Per confrontare i valori di due handle di stringa, usare [**la funzione DdeCmpStringHandles.**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles)

Un handle di stringa passato alla funzione di callback DDE di un'applicazione non è più valido quando la funzione di callback viene restituita. Un'applicazione può salvare un handle di stringa da usare dopo la fine della funzione di callback usando [**la funzione DdeKeepStringHandle.**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle)

Quando un'applicazione [**chiama DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), il sistema immette la stringa specificata in una tabella di stringhe e genera un handle che usa per accedere alla stringa. Il sistema gestisce anche un conteggio di utilizzo per ogni stringa nella tabella delle stringhe.

Quando un'applicazione chiama [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) e specifica una stringa già esistente nella tabella, il sistema incrementa il numero di utilizzi anziché aggiungere un'altra occorrenza della stringa. Un'applicazione può anche incrementare il numero di utilizzi [**usando DdeKeepStringHandle.**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) Quando un'applicazione chiama [**la funzione DdeFreeStringHandle,**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) il sistema decrementa il numero di utilizzi.

Una stringa viene rimossa dalla tabella quando il conteggio dell'utilizzo è uguale a zero. Poiché più di un'applicazione può ottenere l'handle per una determinata stringa, un'applicazione non deve liberare un handle di stringa più volte di quanto abbia creato o mantenuto l'handle. In caso contrario, l'applicazione può causare la rimozione della stringa dalla tabella, negando ad altre applicazioni l'accesso alla stringa.

Le funzioni di gestione delle stringhe DDEML sono basate sul gestore atom e sono soggette alle stesse restrizioni di dimensione degli atom.

## <a name="ddeml-and-threads"></a>DDEML e thread

La [**funzione DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) registra un'applicazione con DDEML, creando un'istanza DDEML. Un'istanza DDEML è basata su thread, associata al thread che ha **chiamato DdeInitialize.**

Tutte le chiamate di funzione DDEML per gli oggetti appartenenti a un'istanza DDEML devono essere effettuate dallo stesso thread che ha chiamato [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) per creare l'istanza. Se si chiama una funzione DDEML da un thread diverso, la funzione avrà esito negativo. Non è possibile accedere a una conversazione DDEML da un thread diverso da quello che ha allocato la conversazione.

 

