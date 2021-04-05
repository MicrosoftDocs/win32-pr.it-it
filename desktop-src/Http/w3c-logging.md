---
title: Registrazione W3C
description: La registrazione estesa W3C è il tipo di registrazione lato server che può essere abilitata nel gruppo di URL o sessione del server.
ms.assetid: a08b8f9e-2247-43c6-b253-81f72001d8d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b253daebae22a2b99e152451cff360c7b633ca64
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724831"
---
# <a name="w3c-logging"></a>Registrazione W3C

La registrazione estesa W3C è il tipo di registrazione lato server che può essere abilitata nel gruppo di URL o sessione del server. Quando la registrazione W3C è abilitata in un gruppo di URL, la registrazione viene eseguita solo sulle richieste indirizzate al gruppo di URL. Viene creato un file di log separato per ogni gruppo di URL configurato per abilitare la registrazione W3C.

Quando la registrazione W3C è abilitata nella sessione del server, funziona come forma centralizzata di registrazione per tutti i gruppi di URL nella sessione del server. Viene mantenuto un unico file di log per tutti i gruppi di URL nella sessione del server.

La tabella seguente elenca i campi che possono essere registrati dall'API del server HTTP. La tabella contiene un subset delle costanti [**dei \_ \_ campi di log http**](http-log-field--constants.md) . Alcuni dei campi elencati di seguito vengono generati automaticamente dall'API del server HTTP internamente e pertanto non sono contenuti nella struttura [**\_ \_ \_ dei dati dei campi di log http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) . La colonna "visualizzato come" contiene il testo visualizzato nel file di log. I dati nella tabella sono nell'ordine di occorrenza nel record del file di log.

I campi che non sono contrassegnati come "API server HTTP generata" devono essere passati all'interno della struttura di [**\_ \_ \_ dati dei campi del log http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) in base all'applicazione. L'applicazione può generare i campi dalla struttura di [**\_ richiesta http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) passata.



| Campo                            | Visualizzato come      | Descrizione                                                                                                                                | \_ \_ \_ Membro dati dei campi di log http | \_ \_ Costanti campi log http      |
|----------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------|
| Data                             | data            | Data in cui si è verificata l'attività.                                                                                                   | API server HTTP generata.     | \_ \_ data campo registro \_ http           |
| Tempo                             | time            | Ora, in formato UTC (Coordinated Universal Time), in cui si è verificata l'attività.                                                             | API server HTTP generata.     | \_ \_ ora campo registro \_ http           |
| Nome del servizio e numero di istanza | s-sitename      | Il nome del servizio Internet e il numero di istanza in esecuzione nel client.                                                              | ServiceName                    | \_ \_ \_ nome sito campo registro \_ http     |
| Nome server                      | s-computername  | Nome del server in cui è stata generata la voce del file di log.                                                                          | ServerName                     | \_ \_ \_ nome computer campo registro \_ http |
| Indirizzo IP del server                | s-IP            | Indirizzo IP del server in cui è stata generata la voce del file di log.                                                                    | ServerIp                       | \_IP del \_ server del campo di log http \_ \_     |
| Metodo                           | CS-metodo       | Verbo richiesto, ad esempio, un metodo GET.                                                                                             | Metodo                         | \_ \_ Metodo campo registro \_ http         |
| Stem URI                         | cs-uri-stem     | La destinazione del verbo, ad esempio Default.htm.                                                                                          | UriStem                        | \_ \_ \_ Stem URI campo registro \_ http      |
| Query URI                        | cs-uri-query    | Eventuale query che il client sta tentando di eseguire. Una query URI è necessaria solo per le pagine dinamiche. | UriQuery                       | \_ \_ \_ query URI campo registro \_ http     |
| Porta server                      | s-porta          | Numero di porta del server configurato per il servizio.                                                                                 | ServerPort                     | \_porta del \_ server del campo di log http \_ \_   |
| Nome utente                        | nome utente CS     | Nome dell'utente autenticato che ha eseguito l'accesso al server. Gli utenti anonimi sono indicati da un trattino.                                    | UserName                       | \_ \_ \_ nome utente campo registro \_ http     |
| Indirizzo IP client                | c-ip            | Indirizzo IP del client che ha eseguito la richiesta.                                                                                        | ClientIp                       | \_ \_ \_ IP client campo registro \_ http     |
| Versione protocollo                 | versione CS      | Versione del protocollo HTTP utilizzata dal client.                                                                                            | API server HTTP generata.     | \_ \_ versione campo registro \_ http        |
| Agente utente                       | CS (User-Agent)  | Tipo di browser usato dal client.                                                                                                     | UserAgent                      | \_ \_ \_ agente utente campo di log http \_    |
| Cookie                           | CS (cookie)      | Contenuto del cookie inviato o ricevuto, se disponibile.                                                                                        | Cookie                         | \_ \_ cookie campo registro \_ http         |
| Referrer                         | CS (referrer)    | Sito che l'utente ha visitato per ultimo. Questo sito fornisce un collegamento al sito corrente.                                                        | Referrer                       | \_ \_ Referrer campo registro \_ http       |
| Host                             | host CS         | Nome dell'intestazione host, se presente.                                                                                                              | Host                           | \_ \_ host campo registro \_ http           |
| Stato HTTP                      | SC-stato       | Codice di stato HTTP.                                                                                                                      | ProtocolStatus                 | \_ \_ stato campo registro \_ http         |
| Stato secondario protocollo               | SC-SubStatus    | Codice di errore dello stato secondario.                                                                                                                  | SubStatus                      | \_ \_ \_ stato secondario campo registro \_ http    |
| Stato Win32                     | SC-Win32-stato | Codice di stato di Windows.                                                                                                                   | Win32Status                    | \_ \_ \_ Stato Win32 campo registro \_ http  |
| Byte inviati                       | SC-byte        | Numero di byte inviati dal server.                                                                                                    | API server HTTP generata.     | \_byte del campo di log http \_ \_ \_ inviati    |
| Byte ricevuti                   | cs-byte        | Numero di byte ricevuti ed elaborati dal server.                                                                                  | API server HTTP generata.     | \_ \_ byte campo registro \_ http \_ ricezione    |
| Tempo impiegato                       | tempo impiegato      | Durata dell'azione, in millisecondi.                                                                                  | API server HTTP generata.     | \_ \_ tempo campo registro \_ http \_ impiegato    |
| ID flusso                      | streamid          | ID del flusso.                                                                                  | API server HTTP generata.     | \_ \_ \_ ID flusso campo registro \_ http       |



 

