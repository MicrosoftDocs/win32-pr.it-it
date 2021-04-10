---
description: Esistono due modi per determinare la procedura di diagnostica da usare.
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: Introduzione con la risoluzione dei problemi di WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12396ea656423772d35dbd4ca237c7c536dcdaf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226925"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>Introduzione con la risoluzione dei problemi di WSDAPI

Questa guida alla risoluzione dei problemi contiene un set di [procedure di diagnostica](wsdapi-diagnostic-procedures.md) che possono essere usate per identificare la cause dei problemi dell'applicazione. Una volta individuata correttamente la causa del problema, è possibile applicare le soluzioni suggerite nella procedura di diagnostica per risolvere il problema.

Esistono due modi per determinare la procedura di diagnostica da usare. Un modo consiste nell'accedere alla pagina risoluzione dei problemi per il tipo di client per visualizzare un elenco dettagliato delle procedure di diagnostica da utilizzare per la risoluzione dei problemi del client. In alternativa, è possibile passare al riferimento rapido per la risoluzione dei problemi riportato di seguito per visualizzare le tabelle di riepilogo che mostrano problemi comuni con le applicazioni WSDAPI e le procedure da usare per diagnosticare i problemi.

## <a name="troubleshooting-by-type-of-client"></a>Risoluzione dei problemi in base al tipo di client

Negli argomenti seguenti vengono illustrate le procedure di diagnostica pertinenti in base al tipo di client. In questi argomenti vengono inoltre illustrati i modelli di messaggio associati al tipo di client.

