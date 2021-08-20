---
description: Elenca le procedure di diagnostica da utilizzare per la risoluzione dei problemi Esplora rete.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Risoluzione dei problemi del Esplora rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a7c8e270fa3f1e07ce9b44fb9ce619d9fe5225e2c4d3ae87896d5e7cf20a2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120581"
---
# <a name="troubleshooting-the-network-explorer"></a>Risoluzione dei problemi del Esplora rete

La Esplora rete:

-   Usa sempre l'WS-Discovery UDP per l'individuazione dei dispositivi
-   Avvia sempre una connessione HTTP o HTTPS per lo scambio di metadati
-   A volte usa un canale sicuro (HTTPS) per lo scambio di metadati

Le procedure di diagnostica seguenti devono essere usate (nell'ordine) per identificare i problemi relativi al Esplora rete.

**Per risolvere i problemi relativi Esplora rete**

1.  [Esaminare le impostazioni della scheda e del firewall.](inspecting-adapter-and-firewall-settings.md)
2.  [Usare un host e un client generici per UDP WS-Discovery.](using-a-generic-host-and-client-for-udp-ws-discovery.md)
3.  [Usare WSD Debug Client per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Esaminare le tracce di rete per UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Usare un host e un client generici per lo scambio di metadati HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
6.  [Usare la registrazione WinHTTP per verificare l'opzione Ottieni traffico](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Esaminare le tracce di rete per lo scambio di metadati HTTP.](inspecting-network-traces-for-http-metadata-exchange.md)

Il Esplora rete usa [l'individuazione delle funzioni per](/previous-versions/windows/desktop/fundisc/fd-portal) enumerare i dispositivi di rete. Per altre informazioni sulla risoluzione dei problemi, vedere [Risoluzione dei problemi dei client di individuazione delle funzioni.](troubleshooting-function-discovery-clients.md)

Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in Abilitazione della traccia [WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali risoluzione dei problemi relativi a WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Risoluzione dei problemi relativi ai client di individuazione delle funzioni](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
