---
description: Elenca le procedure di diagnostica da usare per la risoluzione dei problemi della Creazione guidata proiettore.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Risoluzione dei problemi relativi alla creazione guidata del proiettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5767e9827174d2d8135ac6dfb96c335d49acb82f0a0162b06f22a89c4dbdebef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856071"
---
# <a name="troubleshooting-the-projector-wizard"></a>Risoluzione dei problemi relativi alla creazione guidata del proiettore

Creazione guidata proiettore:

-   Usa sempre l'WS-Discovery UDP per l'individuazione dei dispositivi
-   Usa sempre HTTP per lo scambio di metadati
-   A volte usa l'individuazione diretta

Le procedure di diagnostica seguenti devono essere usate (in ordine) per identificare i problemi relativi alla Creazione guidata proiettore.

**Per risolvere i problemi della creazione guidata del proiettore**

1.  Se si usa l'individuazione diretta, risolvere [i problemi relativi all'individuazione diretta.](troubleshooting-applications-using-directed-discovery.md)
2.  [Esaminare le impostazioni della scheda e del firewall.](inspecting-adapter-and-firewall-settings.md)
3.  [Usare un host e un client generici per UDP WS-Discovery.](using-a-generic-host-and-client-for-udp-ws-discovery.md)
4.  [Usare WSD Debug Client per verificare il traffico multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
5.  [Esaminare le tracce di rete per UDP WS-Discovery.](inspecting-network-traces-for-udp-ws-discovery.md)
6.  [Usare un host e un client generici per lo scambio di metadati HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
7.  [Usare la registrazione WinHTTP per verificare l'opzione Ottieni traffico](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Esaminare le tracce di rete per lo scambio di metadati HTTP.](inspecting-network-traces-for-http-metadata-exchange.md)

Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in Abilitazione della traccia [WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali risoluzione dei problemi relativi a WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