-   [Risoluzione dei problemi relativi alle applicazioni WSDAPI con individuazione diretta](troubleshooting-applications-using-directed-discovery.md)
-   [Risoluzione dei problemi relativi ai client di individuazione delle funzioni](troubleshooting-function-discovery-clients.md)
-   [Risoluzione dei problemi di persone nelle vicinanze/riunioni](troubleshooting-people-near-me-meetings-near-me.md)
-   [Risoluzione dei problemi relativi all'aggiunta guidata stampante](troubleshooting-the-add-printer-wizard.md)
-   [Risoluzione dei problemi di Esplora reti](troubleshooting-the-network-explorer.md)
-   [Risoluzione dei problemi relativi alla procedura guidata del proiettore](troubleshooting-the-projector-wizard.md)
-   [Risoluzione dei problemi relativi ad altre applicazioni WSDAPI](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>Riferimento rapido per la risoluzione dei problemi

Le tabelle seguenti illustrano alcuni problemi che possono impedire a client e host WSDAPI di vedere reciprocamente la rete e di scambiare i metadati del dispositivo. Vengono inoltre illustrate le procedure di diagnostica da eseguire e i criteri da utilizzare per valutare se l'applicazione soffre di un particolare problema.

### <a name="network-environment-problems"></a>Problemi relativi all'ambiente di rete



| Problema                                                                                                                                                                                              | Procedura di diagnostica                                                                                                                                                                                                                             | Identificazione del problema                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il firewall blocca il traffico di individuazione della rete.                                                                                                                                                       | [Controllo delle impostazioni di adapter e firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | L'abilitazione dell'eccezione di individuazione di rete nel firewall risolve il problema.                                                                                                                      |
| Le eccezioni del firewall specifiche per l'applicazione stanno bloccando i messaggi.                                                                                                                               | [Controllo delle impostazioni di adapter e firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | La disabilitazione del firewall risolve il problema. WF. msc Mostra le regole del firewall specifiche dell'applicazione.                                                                                                      |
| Il dispositivo non risponde alle richieste UDP inviando un messaggio [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) in modo tempestivo (meno di 4 secondi). | [Controllo delle impostazioni di adapter e firewall](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | La disabilitazione del firewall risolve il problema e un host generico che risponde in meno di 4 secondi funziona correttamente.                                                                            |
| Il contesto di sicurezza dell'applicazione non è corretto (ovvero il client e l'host non dispongono di autorizzazioni adeguate per la rete).                                                                 | [Utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) o [l'utilizzo di un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md) | L'indirizzo del dispositivo non viene visualizzato nell'output del client di debug WSD. L'esecuzione dell'applicazione come amministratore risolve il problema.                                                                          |
| Un criterio IPSec blocca i messaggi.                                                                                                                                                                | [Utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) o [l'utilizzo di un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md) | L'indirizzo del dispositivo non viene visualizzato nell'output del client di debug WSD. Il problema non viene risolto disabilitando il firewall. Non è possibile riprodurre il problema in un computer che non è soggetto a nessun criterio IPSec. |



 

### <a name="discovery-traffic-problems"></a>Problemi relativi al traffico di individuazione



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problema</th>
<th>Procedura di diagnostica</th>
<th>Identificazione del problema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>I messaggi <a href="hello-message.md">Hello</a>, <a href="probe-message.md">Probe</a>o <a href="resolve-message.md">Resolve</a> non vengono trasmessi in rete perché l'applicazione non enumera correttamente le interfacce di rete multicast.</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Uso del client di debug WSD per verificare il traffico multicast</a></td>
<td>I messaggi Hello, probe o Resolve non vengono visualizzati nell'output del client di debug WSD. I pacchetti non vengono visualizzati nella rete. I pacchetti non vengono generati per l'interfaccia di loopback o per altre interfacce.</td>
</tr>
<tr class="even">
<td>I messaggi <a href="probe-message.md">Probe</a> non vengono inviati dal multicast UDP alla porta 3702 (per le applicazioni che non usano l'individuazione diretta).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a></td>
<td>Il controllo del messaggio indica che è stato inviato alla porta errata.</td>
</tr>
<tr class="odd">
<td>Il messaggio <a href="probe-message.md">Probe</a> non contiene un elemento <strong>types</strong> oppure l'elemento <strong>types</strong> è vuoto.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">controllo delle tracce di rete per le applicazioni tramite l'individuazione diretta</a></td>
<td>L'ispezione del messaggio indica che l'elemento dei <strong>tipi</strong> non è presente o è vuoto.</td>
</tr>
<tr class="even">
<td>L'elemento <strong>types</strong> di un messaggio <a href="probe-message.md">Probe</a> non contiene i tipi a cui un host risponderà.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">controllo delle tracce di rete per le applicazioni tramite l'individuazione diretta</a></td>
<td>L'ispezione del messaggio indica che l'elemento <strong>types</strong> contiene un valore non valido o non corretto.</td>
</tr>
<tr class="odd">
<td>Un messaggio <a href="probematches-message.md">ProbeMatches</a> non è stato inviato unicast alla porta UDP dalla quale è stato inviato il <a href="probe-message.md">Probe</a> .</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">controllo delle tracce di rete per le applicazioni tramite l'individuazione diretta</a></td>
<td>Il controllo dell'output mostra che non è stato inviato alcun messaggio <a href="probematches-message.md">ProbeMatches</a>o che il messaggio è stato inviato alla porta errata.
<blockquote>
[!Note]<br />
Per le applicazioni che usano l'individuazione diretta, il <a href="probematches-message.md">ProbeMatches</a> deve essere inviato tramite http o HTTPS in risposta al messaggio <a href="probe-message.md">Probe</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Il messaggio <a href="probematches-message.md">ProbeMatches</a> non contiene un elemento <strong>reultimissimo</strong> oppure l'elemento <strong>reultimissimo</strong> è vuoto.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">controllo delle tracce di rete per le applicazioni tramite l'individuazione diretta</a></td>
<td>L'ispezione del messaggio indica che l'elemento <strong>Repiù recente</strong> non è presente o è vuoto.</td>
</tr>
<tr class="odd">
<td>Il valore dell'elemento <strong>Reultimissimo</strong> in un messaggio <a href="probematches-message.md">ProbeMatches</a> non corrisponde al valore dell'elemento <strong>MessageID</strong> del messaggio <a href="probe-message.md">Probe</a> corrispondente.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">controllo delle tracce di rete per le applicazioni tramite l'individuazione diretta</a></td>
<td>L'ispezione del messaggio indica che l'elemento <strong>Latest</strong> contiene un valore non valido o non corretto.</td>
</tr>
<tr class="even">
<td>L'elemento <strong>XAddrs</strong> incluso in un messaggio <a href="probematches-message.md">ProbeMatches</a> non è conforme alle <a href="xaddr-validation-rules.md">regole di convalida XAddr</a>.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">controllo delle tracce di rete per le applicazioni tramite l'individuazione diretta</a></td>
<td>L'ispezione del messaggio indica che <strong>XAddrs</strong> non sono validi.</td>
</tr>
<tr class="odd">
<td>I messaggi di <a href="resolve-message.md">risoluzione</a> non vengono inviati dal multicast UDP alla porta 3702 (per le applicazioni che non usano l'individuazione diretta).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">controllo delle tracce di rete per le applicazioni tramite l'individuazione diretta</a></td>
<td>Il controllo dell'output mostra che il messaggio di <a href="resolve-message.md">risoluzione</a> è stato inviato alla porta errata.</td>
</tr>
<tr class="even">
<td>Un messaggio <a href="resolvematches-message.md">ResolveMatches</a> non è stato inviato unicast alla porta UDP dalla quale è stato inviato un messaggio di <a href="resolve-message.md">risoluzione</a> .</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Controllo delle tracce di rete per UDP WS-Discovery</a> o <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">controllo delle tracce di rete per le applicazioni tramite l'individuazione diretta</a></td>
<td>Il controllo dell'output mostra che non è stato inviato alcun messaggio <a href="resolvematches-message.md">ResolveMatches</a> o che il messaggio è stato inviato alla porta errata.</td>
</tr>
</tbody>
</table>



 

### <a name="metadata-exchange-problems"></a>Problemi di scambio di metadati



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Problema</th>
<th>Procedura di diagnostica</th>
<th>Identificazione del problema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>L'indirizzo di trasporto annunciato dall'host non è corretto.</td>
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Uso di un host e di un client generici per lo scambio di metadati HTTP</a></td>
<td>L'ispezione del XAddrs nell'output del client di debug WSD Mostra che l'indirizzo di trasporto è errato o non valido.</td>
</tr>
<tr class="even">
<td>Non è stato possibile stabilire una connessione TCP per lo scambio di metadati.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>L'output dell'analizzatore di pacchetti non Mostra lo scambio di pacchetti seguente:
<ul>
<li>Pacchetto TCP SYN inviato dal client</li>
<li>Un pacchetto TCP SYN/ACK inviato dall'host</li>
<li>Un pacchetto TCP ACK inviato dal client</li>
</ul></td>
</tr>
<tr class="odd">
<td>Il client non ha inviato una richiesta HTTP GET valida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>Non è presente alcuna richiesta HTTP GET nell'output dell'analizzatore di pacchetti oppure il formato della richiesta non è corretto.</td>
</tr>
<tr class="even">
<td>Il client non ha inviato un messaggio di WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> valido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>Nessun messaggio di WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> nell'output dell'analizzatore di pacchetti oppure il formato del messaggio non è corretto.</td>
</tr>
<tr class="odd">
<td>L'host non è in ascolto sul percorso URL specificato nella richiesta HTTP GET.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>Non è presente alcuna risposta HTTP nell'output dell'analizzatore di pacchetti.</td>
</tr>
<tr class="even">
<td>Il messaggio WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> non contiene un elemento <strong>to</strong> oppure l'elemento <strong>to</strong> è vuoto.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>L'ispezione del messaggio indica che l'elemento <strong>to</strong> non è presente o vuoto.</td>
</tr>
<tr class="odd">
<td>Il valore dell'elemento <strong>to</strong> di un messaggio WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> non corrisponde a uno degli indirizzi endpoint dell'host.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>L'ispezione del messaggio indica che il valore dell'elemento <strong>to</strong> non corrisponde a uno degli indirizzi endpoint annunciati nel messaggio <a href="probematches-message.md">ProbeMatches</a> o <a href="resolvematches-message.md">ResolveMatches</a> dell'host.</td>
</tr>
<tr class="even">
<td>L'host non ha inviato un'intestazione di risposta HTTP valida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>Non è presente alcuna risposta HTTP nell'output dell'analizzatore di pacchetti oppure il formato della richiesta non è valido.</td>
</tr>
<tr class="odd">
<td>L'intestazione della risposta HTTP inviata dall'host indica che non è possibile completare la richiesta.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>L'intestazione della risposta ha un codice di stato diverso da HTTP/1.1 200.</td>
</tr>
<tr class="even">
<td>L'host non ha inviato un messaggio <a href="getresponse--metadata-exchange--message.md">GetResponse</a> valido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>Nessun messaggio <a href="getresponse--metadata-exchange--message.md">GetResponse</a> nell'output dell'analizzatore di pacchetti oppure il formato del messaggio non è corretto.</td>
</tr>
<tr class="odd">
<td>Il messaggio <a href="getresponse--metadata-exchange--message.md">GetResponse</a> non contiene un elemento <strong>reultimissimo</strong> oppure l'elemento <strong>requeste</strong> è vuoto.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>L'ispezione del messaggio indica che l'elemento <strong>Repiù recente</strong> non è presente o è vuoto.</td>
</tr>
<tr class="even">
<td>Il valore dell'elemento <strong>Repiù recente</strong> in un messaggio <a href="getresponse--metadata-exchange--message.md">GetResponse</a> non corrisponde al valore dell'elemento <strong>MessageID</strong> del messaggio <a href="get--metadata-exchange--http-request-and-message.md">Get</a> corrispondente.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Controllo delle tracce di rete per lo scambio di metadati HTTP</a></td>
<td>L'ispezione del messaggio indica che l'elemento <strong>Latest</strong> contiene un valore non valido o non corretto.</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla risoluzione dei problemi di WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>
