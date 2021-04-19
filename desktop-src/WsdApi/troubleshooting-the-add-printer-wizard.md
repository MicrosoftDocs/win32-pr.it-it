---
description: Elenca le procedure di diagnostica da utilizzare per la risoluzione dei problemi relativi all'aggiunta guidata stampante.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Risoluzione dei problemi relativi all'aggiunta guidata stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310269"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Risoluzione dei problemi relativi all'aggiunta guidata stampante

Aggiunta guidata stampante:

-   Usa sempre WS-Discovery UDP per l'individuazione dei dispositivi
-   Avvia sempre una connessione HTTP o HTTPS per lo scambio di metadati
-   A volte usa l'individuazione diretta
-   USA a volte un canale sicuro (HTTPS) per lo scambio di metadati

Le seguenti procedure di diagnostica devono essere utilizzate (in ordine) per facilitare l'identificazione dei problemi con l'aggiunta guidata stampante.

**Per risolvere i problemi relativi all'aggiunta guidata stampante**

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
</dt> <dt>

[Risoluzione dei problemi relativi alle applicazioni mediante l'individuazione diretta](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



