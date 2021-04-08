---
title: Concetti di base
description: In questo argomento vengono illustrati i concetti chiave relativi a Dynamic Data Exchange.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), interazione del server client
- DDE (Dynamic Data Exchange), interazione server client
- scambio di dati, Dynamic Data Exchange (DDE)
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), applicazioni client
- DDE (Dynamic Data Exchange), applicazioni client
- Dynamic Data Exchange (DDE), applicazioni server
- DDE (Dynamic Data Exchange), applicazioni server
- Dynamic Data Exchange (DDE), funzioni di callback
- DDE (Dynamic Data Exchange), funzioni di callback
- Dynamic Data Exchange (DDE), transazioni
- DDE (Dynamic Data Exchange), transazioni
- Dynamic Data Exchange (DDE), nomi di servizio
- DDE (Dynamic Data Exchange), nomi di servizio
- Dynamic Data Exchange (DDE), nomi di elementi
- DDE (Dynamic Data Exchange), nomi di elementi
- Dynamic Data Exchange (DDE), nomi degli argomenti
- DDE (Dynamic Data Exchange), nomi degli argomenti
- Dynamic Data Exchange (DDE), argomento di sistema
- DDE (Dynamic Data Exchange), argomento di sistema
- Libreria di gestione Dynamic Data Exchange (DDEML), inizializzazione
- DDEML (libreria di gestione Dynamic Data Exchange), inizializzazione
- Libreria di gestione Dynamic Data Exchange (DDEML), funzioni di callback
- DDEML (libreria di gestione Dynamic Data Exchange), funzioni di callback
- Libreria di gestione Dynamic Data Exchange (DDEML), gestione delle stringhe
- DDEML (libreria di gestione Dynamic Data Exchange), gestione delle stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c564bffbcbb06ddc3a0e0fa4e0a9ed398d3ca55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727919"
---
# <a name="basic-concepts-dde"></a>Concetti di base (DDE)

Questi concetti sono chiave per comprendere Dynamic Data Exchange (DDE) e la libreria di gestione Dynamic Data Exchange (DDEML).

