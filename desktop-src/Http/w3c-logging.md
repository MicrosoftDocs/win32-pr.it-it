---
title: Registrazione W3C
description: La registrazione estesa W3C è un tipo di registrazione lato server che può essere abilitata nella sessione del server o nel gruppo di URL.
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb53ccf3b6bf5383a0a4da62538b6fa516c500f8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119946"
---
# <a name="w3c-logging"></a>Registrazione W3C

La registrazione estesa W3C è un tipo di registrazione lato server che può essere abilitata nella sessione del server o nel gruppo di URL. Quando la registrazione W3C è abilitata in un gruppo di URL, la registrazione viene eseguita solo sulle richieste indirizzate al gruppo di URL. Viene creato un file di log separato per ogni gruppo di URL configurato per abilitare la registrazione W3C.

Quando la registrazione W3C è abilitata nella sessione del server, funziona come forma centralizzata di registrazione per tutti i gruppi di URL nella sessione del server. Viene mantenuto un singolo file di log per tutti i gruppi di URL nella sessione del server.

La tabella seguente elenca i campi che possono essere registrati dall'API del server HTTP. La tabella contiene un subset delle [**costanti HTTP \_ LOG \_ FIELD.**](http-log-field--constants.md) Alcuni dei campi elencati di seguito vengono generati automaticamente dall'API del server HTTP internamente e pertanto non sono contenuti nella [**struttura HTTP LOG FIELDS \_ \_ \_ DATA.**](/windows/desktop/api/Http/ns-http-http_log_fields_data) La colonna "Appears As" contiene il testo visualizzato nel file di log. I dati nella tabella sono nell'ordine di occorrenza nel record del file di log.

I campi che non sono contrassegnati come "HTTP Server API generated" devono essere passati all'interno della struttura [**HTTP \_ LOG FIELDS \_ \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) dall'applicazione. L'applicazione può generare tali campi dalla [**struttura \_ HTTP REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) passata.



