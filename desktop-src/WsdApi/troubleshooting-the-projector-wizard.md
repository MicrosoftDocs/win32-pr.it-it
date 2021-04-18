---
description: Elenca le procedure di diagnostica da utilizzare per la risoluzione dei problemi relativi alla procedura guidata del proiettore.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Risoluzione dei problemi relativi alla procedura guidata del proiettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306865"
---
# <a name="troubleshooting-the-projector-wizard"></a>Risoluzione dei problemi relativi alla procedura guidata del proiettore

Creazione guidata proiettore:

-   Usa sempre WS-Discovery UDP per l'individuazione dei dispositivi
-   Usa sempre HTTP per lo scambio di metadati
-   A volte usa l'individuazione diretta

Per identificare i problemi relativi alla procedura guidata del proiettore, è necessario utilizzare le seguenti procedure di diagnostica (in ordine).

**Per risolvere i problemi relativi alla procedura guidata del proiettore**

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

 

 



