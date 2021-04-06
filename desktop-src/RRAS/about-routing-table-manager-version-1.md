---
title: Informazioni su Routing Table Manager versione 1
description: Gestione tabelle di routing è un repository centrale di informazioni di routing per tutti i protocolli di routing che operano con il servizio Routing e accesso remoto (RRAS).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Servizio Routing e accesso remoto RRAS, gestione tabelle di routing versione 1
- Servizio Routing e accesso remoto RRAS, gestione tabelle di routing versione 1, descritta
- Gestione tabelle di routing versione 1 RRAS
- Gestione tabelle di routing versione 1 RRAS, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044837"
---
# <a name="about-routing-table-manager-version-1"></a>Informazioni su Routing Table Manager versione 1

**Windows Server 2003:** Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le nuove applicazioni devono usare l'API di Routing Table Manager versione 2.

Gestione tabelle di routing è un repository centrale di informazioni di routing per tutti i protocolli di routing che operano con il servizio Routing e accesso remoto (RRAS). Gestione tabelle di routing fornisce informazioni di routing a tutti i componenti interessati, ad esempio i protocolli di routing, gli agenti di gestione e gli agenti di monitoraggio. Gestione tabelle di routing determina inoltre la migliore route per ogni rete di destinazione nota ai protocolli di routing. Determina questa route in base alle priorità del protocollo di routing e alle metriche associate alle route. Si noti che l'amministratore è in grado di configurare le priorità del protocollo di routing. Gestione tabelle di routing passa quindi le informazioni sulle route migliori sui server d'inoltro e di nuovo ai protocolli di routing.

Ogni protocollo di routing chiama [**RtmRegisterClient**](rtmregisterclient.md) per la registrazione con gestione tabelle di routing. **RtmRegisterClient** restituisce un handle utilizzato dal protocollo di routing per aggiungere o eliminare le voci della route. **RtmRegisterClient** consente inoltre al protocollo di routing di registrare un oggetto evento con gestione tabelle di routing. Questo oggetto evento viene segnalato da Gestione tabelle di routing per notificare al protocollo di routing le modifiche apportate alle informazioni sulla Route consigliata. Tutti gli altri componenti possono ottenere informazioni archiviate in Gestione tabelle di routing tramite l'enumerazione route.

 

 




