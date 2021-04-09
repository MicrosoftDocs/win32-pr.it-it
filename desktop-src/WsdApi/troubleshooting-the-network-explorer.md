---
description: Elenca le procedure di diagnostica da usare per la risoluzione dei problemi di Network Explorer.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Risoluzione dei problemi di Esplora reti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966671"
---
# <a name="troubleshooting-the-network-explorer"></a>Risoluzione dei problemi di Esplora reti

Esplora reti:

-   Usa sempre WS-Discovery UDP per l'individuazione dei dispositivi
-   Avvia sempre una connessione HTTP o HTTPS per lo scambio di metadati
-   USA a volte un canale sicuro (HTTPS) per lo scambio di metadati

Per identificare i problemi con Esplora reti, è necessario usare le procedure di diagnostica seguenti (in ordine).

**Per risolvere i problemi di Esplora reti**

1.  [Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).
2.  [Utilizzare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Usare il client di debug WSD per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).

Esplora reti usa l' [individuazione funzione](/previous-versions/windows/desktop/fundisc/fd-portal) per enumerare i dispositivi di rete. Per ulteriori informazioni sulla risoluzione dei problemi, vedere [risoluzione dei problemi relativi ai client di individuazione funzioni](troubleshooting-function-discovery-clients.md).

Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Risoluzione dei problemi relativi ai client di individuazione delle funzioni](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
