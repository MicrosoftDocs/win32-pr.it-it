---
title: Formato dei log degli errori dell'API del server HTTP
description: In generale, i file di log degli errori dell'API server HTTP hanno lo stesso formato dei log degli errori W3C, ad eccezione del fatto che i file di log degli errori dell'API server HTTP non contengono intestazioni di colonna.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API server HTTP, formato del log degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e666e29178695482b05cfef6bdd252fb35072b7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477777"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Formato dei log degli errori dell'API del server HTTP

In generale, i file di log degli errori dell'API server HTTP hanno lo stesso formato dei log degli errori W3C, ad eccezione del fatto che i file di log degli errori dell'API server HTTP non contengono intestazioni di colonna. Ogni riga di un log degli errori dell'API server HTTP registra un errore con i campi in un ordine specifico. Ogni campo è separato dal campo precedente da uno spazio singolo (0x0020). All'interno di ogni campo, gli spazi, le tabulazioni e i caratteri di controllo non stampabili vengono sostituiti da segni più (0x002B).

La tabella seguente identifica i campi e l'ordine dei campi in un record del log degli errori.




| Campo | Descrizione | 
|-------|-------------|
| <span id="Date"></span><span id="date"></span><span id="DATE"></span>Data<br /> | Il campo Date segue il formato W3C ed è basato Coordinated Universal Time (UTC). Il campo Date è sempre di 10 caratteri nel formato "AAAA-MM-GG". Ad esempio, il 1° maggio 2003 viene espresso come "2003-05-01".<br /> | 
| <span id="Time"></span><span id="time"></span><span id="TIME"></span>Tempo<br /> | Il campo Time segue il formato W3C ed è basato su UTC. Il campo time è sempre di 8 caratteri nel formato "MM:HH:SS". Ad esempio, alle 17:30 (UTC) viene espresso come "17:30:00".<br /> | 
| <span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Indirizzo IP client<br /> | Indirizzo IP del client interessato che può essere un indirizzo IPv4 o un indirizzo IPv6. Se l'indirizzo IP del client è un indirizzo IPv6, anche il campo ScopeId viene incluso nell'indirizzo.<br /> | 
| <span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Porta client<br /> | Numero di porta per il client interessato.<br /> | 
| <span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Indirizzo IP del server<br /> | Indirizzo IP del server interessato che può essere un indirizzo IPv4 o un indirizzo IPv6. Se l'indirizzo IP del server è un indirizzo IPv6, anche il campo ScopeId viene incluso nell'indirizzo.<br /> | 
| <span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Porta server<br /> | Numero di porta del server interessato.<br /> | 
| <span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versione del protocollo<br /> | Versione del protocollo in uso. <br /><ul><li>Se la connessione non è stata analizzata abbastanza per determinare la versione del protocollo, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</li><li>Se il numero di versione principale o secondario analizzato è maggiore o uguale a 10, la versione viene registrata come "HTTP/?.?".</li></ul> | 
| <span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo<br /> | Stato del verbo passato dall'ultima richiesta analizzata. Sono inclusi verbi sconosciuti, ma qualsiasi verbo di lunghezza superiore a 255 byte viene troncato a questa lunghezza. Se un verbo non è disponibile, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.<br /> | 
| <span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + Query<br /> | L'URL e qualsiasi query associata vengono registrati come un unico campo, separati da un punto interrogativo (0x3F). Questo campo viene troncato al limite di lunghezza di 4096 byte.<ul><li>Se questo URL è stato analizzato ("cotto"), viene registrato con la conversione della tabella codici locale e viene considerato un campo Unicode.</li><li>Se questo URL non è stato analizzato ("cotto") al momento della registrazione, viene copiato esattamente, senza alcuna conversione Unicode.</li><li>Se l'API server HTTP non è in grado di analizzare questo URL, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</li></ul><br /> | 
| <span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Stato del protocollo<br /> | Lo stato del protocollo non può superare 999. <br /><ul><li>Se lo stato del protocollo della risposta a una richiesta è disponibile, viene registrato in questo campo.</li><li>Se lo stato del protocollo non è disponibile, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</li></ul> | 
| <span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>Siteid<br /> | Non usato in questa versione dell'API del server HTTP. Un trattino segnaposto (0x002D) viene sempre visualizzato in questo campo.<br /> | 
| <span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase del motivo<br /> | Questo campo contiene una stringa che identifica il tipo di errore registrato. Non viene mai lasciato vuoto.<br /> | 




 

Le righe di esempio seguenti derivano da un log degli errori dell'API del server HTTP:

``` syntax
2002-07-05 18:45:09 172.31.77.6 2094 172.31.77.6 80 
                    HTTP/1.1 GET /qos/1kbfile.txt 503 - ConnLimit
2002-07-05 19:51:59 127.0.0.1 2780 127.0.0.1 80 
                    HTTP/1.1 GET /ThisIsMyUrl.htm 400 - Hostname
2002-07-05 19:53:00 127.0.0.1 2894 127.0.0.1 80 
                    HTTP/2.0 GET / 505 - Version_N/S
2002-07-05 20:06:01 172.31.77.6 64388 127.0.0.1 80 
                    - - - - - Timer_MinBytesPerSecond
```

 

 