Il file di log è un formato basato su testo ASCII personalizzabile. I prefissi dei campi nel file sono definiti come segue:

|     |                           |
|-----|---------------------------|
| s   | Azioni del server.           |
| c   | Azioni client.           |
| SC  | Azioni da server a client. |
| cs  | Azioni da client a server. |



 

L'applicazione può selezionare uno o più campi del file di log esteso W3C. Tuttavia, non tutti i campi conterranno informazioni. Per i campi selezionati ma per i quali non sono disponibili informazioni, viene visualizzato un trattino (-) come segnaposto. Se un campo contiene un carattere non stampabile, l'API server HTTP la sostituisce con un segno più (+) per mantenere il formato del file di log. Questa situazione si verifica in genere con attacchi di virus, quando, ad esempio, un utente malintenzionato invia ritorni a capo e feed di riga che, se non sostituiti con il segno più (+), interrompono il formato del file di log. I campi sono separati da spazi.

Se un campo è abilitato dal gruppo di URL o dalla sessione del server, ma non è selezionato per la richiesta, viene visualizzato nel file di log con un trattino (-) come segnaposto.

I file di log vengono creati quando la prima richiesta arriva al gruppo di URL o alla sessione del server e non vengono creati durante la configurazione della registrazione. Nell'esempio seguente viene illustrata la prima voce di file di log per un file di log W3C con i campi IP client, nome utente, indirizzo IP del server, porta server, metodo, radice URI, query URI, stato e agente utente abilitati:

``` syntax
#Software: Microsoft HTTP Server API 2.0  
#Version: 1.0   // the log file version as it's described by "https://www.w3.org/TR/WD-logfile".
#Date: 2002-05-02 17:42:15  // when the first log file entry was recorded, which is when the entire log file was created.
#Fields: date time c-ip cs-username s-ip s-port cs-method cs-uri-stem cs-uri-query sc-status cs(User-Agent)
2002-05-02 17:42:15 172.22.255.255 - 172.30.255.255 80 GET /images/picture.jpg - 200 Mozilla/4.0+(compatible;MSIE+5.5;+Windows+2000+Server)
```

Il campo relativo al tempo viene inizializzato quando l'API del server HTTP riceve il primo byte, prima che la richiesta venga analizzata. Il timestamp del tempo viene interrotto quando si verifica l'ultimo completamento dell'invio. Il tempo impiegato non riflette il tempo in rete. La prima richiesta al sito mostra un tempo leggermente più lungo di altre richieste analoghe, perché l'API del server HTTP apre il file di log con la prima richiesta.

 

 