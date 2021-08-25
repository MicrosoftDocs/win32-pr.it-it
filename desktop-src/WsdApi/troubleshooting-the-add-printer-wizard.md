---
description: Elenca le procedure di diagnostica da usare per la risoluzione dei problemi dell'Installazione guidata stampante.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Risoluzione dei problemi relativi all'Aggiunta guidata stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6c6971108b0f6fb46a373be47943a3ccbc7fcd97b830733c139653f991debd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860051"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Risoluzione dei problemi relativi all'Aggiunta guidata stampante

Aggiunta guidata stampante:

-   Usa sempre il WS-Discovery UDP per l'individuazione dei dispositivi
-   Avvia sempre una connessione HTTP o HTTPS per lo scambio di metadati
-   A volte usa l'individuazione diretta
-   A volte usa un canale sicuro (HTTPS) per lo scambio di metadati

Per identificare i problemi relativi all'Installazione guidata stampante, è necessario usare le procedure di diagnostica seguenti.

**Per risolvere i problemi relativi all'Installazione guidata stampante**

1.  Se si usa l'individuazione diretta, risolvere [i problemi relativi all'individuazione diretta.](troubleshooting-applications-using-directed-discovery.md)
2.  [Esaminare le impostazioni dell'adapter e del firewall.](inspecting-adapter-and-firewall-settings.md)
3.  [Usare un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Usare il client di debug WSD per verificare il traffico multicast.](using-wsddebug-client-to-verify-multicast-traffic.md)
5.  [Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
6.  [Usare un host e un client generici per lo scambio di metadati HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
7.  [Usare la registrazione WinHTTP per verificare ottenere il traffico](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Esaminare le tracce di rete per lo scambio di metadati HTTP.](inspecting-network-traces-for-http-metadata-exchange.md)

Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in Abilitazione della traccia [WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Risoluzione dei problemi relativi alle applicazioni tramite individuazione diretta](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



