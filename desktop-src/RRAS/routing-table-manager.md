---
title: Gestione tabelle di routing
description: Il gestore tabelle di routing è il repository centrale delle informazioni di routing per tutti i protocolli di routing che operano nel servizio Routing e Accesso remoto (RRAS).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 850726cd2203eca85be33aea3bd33f1ed903ba2d197d102ff7de294c5e852626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787469"
---
# <a name="routing-table-manager"></a>Gestione tabelle di routing

Il gestore tabelle di routing è il repository centrale delle informazioni di routing per tutti i protocolli di routing che operano nel servizio Routing e Accesso remoto (RRAS). Notifica ai client quando sono state apportate modifiche e consente ai client di scambiare informazioni private.

Il gestore tabelle di routing fornisce informazioni di routing a tutti i client interessati, ad esempio protocolli di routing, programmi di gestione e programmi di monitoraggio. Il gestore tabelle di routing determina anche la route migliore per ogni rete di destinazione nota ai protocolli di routing. Il gestore tabelle di routing determina questa route in base alle priorità del protocollo di routing e alle metriche associate alle route. La persona che amministra il router può configurare le priorità del protocollo di routing usando la console di gestione di RRAS.

Il gestore tabelle di routing passa le informazioni di route migliori ai server d'inoltro (una per famiglia di indirizzi o una per interfaccia) e a tutti i client interessati.

Ogni client viene registrato con il gestore tabelle di routing e in cambio riceve un handle che il client usa per aggiungere o eliminare route. I client possono recuperare le informazioni archiviate nella tabella di routing. Inoltre, i client possono registrarsi con il gestore tabelle di routing per ricevere la notifica delle modifiche alla route migliore verso una destinazione.

 

 




