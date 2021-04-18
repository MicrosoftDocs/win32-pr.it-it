---
title: Gestione tabelle di routing
description: Gestione tabelle di routing è il repository centrale di informazioni di routing per tutti i protocolli di routing che operano nel servizio Routing e accesso remoto (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297829"
---
# <a name="routing-table-manager"></a>Gestione tabelle di routing

Gestione tabelle di routing è il repository centrale di informazioni di routing per tutti i protocolli di routing che operano nel servizio Routing e accesso remoto (RRAS). Invia una notifica ai client quando si sono verificate modifiche e consente ai client di scambiare informazioni private.

Gestione tabelle di routing fornisce informazioni di routing a tutti i client interessati, ad esempio i protocolli di routing, i programmi di gestione e i programmi di monitoraggio. Gestione tabelle di routing determina inoltre il percorso migliore per ogni rete di destinazione nota ai protocolli di routing. Gestione tabelle di routing determina questa route in base alle priorità del protocollo di routing e alle metriche associate alle route. La persona che gestisce il router può configurare le priorità del protocollo di routing tramite la console di gestione di RRAS.

Gestione tabelle di routing passa le informazioni sulla route migliore ai server d'inoltro (uno per famiglia di indirizzi o uno per interfaccia) e a tutti i client interessati.

Ogni client esegue la registrazione con gestione tabelle di routing e in return riceve un handle che il client usa per aggiungere o eliminare route. I client possono recuperare le informazioni archiviate nella tabella di routing. Inoltre, i client possono eseguire la registrazione con gestione tabelle di routing per ricevere notifiche delle modifiche apportate al percorso migliore a una destinazione.

 

 




