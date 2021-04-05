---
description: Elenca le procedure di diagnostica da utilizzare per la risoluzione dei problemi relativi ai client di individuazione funzioni.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Risoluzione dei problemi relativi ai client di individuazione delle funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753666"
---
# <a name="troubleshooting-function-discovery-clients"></a>Risoluzione dei problemi relativi ai client di individuazione delle funzioni

Client di individuazione funzioni:

-   Usare sempre WS-Discovery UDP per l'individuazione dei dispositivi
-   Avviare sempre le connessioni HTTP o HTTPS per lo scambio di metadati
-   USA a volte l'individuazione diretta
-   USA a volte un canale sicuro (HTTPS) per lo scambio di metadati

Nell'elenco seguente viene illustrata la sequenza tipica dei messaggi inviati e ricevuti dai client di individuazione funzioni. Non tutti i messaggi sono obbligatori.

1.  Il client invia un messaggio [Probe](probe-message.md) per individuare i dispositivi e i servizi. Se il client utilizza l'individuazione diretta, il messaggio viene inviato tramite HTTP o HTTPS. in caso contrario, il messaggio viene inviato dal multicast UDP alla porta 3702.
2.  Il client riceve i messaggi [ProbeMatches](probematches-message.md) da dispositivi o servizi corrispondenti. I messaggi di individuazione indirizzati vengono inviati tramite HTTP o HTTPS. in caso contrario, questi messaggi vengono inviati dall'unicast UDP e provengono dalla porta 3702.
3.  Se non è stato incluso alcun XAddrs nel messaggio ProbeMatches, il client invierà un messaggio di [risoluzione](resolve-message.md) tramite multicast UDP alla porta 3702.
4.  Se è stato inviato un messaggio di [risoluzione](resolve-message.md) , il client riceve un messaggio [ResolveMatches](resolvematches-message.md) dai servizi corrispondenti. Questo messaggio viene inviato dall'unicast UDP dalla porta 3702 alla porta in cui ha avuto origine il messaggio di risoluzione.
5.  Il client invia un messaggio [Get](get--metadata-exchange--http-request-and-message.md) per richiedere i metadati dal dispositivo o dal servizio. Questo messaggio viene inviato da HTTP o HTTPS.
6.  Il client riceve un messaggio [GetResponse](getresponse--metadata-exchange--message.md) con i metadati del dispositivo o del servizio. Questo messaggio viene inviato da HTTP o HTTPS.

Le seguenti procedure di diagnostica devono essere utilizzate (in ordine) per facilitare l'identificazione dei problemi relativi a un client di individuazione delle funzioni.

**Per risolvere i problemi relativi a un client di individuazione funzioni**

1.  Se si usa l'individuazione diretta, [risolvere i problemi di individuazione diretta](troubleshooting-applications-using-directed-discovery.md).
2.  [Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).
3.  [Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
5.  [Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
6.  [Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
7.  [Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).

Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



