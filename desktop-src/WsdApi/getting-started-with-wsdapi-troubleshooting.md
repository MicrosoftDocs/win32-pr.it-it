---
description: Esistono due modi per determinare la procedura di diagnostica da usare.
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: Attività iniziali con la risoluzione dei problemi di WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 413146288e6c7fc6e513f994fbe24d6ee9940897f22bcd5a715ae41f77f83c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738617"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a>Attività iniziali con la risoluzione dei problemi di WSDAPI

Questa guida alla risoluzione dei problemi contiene un set [di procedure di diagnostica](wsdapi-diagnostic-procedures.md) che possono essere usate per identificare la causa dei problemi dell'applicazione. Dopo aver identificato correttamente la causa del problema, è possibile applicare le soluzioni suggerite nella procedura di diagnostica per risolvere il problema.

Esistono due modi per determinare la procedura di diagnostica da usare. Un modo consiste nel passare alla pagina di risoluzione dei problemi per il tipo di client per visualizzare un elenco di procedure di diagnostica dettagliate da usare per risolvere i problemi del client. L'altro modo è passare alla guida di riferimento rapido per la risoluzione dei problemi riportata di seguito per visualizzare le tabelle di riepilogo che mostrano i problemi comuni con le applicazioni WSDAPI e le procedure da usare per diagnosticare i problemi.

## <a name="troubleshooting-by-type-of-client"></a>Risoluzione dei problemi per tipo di client

Negli argomenti seguenti vengono illustrate le procedure di diagnostica pertinenti in base al tipo di client. Questi argomenti illustrano anche i modelli di messaggio associati al tipo di client.

