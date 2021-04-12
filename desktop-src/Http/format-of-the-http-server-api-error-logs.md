---
title: Formato dei log degli errori dell'API del server HTTP
description: In generale, i file di log degli errori dell'API del server HTTP hanno lo stesso formato dei log degli errori W3C, ad eccezione del fatto che i file di log degli errori dell'API server HTTP non contengono intestazioni di colonna.
ms.assetid: 436f898c-9063-4aee-b276-e6ab935e3606
keywords:
- API server HTTP, formato log degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2eb914251a809178adef28c8a61b1a174c6e86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221127"
---
# <a name="format-of-the-http-server-api-error-logs"></a>Formato dei log degli errori dell'API del server HTTP

In generale, i file di log degli errori dell'API del server HTTP hanno lo stesso formato dei log degli errori W3C, ad eccezione del fatto che i file di log degli errori dell'API server HTTP non contengono intestazioni di colonna. Ogni riga di un log degli errori dell'API del server HTTP registra un errore con i campi in un ordine specifico. Ogni campo è separato dal campo precedente per un singolo carattere di spazio (0x0020). All'interno di ogni campo, i caratteri di spazio, le tabulazioni e i caratteri di controllo non stampabili vengono sostituiti da segni più (0x002B).

Nella tabella seguente vengono identificati i campi e l'ordine dei campi in un record del log degli errori.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Date"></span><span id="date"></span><span id="DATE"></span>Data<br/></td>
<td>Il campo della data segue il formato W3C ed è basato sull'ora UTC (Coordinated Universal Time). Il campo della data è sempre di 10 caratteri nel formato &quot; aaaa-mm-gg &quot; . Ad esempio, il 1 ° maggio 2003 è espresso come &quot; 2003-05-01 &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="Time"></span><span id="time"></span><span id="TIME"></span>Tempo<br/></td>
<td>Il campo time segue il formato W3C ed è basato su UTC. Il campo dell'ora è sempre di 8 caratteri nel formato &quot; mm: HH: SS &quot; . Ad esempio, 5:30 PM (UTC) viene espresso come &quot; 17:30:00 &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="Client_IP_Address"></span><span id="client_ip_address"></span><span id="CLIENT_IP_ADDRESS"></span>Indirizzo IP client<br/></td>
<td>Indirizzo IP del client interessato che può essere un indirizzo IPv4 o un indirizzo IPv6. Se l'indirizzo IP del client è un indirizzo IPv6, anche il campo elemento ScopeId viene incluso nell'indirizzo.<br/></td>
</tr>
<tr class="even">
<td><span id="Client_Port"></span><span id="client_port"></span><span id="CLIENT_PORT"></span>Porta client<br/></td>
<td>Numero di porta per il client interessato.<br/></td>
</tr>
<tr class="odd">
<td><span id="Server_IP_Address"></span><span id="server_ip_address"></span><span id="SERVER_IP_ADDRESS"></span>Indirizzo IP del server<br/></td>
<td>Indirizzo IP del server interessato che può essere un indirizzo IPv4 o un indirizzo IPv6. Se l'indirizzo IP del server è un indirizzo IPv6, anche il campo elemento ScopeId viene incluso nell'indirizzo.<br/></td>
</tr>
<tr class="even">
<td><span id="Server_Port"></span><span id="server_port"></span><span id="SERVER_PORT"></span>Porta server<br/></td>
<td>Numero di porta del server interessato.<br/></td>
</tr>
<tr class="odd">
<td><span id="Protocol_Version"></span><span id="protocol_version"></span><span id="PROTOCOL_VERSION"></span>Versione protocollo<br/></td>
<td>Versione del protocollo in uso. <br/>
<ul>
<li>Se la connessione non è stata analizzata abbastanza per determinare la versione del protocollo, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</li>
<li>Se il numero di versione principale o secondario analizzato è maggiore o uguale a 10, la versione viene registrata come &quot; http/?.? &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo<br/></td>
<td>Stato del verbo passato dall'ultima richiesta analizzata. Sono inclusi verbi sconosciuti, ma qualsiasi verbo che supera i 255 byte viene troncato a questa lunghezza. Se un verbo non è disponibile, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.<br/></td>
</tr>
<tr class="odd">
<td><span id="CookedURL___Query"></span><span id="cookedurl___query"></span><span id="COOKEDURL___QUERY"></span>CookedURL + query<br/></td>
<td>L'URL e qualsiasi query associata vengono registrati come un solo campo, separati da un punto interrogativo (0x3F). Questo campo è troncato al limite di lunghezza di 4096 byte.
<ul>
<li>Se l'URL è stato analizzato ( &quot; cotto &quot; ), viene registrato con la conversione della tabella codici locale e viene considerato come un campo Unicode.</li>
<li>Se questo URL non è stato analizzato ( &quot; cotto &quot; ) al momento della registrazione, viene copiato esattamente, senza alcuna conversione Unicode.</li>
<li>Se l'API del server HTTP non è in grado di analizzare questo URL, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="Protocol_Status"></span><span id="protocol_status"></span><span id="PROTOCOL_STATUS"></span>Stato protocollo<br/></td>
<td>Lo stato del protocollo non può essere maggiore di 999. <br/>
<ul>
<li>Se lo stato del protocollo della risposta a una richiesta è disponibile, viene registrato in questo campo.</li>
<li>Se lo stato del protocollo non è disponibile, viene usato un trattino (0x002D) come segnaposto per il campo vuoto.</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SiteId"></span><span id="siteid"></span><span id="SITEID"></span>SiteId<br/></td>
<td>Non usato in questa versione dell'API del server HTTP. In questo campo viene sempre visualizzato un trattino del segnaposto (0x002D).<br/></td>
</tr>
<tr class="even">
<td><span id="Reason_Phrase"></span><span id="reason_phrase"></span><span id="REASON_PHRASE"></span>Frase motivo<br/></td>
<td>Questo campo contiene una stringa che identifica il tipo di errore registrato. Non viene mai lasciata vuota.<br/></td>
</tr>
</tbody>
</table>



 

Le righe di esempio seguenti proseguono da un log degli errori dell'API del server HTTP:

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

 

 