-   [Interazione tra client e server](#client-and-server-interaction)
-   [Transazioni e funzione di callback DDE](#transactions-and-the-dde-callback-function)
-   [Nomi di servizi, nomi di argomenti e nomi di elementi](#service-names-topic-names-and-item-names)
-   [Argomento di sistema](#system-topic)
-   [Inizializzazione](#initialization)
-   [Funzione di callback](#callback-function)
-   [Gestione delle stringhe](#string-management)
-   [DDEML e thread](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>Interazione tra client e server

Il DDE si verifica sempre tra un'applicazione client e un'applicazione server. L' *applicazione client DDE* avvia lo scambio stabilendo una conversazione con il server per l'invio di transazioni al server. Una transazione è una richiesta di dati o servizi. L' *applicazione server DDE* risponde alle transazioni fornendo dati o servizi al client. Ad esempio, un'applicazione grafica potrebbe contenere un grafico a barre che rappresenta i profitti trimestrali di un'azienda, ma i dati per il grafico a barre potrebbero essere contenuti in un'applicazione del foglio di calcolo. Per ottenere le cifre di profitto più recenti, l'applicazione grafica (il client) potrebbe stabilire una conversazione con l'applicazione del foglio di calcolo (il server). L'applicazione grafica potrebbe quindi inviare una transazione all'applicazione foglio di calcolo, richiedendo le cifre di profitto più recenti.

Un server può avere molti client contemporaneamente e un client può richiedere dati da più server. Un'applicazione può essere anche un client e un server. Il client o il server può terminare la conversazione in qualsiasi momento.

## <a name="transactions-and-the-dde-callback-function"></a>Transazioni e funzione di callback DDE

DDEML notifica a un'applicazione l'attività DDE che influiscono sull'applicazione inviando transazioni alla funzione di callback DDE dell'applicazione. Una *transazione DDE* è simile a un messaggio che è una costante denominata accompagnata da altri parametri che contengono informazioni aggiuntive sulla transazione.

DDEML passa una transazione a una funzione di callback DDE definita dall'applicazione che esegue un'azione appropriata per il tipo di transazione. Ad esempio, quando un'applicazione client tenta di stabilire una conversazione con un'applicazione server, il client chiama la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) . Questa funzione fa in modo che DDEML invii una transazione di [**\_ connessione XTYP**](xtyp-connect.md) alla funzione di callback DDE del server. La funzione di callback può consentire la conversazione restituendo **true** a DDEML oppure può negare la conversazione restituendo **false**. Per una descrizione dettagliata delle transazioni, vedere [gestione delle](transaction-management.md)transazioni.

## <a name="service-names-topic-names-and-item-names"></a>Nomi di servizi, nomi di argomenti e nomi di elementi

Un server DDE utilizza un nome di servizio della gerarchia a tre livelli (denominato "nome applicazione" nella documentazione DDE precedente), il nome dell'argomento e il nome dell'elemento per identificare in modo univoco un'unità di dati che il server può scambiare durante una conversazione.

Un *nome di servizio* è una stringa a cui risponde un'applicazione server quando un client tenta di stabilire una conversazione con il server. Un client deve specificare il nome del servizio per stabilire una conversazione con il server. Sebbene un server possa rispondere a molti nomi di servizio, la maggior parte dei server risponde a un solo nome.

Il *nome* di un argomento è una stringa che identifica un contesto dati logico. Per i server che operano su documenti basati su file, i nomi degli argomenti sono in genere nomi file; per gli altri server, si tratta di altre stringhe specifiche dell'applicazione. Un client deve specificare un nome di argomento insieme al nome del servizio di un server durante il tentativo di stabilire una conversazione con un server.

Il *nome* di un elemento è una stringa che identifica un'unità di dati che un server può passare a un client durante una transazione. Ad esempio, un nome di elemento può identificare un numero intero, una stringa, diversi paragrafi di testo o una bitmap.

I nomi di servizio, argomento e elemento consentono al client di stabilire una conversazione con un server e di ricevere i dati dal server.

## <a name="system-topic"></a>Argomento di sistema

L'argomento System fornisce un contesto per informazioni di interesse generale per qualsiasi client DDE. È consigliabile che le applicazioni server supportino l'argomento di sistema in qualsiasi momento. L'argomento di sistema è definito in DDEML. File di intestazione H come \_ argomento SZDDESYS.

Per determinare quali server sono presenti e i tipi di informazioni che possono fornire, un'applicazione client può richiedere una conversazione nell'argomento del sistema all'avvio, impostando il nome del dispositivo su **null**. Queste conversazioni con caratteri jolly sono costose in termini di prestazioni del sistema, pertanto devono essere conservate come minimo. Per ulteriori informazioni sull'avvio delle conversazioni DDE, vedere [gestione conversazioni](conversation-management.md).

Un server deve supportare i nomi di elemento seguenti all'interno dell'argomento di sistema e di qualsiasi altro nome di elemento utile a un client.



| Elemento                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| elemento SZDDE Item \_ \_    | Elenco degli elementi supportati in un argomento non di sistema. (Questo elenco può variare a seconda del momento e dall'argomento all'argomento).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \_formati di elementi SZDDESYS \_  | Elenco di stringhe delimitate da tabulazioni che rappresentano tutti i formati degli Appunti potenzialmente supportati dall'applicazione di servizio. Le stringhe che rappresentano formati degli appunti predefiniti sono equivalenti ai \_ valori CF con il prefisso "CF \_ " rimosso. Ad esempio, il \_ formato del testo CF è rappresentato dalla stringa "Text". Queste stringhe devono essere maiuscole per identificarle ulteriormente come formati predefiniti. L'elenco dei formati deve comparire nell'ordine di contenuto più completo per il contenuto meno ricco. Per ulteriori informazioni sui formati degli Appunti e sul rendering dei dati, vedere [Appunti](clipboard.md).<br/> |
| \_Guida dell'elemento SZDDESYS \_     | Informazioni leggibili dall'utente di interesse generale. Questo elemento deve contenere almeno le informazioni su come utilizzare le funzionalità DDE dell'applicazione server. Queste informazioni possono includere, a differenza di, come specificare gli elementi all'interno degli argomenti, quali sono le stringhe di esecuzione che il server può eseguire, le transazioni poke consentite e come trovare la guida per altri elementi dell'argomento di sistema.                                                                                                                                                                                                                           |
| \_elemento SZDDESYS \_ RTNMSG   | Dettagli di supporto per il messaggio [**\_ \_ ACK DDE WM**](wm-dde-ack.md) usato più di recente. Questo elemento è utile quando sono necessari più di 8 bit di dati restituiti specifici dell'applicazione.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_stato elemento \_ SZDDESYS   | Indica lo stato corrente del server. In genere, questo elemento supporta solo il \_ formato di testo CF e contiene la stringa pronta o occupata.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_elemento SZDDESYS \_ SYSITEMS | Elenco degli elementi supportati nell'argomento di sistema da questo server.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_argomenti sugli elementi di SZDDESYS \_   | Elenco degli argomenti supportati dal server al momento corrente. Questo elenco può variare a seconda del momento.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Questi nomi di elemento sono valori definiti in DDEML. File di intestazione H. Per ottenere handle di stringa per queste stringhe, un'applicazione deve usare le funzioni di gestione delle stringhe DDEML, così come per qualsiasi altra stringa in un'applicazione DDEML. Per ulteriori informazioni sulla gestione delle stringhe, vedere [gestione delle](#string-management)stringhe.

## <a name="initialization"></a>Inizializzazione

Prima di chiamare qualsiasi altra funzione DDEML, un'applicazione deve chiamare la funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . **DdeInitialize** ottiene un identificatore di istanza per l'applicazione, registra la funzione di callback DDE dell'applicazione con il DDE e specifica i flag di filtro delle transazioni per la funzione di callback.

Ogni istanza di un'applicazione o di una DLL deve passare il relativo identificatore di istanza come parametro *idInst* a qualsiasi altra funzione DDEML che la richiede. Lo scopo di più istanze di DDEML è supportare le dll che devono usare il DDEML nello stesso momento in cui viene usato da un'applicazione. Un'applicazione non deve usare più di un'istanza di DDEML.

I *filtri di transazione* ottimizzano le prestazioni del sistema impedendo al DDEML di passare transazioni indesiderate alla funzione di callback DDE dell'applicazione. Un'applicazione imposta i filtri delle transazioni nel parametro [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* Un'applicazione deve specificare un flag di filtro delle transazioni per ogni tipo di transazione che non elabora nella funzione di callback. Un'applicazione può modificare i filtri delle transazioni con una chiamata successiva a **DdeInitialize**. Per ulteriori informazioni sulle transazioni, vedere [gestione delle transazioni](transaction-management.md).

Nell'esempio seguente viene illustrato come inizializzare un'applicazione per l'utilizzo di DDEML.


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



Un'applicazione deve chiamare la funzione [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) quando non USERÀ più DDEML. Questa funzione termina tutte le conversazioni attualmente aperte per l'applicazione e libera le risorse DDEML allocate dal sistema per l'applicazione.

## <a name="callback-function"></a>Funzione di callback

Un'applicazione che utilizza DDEML deve fornire una funzione di callback che elabora gli eventi DDE che interessano l'applicazione. DDEML notifica a un'applicazione questi eventi inviando transazioni alla funzione di callback DDE dell'applicazione. Le transazioni ricevute da una funzione di callback dipendono dal fatto che il filtro di callback contrassegna l'applicazione specificata in [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) e se l'applicazione è un client, un server o entrambi. Per ulteriori informazioni, vedere [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).

Nell'esempio seguente viene illustrata la struttura generale di una funzione di callback per una tipica applicazione client.


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



Il parametro *uType* specifica il tipo di transazione inviato alla funzione di callback da DDEML. I valori dei parametri rimanenti dipendono dal tipo di transazione. I tipi di transazione e gli eventi che li generano sono descritti negli argomenti seguenti. Per informazioni dettagliate su ogni tipo di transazione, vedere [gestione delle transazioni](transaction-management.md).

## <a name="string-management"></a>Gestione delle stringhe

Per eseguire un'attività DDE, molte funzioni DDEML richiedono l'accesso alle stringhe. Un client, ad esempio, deve specificare un nome di servizio e un nome di argomento quando chiama la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) per richiedere una conversazione con un server. Un'applicazione specifica una stringa passando un handle di stringa (HSZ) anziché un puntatore in una funzione DDEML. Un *handle di stringa* è un valore **DWORD** , assegnato dal sistema, che identifica una stringa.

Un'applicazione può ottenere un handle di stringa per una determinata stringa chiamando la funzione [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) . Questa funzione registra la stringa con il sistema e restituisce un handle di stringa per l'applicazione. L'applicazione può passare l'handle alle funzioni DDEML che devono accedere alla stringa. Nell'esempio seguente vengono ottenuti handle di stringa per la stringa dell'argomento di sistema e la stringa del nome del servizio.


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



Il parametro *idInst* nell'esempio precedente specifica l'identificatore di istanza ottenuto dalla funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

La funzione di callback DDE di un'applicazione riceve uno o più handle di stringa durante la maggior parte delle transazioni DDE. Ad esempio, un server riceve due handle di stringa durante la transazione della [**\_ richiesta XTYP**](xtyp-request.md) : uno identifica una stringa che specifica un nome di argomento e l'altro identifica una stringa che specifica il nome di un elemento. Un'applicazione può ottenere la lunghezza della stringa che corrisponde a un handle di stringa e copiare la stringa in un buffer definito dall'applicazione chiamando la funzione [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) , come illustrato nell'esempio seguente.


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



Non è possibile eseguire il mapping di un handle di stringa specifico dell'istanza da un handle di stringa a una stringa e viceversa. Ad esempio, sebbene [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) crei una stringa da un handle di stringa e quindi [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) crei un handle di stringa da tale stringa, i due handle non sono uguali, come illustrato nell'esempio seguente.


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



Per confrontare i valori di due handle di stringa, usare la funzione [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) .

Un handle di stringa passato alla funzione di callback DDE di un'applicazione diventa non valido quando la funzione di callback restituisce. Un'applicazione può salvare un handle di stringa da utilizzare dopo che la funzione di callback viene restituita utilizzando la funzione [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) .

Quando un'applicazione chiama [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), il sistema immette la stringa specificata in una tabella di stringhe e genera un handle che usa per accedere alla stringa. Il sistema gestisce anche un conteggio di utilizzo per ogni stringa nella tabella di stringhe.

Quando un'applicazione chiama [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) e specifica una stringa già esistente nella tabella, il sistema incrementa il conteggio di utilizzo anziché aggiungere un'altra occorrenza della stringa. Un'applicazione può anche incrementare il conteggio di utilizzo usando [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle). Quando un'applicazione chiama la funzione [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) , il sistema decrementa il conteggio dell'utilizzo.

Una stringa viene rimossa dalla tabella quando il conteggio di utilizzo è uguale a zero. Poiché più di un'applicazione può ottenere l'handle per una determinata stringa, un'applicazione non deve liberare un handle di stringa più volte rispetto a quando ha creato o mantenuto l'handle. In caso contrario, l'applicazione può causare la rimozione della stringa dalla tabella, negando ad altre applicazioni l'accesso alla stringa.

Le funzioni di gestione delle stringhe DDEML sono basate su Atom Manager e sono soggette alle stesse restrizioni di dimensione degli atomi.

## <a name="ddeml-and-threads"></a>DDEML e thread

La funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) registra un'applicazione con DDEML, creando un'istanza di DDEML. Un'istanza di DDEML è basata su thread, associata al thread che ha chiamato **DdeInitialize**.

Tutte le chiamate di funzione DDEML per gli oggetti appartenenti a un'istanza di DDEML devono essere effettuate dallo stesso thread che ha chiamato [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) per creare l'istanza. Se si chiama una funzione DDEML da un thread diverso, la funzione avrà esito negativo. Non è possibile accedere a una conversazione DDEML da un thread diverso da quello che ha allocato la conversazione.

 