| Campo                            | Viene visualizzato come      | Descrizione                                                                                                                                | Membro \_ dati DEI CAMPI DI LOG \_ \_ HTTP | Costanti \_ HTTP LOG \_ FIELDS      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| Data                             | data            | Data in cui si è verificata l'attività.                                                                                                   | API server HTTP generata.     | HTTP LOG FIELD DATE (DATA \_ \_ CAMPO LOG \_ HTTP)           |
| Ora                             | time            | Ora, in formato UTC (Coordinated Universal Time), in cui si è verificata l'attività.                                                             | API server HTTP generata.     | ORA \_ CAMPO \_ LOG HTTP \_           |
| Nome del servizio e numero di istanza | s-sitename      | Nome del servizio Internet e numero di istanza in esecuzione nel client.                                                              | ServiceName                    | NOME \_ DEL SITO DEL CAMPO DEL \_ \_ LOG \_ HTTP     |
| Nome server                      | s-computername  | Nome del server in cui è stata generata la voce del file di log.                                                                          | ServerName                     | NOME \_ COMPUTER \_ CAMPO \_ LOG \_ HTTP |
| Indirizzo IP del server                | s-ip            | Indirizzo IP del server in cui è stata generata la voce del file di log.                                                                    | ServerIp                       | HTTP \_ LOG \_ FIELD \_ SERVER \_ IP     |
| Metodo                           | cs-method       | Verbo richiesto, ad esempio un metodo GET.                                                                                             | Metodo                         | METODO \_ DEL CAMPO DI LOG \_ \_ HTTP         |
| Origine URI                         | cs-uri-stem     | Destinazione del verbo, ad esempio, Default.htm.                                                                                          | UriStem                        | ORIGINE \_ URI \_ CAMPO \_ LOG \_ HTTP      |
| URI Query                        | cs-uri-query    | Query, se presente, che il client stava tentando di eseguire. Una query URI è necessaria solo per le pagine dinamiche. | UriQuery                       | \_QUERY URI CAMPO LOG \_ \_ \_ HTTP     |
| Porta server                      | s-port          | Numero di porta del server configurato per il servizio.                                                                                 | ServerPort                     | PORTA \_ DEL SERVER DI LOG \_ \_ \_ HTTP   |
| Nome utente                        | cs-username     | Nome dell'utente autenticato che ha eseguito l'accesso al server. Gli utenti anonimi sono indicati da un trattino.                                    | Nome utente                       | NOME \_ UTENTE CAMPO LOG \_ \_ \_ HTTP     |
| Indirizzo IP client                | c-ip            | Indirizzo IP del client che ha eseguito la richiesta.                                                                                        | ClientIp                       | HTTP \_ LOG FIELD CLIENT IP \_ \_ (IP CLIENT CAMPO LOG \_ HTTP)     |
| Versione del protocollo                 | versione cs      | Versione del protocollo HTTP utilizzata dal client.                                                                                            | API server HTTP generata.     | VERSIONE \_ DEL CAMPO DEL LOG \_ \_ HTTP        |
| Agente utente                       | cs(User-Agent)  | Tipo di browser usato dal client.                                                                                                     | UserAgent                      | HTTP \_ LOG \_ FIELD \_ USER \_ AGENT    |
| Cookie                           | cs(Cookie)      | Contenuto del cookie inviato o ricevuto, se presente.                                                                                        | Cookie                         | COOKIE \_ DEL CAMPO DI LOG \_ \_ HTTP         |
| Referrer                         | cs(Referrer)    | Sito visitato per l'ultima volta dall'utente. Questo sito fornisce un collegamento al sito corrente.                                                        | Referrer                       | HTTP \_ LOG \_ FIELD \_ REFERRER (REFERRER CAMPO LOG HTTP)       |
| Host                             | cs-host         | Nome dell'intestazione host, se presente.                                                                                                              | Host                           | \_HOST DEL CAMPO DEL \_ \_ LOG HTTP           |
| Stato HTTP                      | sc-status       | Codice di stato HTTP.                                                                                                                      | ProtocolStatus                 | STATO \_ DEL CAMPO DEL LOG \_ \_ HTTP         |
| Stato secondario del protocollo               | sc-substatus    | Codice di errore di stato secondario.                                                                                                                  | SubStatus                      | STATO \_ \_ SECONDARIO DEL CAMPO \_ DI \_ LOG HTTP    |
| Stato Win32                     | sc-win32-status | Codice di stato di Windows.                                                                                                                   | Win32Status                    | STATO \_ \_ \_ WIN32 DEL CAMPO DI LOG \_ HTTP  |
| Byte inviati                       | sc-bytes        | Numero di byte inviati dal server.                                                                                                    | API del server HTTP generata.     | BYTE DEL CAMPO DEL LOG HTTP \_ \_ \_ \_ INVIATI    |
| Byte ricevuti                   | cs-bytes        | Numero di byte ricevuti ed elaborati dal server.                                                                                  | API del server HTTP generata.     | BYTE DEL CAMPO DEL LOG HTTP \_ \_ \_ \_ RECV    |
| Tempo impiegato                       | tempo impiegato      | Durata dell'azione, in millisecondi.                                                                                  | API del server HTTP generata.     | TEMPO DI CAMPO DEL LOG HTTP \_ \_ \_ \_ IMPIEGATO    |
| ID flusso                      | streamid          | ID flusso.                                                                                  | API del server HTTP generata.     | ID \_ FLUSSO DEL CAMPO DEL \_ \_ \_ LOG HTTP       |



 

Il file di log è un formato ascii personalizzabile basato su testo. I prefissi di campo nel file sono definiti come segue:

| Prefisso    | Descrizione                          |
|-----|---------------------------|
| s   | Azioni del server.           |
| c   | Azioni client.           |
| M.b  | Azioni da server a client. |
| cs  | Azioni da client a server. |



 

L'applicazione può selezionare uno o più campi del file di log esteso W3C, ma non tutti i campi conterranno informazioni. Per i campi selezionati ma per i quali non sono presenti informazioni, come segnaposto viene visualizzato un trattino (-). Se un campo contiene un carattere non stampabile, l'API server HTTP lo sostituisce con un segno più (+) per mantenere il formato del file di log. Ciò si verifica in genere con attacchi di virus, quando, ad esempio, un utente malintenzionato invia ritorni a capo e avanzamento riga che, se non sostituiti con il segno più (+), interrompe il formato del file di log. I campi sono separati da spazi.

Se un campo è abilitato dal gruppo di URL o dalla sessione server, ma non selezionato per la richiesta, viene visualizzato nel file di log con un trattino (-) come segnaposto.

I file di log vengono creati quando la prima richiesta arriva nel gruppo di URL o nella sessione del server e non vengono creati quando viene configurata la registrazione. L'esempio seguente mostra la prima voce del file di log per un file di log W3C con i campi Ip client, Nome utente, IP server, Porta server, Metodo, Uri Stem, Query URI, Stato e Agente utente abilitati:

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

Il campo time-taken viene inizializzato quando l'API del server HTTP riceve il primo byte, prima che la richiesta venga analizzata. Il timestamp impiegato viene arrestato quando si verifica l'ultimo completamento dell'invio. Il tempo impiegato non riflette il tempo nella rete. La prima richiesta al sito mostra un tempo leggermente più lungo rispetto ad altre richieste simili perché l'API server HTTP apre il file di log con la prima richiesta.

 

 