-   [Risoluzione dei problemi delle applicazioni WSDAPI tramite l'individuazione diretta](troubleshooting-applications-using-directed-discovery.md)
-   [Risoluzione dei problemi relativi ai client di individuazione delle funzioni](troubleshooting-function-discovery-clients.md)
-   [Risoluzione dei Persone nelle vicinanze/riunioni nelle vicinanze](troubleshooting-people-near-me-meetings-near-me.md)
-   [Risoluzione dei problemi relativi all'Aggiunta guidata stampante](troubleshooting-the-add-printer-wizard.md)
-   [Risoluzione dei problemi Esplora rete](troubleshooting-the-network-explorer.md)
-   [Risoluzione dei problemi della Creazione guidata proiettore](troubleshooting-the-projector-wizard.md)
-   [Risoluzione dei problemi di altre applicazioni WSDAPI](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a>Guida di riferimento rapido per la risoluzione dei problemi

Le tabelle seguenti illustrano alcuni problemi che possono impedire ai client e agli host WSDAPI di visualizzare l'un l'altro nella rete e di scambiare i metadati del dispositivo. Le tabelle mostrano anche le procedure di diagnostica da eseguire e i criteri da usare per valutare se l'applicazione presenta un problema specifico.

### <a name="network-environment-problems"></a>Problemi dell'ambiente di rete



| Problema                                                                                                                                                                                              | Procedura di diagnostica                                                                                                                                                                                                                             | Identificazione del problema                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il firewall blocca il traffico di Individuazione rete.                                                                                                                                                       | [Ispezione dell'adapter e del firewall Impostazioni](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | L'abilitazione dell'eccezione di individuazione di rete nel firewall risolve il problema.                                                                                                                      |
| Le eccezioni del firewall specifiche per l'applicazione bloccano i messaggi.                                                                                                                               | [Ispezione dell'adapter e del firewall Impostazioni](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | La disabilitazione del firewall risolve il problema. WF.msc mostra le regole del firewall specifiche dell'applicazione.                                                                                                      |
| Il dispositivo non risponde alle richieste UDP inviando un messaggio [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) in modo orario (meno di 4 secondi). | [Ispezione dell'adapter e del firewall Impostazioni](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | La disabilitazione del firewall risolve il problema e un host generico che risponde in meno di 4 secondi funziona correttamente.                                                                            |
| Il contesto di sicurezza dell'applicazione non è corretto, ovvero il client e l'host non dispongono delle autorizzazioni appropriate per la rete.                                                                 | [Uso di un host generico e di un client per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) o di un host generico e [di un client per i metadati HTTP Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) | L'indirizzo del dispositivo non viene visualizzato nell'output del client di debug WSD. L'esecuzione dell'applicazione come amministratore risolve il problema.                                                                          |
| Un criterio IPSec blocca i messaggi.                                                                                                                                                                | [Uso di un host generico e di un client per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) o di un host generico e [di un client per i metadati HTTP Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) | L'indirizzo del dispositivo non viene visualizzato nell'output del client di debug WSD. Il problema non viene risolto disabilitando il firewall. Il problema non può essere riprodotto in un computer non soggetto ad alcun criterio IPSec. |



 

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
<td><a href="hello-message.md">I</a>messaggi Hello , <a href="probe-message.md">Probe</a>o <a href="resolve-message.md">Resolve</a> non vengono trasmessi in rete perché l'applicazione non enumera correttamente le interfacce di rete multicast.</td>
<td><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Uso del client di debug WSD per verificare il traffico multicast</a></td>
<td>I messaggi Hello, Probe o Resolve non vengono visualizzati nell'output del client di debug WSD. I pacchetti non vengono visualizzati nella rete. I pacchetti non vengono generati per l'interfaccia di loopback o per altre interfacce.</td>
</tr>
<tr class="even">
<td><a href="probe-message.md">I</a> messaggi di probe non vengono inviati dal multicast UDP alla porta 3702 (per le applicazioni che non usano l'individuazione diretta).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Analisi delle tracce di rete per l'individuazione WS-UDP</a></td>
<td>L'ispezione del messaggio indica che è stato inviato alla porta errata.</td>
</tr>
<tr class="odd">
<td>Il <a href="probe-message.md">messaggio Probe</a> non contiene un elemento <strong>Types</strong> oppure l'elemento <strong>Types</strong> è vuoto.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Ispezione delle tracce di rete per l'individuazione WS-UDP</a> o ispezione delle tracce di rete per <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">le applicazioni tramite individuazione diretta</a></td>
<td>L'ispezione del messaggio indica che <strong>l'elemento Types</strong> non è presente o vuoto.</td>
</tr>
<tr class="even">
<td><strong>L'elemento Types</strong> di un <a href="probe-message.md">messaggio Probe</a> non contiene i tipi a cui risponderà un host.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Ispezione delle tracce di rete per l'individuazione WS-UDP</a> o ispezione delle tracce di rete per <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">le applicazioni tramite individuazione diretta</a></td>
<td>L'ispezione del messaggio mostra che <strong>l'elemento Types</strong> contiene un valore non valido o non corretto.</td>
</tr>
<tr class="odd">
<td>Un <a href="probematches-message.md">messaggio ProbeMatches</a> non è stato inviato unicast alla porta UDP da cui <a href="probe-message.md">è</a> stato inviato il probe.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Ispezione delle tracce di rete per l'individuazione WS-UDP</a> o ispezione delle tracce di rete per <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">le applicazioni tramite individuazione diretta</a></td>
<td>L'ispezione dell'output indica che non è stato inviato alcun messaggio <a href="probematches-message.md">ProbeMatches</a>o che il messaggio è stato inviato alla porta errata.
<blockquote>
[!Note]<br />
Per le applicazioni che usano l'individuazione diretta, è necessario inviare <a href="probematches-message.md">ProbeMatches</a> tramite HTTP o HTTPS in risposta al messaggio <a href="probe-message.md">Probe.</a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Il <a href="probematches-message.md">messaggio ProbeMatches</a> non contiene un <strong>elemento RelatesTo</strong> oppure l'elemento <strong>RelatesTo</strong> è vuoto.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Ispezione delle tracce di rete per l'individuazione WS-UDP</a> o ispezione delle tracce di rete per <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">le applicazioni tramite individuazione diretta</a></td>
<td>L'ispezione del messaggio indica che <strong>l'elemento RelatesTo</strong> non è presente o vuoto.</td>
</tr>
<tr class="odd">
<td>Il valore <strong>dell'elemento RelatesTo</strong> in <a href="probematches-message.md">un messaggio ProbeMatches</a> non corrisponde al valore dell'elemento <strong>MessageId</strong> del messaggio <a href="probe-message.md">Probe</a> corrispondente.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Ispezione delle tracce di rete per l'individuazione WS-UDP</a> o ispezione delle tracce di rete per <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">le applicazioni tramite individuazione diretta</a></td>
<td>L'ispezione del messaggio mostra che <strong>l'elemento RelatesTo</strong> contiene un valore in formato non corretto o non corretto.</td>
</tr>
<tr class="even">
<td><strong>L'elemento XAddrs</strong> incluso in <a href="probematches-message.md">un messaggio ProbeMatches</a> non è conforme alle <a href="xaddr-validation-rules.md">regole di convalida XAddr</a>.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Ispezione delle tracce di rete per l'individuazione WS-UDP</a> o ispezione delle tracce di rete per <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">le applicazioni tramite individuazione diretta</a></td>
<td>L'ispezione del messaggio indica che <strong>XAddrs</strong> non è valido.</td>
</tr>
<tr class="odd">
<td><a href="resolve-message.md">I</a> messaggi di risoluzione non vengono inviati dal multicast UDP alla porta 3702 (per le applicazioni che non usano l'individuazione diretta).</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Ispezione delle tracce di rete per l'individuazione WS-UDP</a> o ispezione delle tracce di rete per <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">le applicazioni tramite individuazione diretta</a></td>
<td>L'ispezione dell'output mostra che <a href="resolve-message.md">il messaggio Resolve</a> è stato inviato alla porta errata.</td>
</tr>
<tr class="even">
<td>Un <a href="resolvematches-message.md">messaggio ResolveMatches</a> non è stato inviato unicast alla porta UDP da cui è <a href="resolve-message.md">stato inviato un messaggio</a> Resolve.</td>
<td><a href="inspecting-network-traces-for-udp-ws-discovery.md">Ispezione delle tracce di rete per l'individuazione WS-UDP</a> o ispezione delle tracce di rete per <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">le applicazioni tramite individuazione diretta</a></td>
<td>L'ispezione dell'output indica che non è stato inviato alcun messaggio <a href="resolvematches-message.md">ResolveMatches</a> o che il messaggio è stato inviato alla porta errata.</td>
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
<td>L'indirizzo di trasporto annunciato dall'host è errato.</td>
<td><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Uso di un host generico e di un client per i metadati HTTP Exchange</a></td>
<td>L'ispezione degli XAddrs nell'output del client di debug WSD mostra che l'indirizzo di trasporto è errato o in formato non corretto.</td>
</tr>
<tr class="even">
<td>Impossibile stabilire una connessione TCP per lo scambio di metadati.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>L'output dell'analizzatore di pacchetti non mostra lo scambio di pacchetti seguente:
<ul>
<li>Un pacchetto TCP SYN inviato dal client</li>
<li>Pacchetto SYN/ACK TCP inviato dall'host</li>
<li>Un pacchetto TCP ACK inviato dal client</li>
</ul></td>
</tr>
<tr class="odd">
<td>Il client non ha inviato una richiesta HTTP GET valida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>Non è presente alcuna richiesta HTTP GET nell'output dell'analizzatore di pacchetti o il formato della richiesta non è corretto.</td>
</tr>
<tr class="even">
<td>Il client non ha inviato un messaggio WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">get</a> valido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>Non è presente alcun WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">get</a> message nell'output dell'analizzatore di pacchetti o il formato del messaggio non è corretto.</td>
</tr>
<tr class="odd">
<td>L'host non è in ascolto sul percorso URL specificato nella richiesta HTTP GET.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>Non è presente alcuna risposta HTTP nell'output dell'analizzatore di pacchetti.</td>
</tr>
<tr class="even">
<td>Il WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> non contiene un elemento <strong>To</strong> oppure l'elemento <strong>To</strong> è vuoto.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>L'ispezione del messaggio indica che <strong>l'elemento To</strong> non è presente o vuoto.</td>
</tr>
<tr class="odd">
<td>Il valore <strong>dell'elemento To</strong> di un messaggio WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> non corrisponde a uno degli indirizzi endpoint dell'host.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>L'ispezione del messaggio mostra che il valore dell'elemento <strong>To</strong> non corrisponde a uno degli indirizzi endpoint annunciati nel messaggio <a href="probematches-message.md">ProbeMatches</a> o <a href="resolvematches-message.md">ResolveMatches</a> dell'host.</td>
</tr>
<tr class="even">
<td>L'host non ha inviato un'intestazione di risposta HTTP valida.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>Non è presente alcuna risposta HTTP nell'output dell'analizzatore di pacchetti o il formato della richiesta non è corretto.</td>
</tr>
<tr class="odd">
<td>L'intestazione della risposta HTTP inviata dall'host indica che la richiesta non può essere completata.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>L'intestazione della risposta ha un codice di stato diverso da HTTP/1.1 200.</td>
</tr>
<tr class="even">
<td>L'host non ha inviato un messaggio <a href="getresponse--metadata-exchange--message.md">GetResponse</a> valido.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>Non è presente alcun <a href="getresponse--metadata-exchange--message.md">messaggio GetResponse</a> nell'output dell'analizzatore di pacchetti o il formato del messaggio non è corretto.</td>
</tr>
<tr class="odd">
<td>Il <a href="getresponse--metadata-exchange--message.md">messaggio GetResponse</a> non contiene un <strong>elemento RelatesTo</strong> oppure <strong>l'elemento RelatesTo</strong> è vuoto.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>L'ispezione del messaggio indica che <strong>l'elemento RelatesTo</strong> non è presente o vuoto.</td>
</tr>
<tr class="even">
<td>Il valore <strong>dell'elemento RelatesTo</strong> in un <a href="getresponse--metadata-exchange--message.md">messaggio GetResponse</a> non corrisponde al valore dell'elemento <strong>MessageId</strong> del messaggio <a href="get--metadata-exchange--http-request-and-message.md">Get</a> corrispondente.</td>
<td><a href="inspecting-network-traces-for-http-metadata-exchange.md">Analisi delle tracce di rete per i metadati HTTP Exchange</a></td>
<td>L'ispezione del messaggio indica che <strong>l'elemento RelatesTo</strong> contiene un valore non valido o non corretto.</td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla risoluzione dei problemi di WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>
