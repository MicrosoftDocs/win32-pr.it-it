---
description: Le applicazioni che usano l'individuazione diretta inviano messaggi Probe su HTTP o HTTPS per individuare i dispositivi.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Risoluzione dei problemi relativi alle applicazioni WSDAPI con individuazione diretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528573"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a>Risoluzione dei problemi relativi alle applicazioni WSDAPI con individuazione diretta

Le applicazioni che usano l'individuazione diretta inviano messaggi [Probe](probe-message.md) su http o HTTPS per individuare i dispositivi. I messaggi [ProbeMatches](probematches-message.md) corrispondenti inviati in risposta vengono inviati anche tramite http o HTTPS. L'individuazione diretta può essere avviata dall'aggiunta guidata stampante, da un client di individuazione funzioni o da un'applicazione WSDAPI. I messaggi Probe e ProbeMatches sono strutturalmente identici a quelli inviati tramite UDP. I messaggi sono preceduti dalle intestazioni HTTP o HTTPS appropriate.

Le seguenti procedure di diagnostica devono essere utilizzate (in ordine) per identificare i problemi di un'applicazione mediante l'individuazione diretta.

**Per risolvere i problemi di un'applicazione WSDAPI utilizzando l'individuazione diretta**

1.  [Controllare le impostazioni del firewall e dell'adapter](inspecting-adapter-and-firewall-settings.md).
2.  [Usare un host e un client generici per lo scambio di metadati http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Usare la registrazione WinHTTP per verificare l'ottenimento del traffico](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Esaminare le tracce di rete per un'applicazione usando l'individuazione diretta](inspecting-network-traces-for-applications-using-directed-discovery.md).

Se non è possibile identificare l'origine del problema usando le procedure di diagnostica precedenti, seguire le istruzioni riportate in [Abilitazione della traccia di WSDAPI](enabling-wsdapi-tracing.md) e contattare il supporto tecnico Microsoft.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Risoluzione dei problemi relativi all'aggiunta guidata stampante](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[Risoluzione dei problemi relativi alle applicazioni WSDAPI](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



